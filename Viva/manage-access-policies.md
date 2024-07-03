---
title: "Microsoft Viva - Feature access management using PowerShell"
ms.reviewer: elizapo
ms.author: loreenl
author: loreenl
manager: elizapo
ms.date: 07/02/2024
audience: Admin
f1.keywords:
- NOCSH
ms.topic: article
ms.service: viva-suite
ms.localizationpriority: medium
ms.custom:
ms.collection:  
- M365initiative-viva
- m365solution-overview
- highpri
- tier1
search.appverid:
- MET150
description: "Control who can access features in Microsoft Viva using PowerShell"
---

# Control access to features in Viva using PowerShell

You can use access policies in Viva to manage which users can access specific features in Viva apps with PowerShell. Feature access management lets you enable or disable specific features in Viva for specific groups or users in your tenant and so tailor your deployments to meet your local regulatory and business requirements.  

> [!IMPORTANT]
> You can have multiple access policies for a feature active in your organization. That means that a user or group could be impacted by multiple policies. In that case, the most restrictive policy assigned directly to a user or group takes precedence. For more information, see [How access policies work in Viva](\viva\feature-access-management#how-access-policies-work-in-viva).

An authorized admin in your tenant can create, assign, and manage access policies from PowerShell. When a user signs into Viva, the policy settings are applied, and they only see the features that haven't been disabled.

> [!NOTE]
> You can only disable a subset of features in Viva apps by using feature access management. Restricting the use of one feature might impact the functionality of other features in the app. Be sure to check the app documentation on the specific feature to understand the implications of disabling or enabling access to a feature.

## Features available for feature access management

You can use feature access management to manage access to the following features:

> [!NOTE]
> - For information on the impact of policies on your tenant or the users in your tenant, refer to the feature documentation by using the link in the table. 
> - Only some features have the controls available for admins to provide users with the option to opt out.

|App|Feature|Control for user opt-out?|Who can manage access|ModuleID|
|-|-|-|-|-|
|Engage|[Copilot in Engage](/viva/engage/configure-copilot-for-engage)|No|Engage admin|VivaEngage|
||[AI Summarization](/viva/engage/configure-copilot-for-engage)|Yes|Engage admin|VivaEngage|
|Insights|[Copilot Dashboard](/viva/insights/org-team-insights/copilot-dashboard)|No|Global admin|VivaInsights|
||[Copilot Dashboard Auto Enablement](/viva/insights/org-team-insights/copilot-dashboard#remove-access-to-the-dashboard-for-the-entire-tenant-with-powershell)|No|Global admin|VivaInsights|
||[Digest Welcome Email](/viva/insights/advanced/setup-maint/configure-personal-insights#configure-access-at-the-tenant-level)|No| Global admin|VivaInsights|
||[Meeting cost and quality](https://aka.ms/meetingcostandqualitypost)|No|Insights admin|VivaInsights|
||[Reflection](https://support.microsoft.com/topic/reflect-in-viva-insights-55379cb7-cf2a-408d-b740-2b2082eb3743)|No|Insights admin|VivaInsights|
|Pulse|[Customization](/viva/pulse/setup-admin-access/set-up-in-app-pulse-experience#customization)|No|Global admin|VivaPulse|
||Team conversations in Pulse reports*|No|Global admin|VivaPulse|
|Skills|[Skill suggestions](/viva/skills/skills-overview)*|Yes|Knowledge admin|VivaSkills| 


\* The feature or feature control might not yet be available for all tenants. Support will be added soon.

> [!NOTE]
> - You can only control access to features that support access policies *and* that are available in your tenant. For example, if you have an EDU-based tenant, you cannot use policies to gain access to features that are not available to EDU tenants. The same applies for features that are unavailable in specific geographies. Check the documentation for the specific feature that you'd like to use for more information about its availability.
> - Changes to the Copilot in Viva Engage feature might take up to 48 hours to take effect. Changes for other features generally take effect within 24 hours.

## Requirements

Before you can create an access policy in Viva, you need:

- A [supported version of Microsoft 365 or a Viva Suite license](https://www.microsoft.com/microsoft-viva/pricing)
- Access to [Exchange Online PowerShell Version 3.2.0](https://www.powershellgallery.com/packages/ExchangeOnlineManagement/3.2.0) or later
- User accounts created in or synchronized to Microsoft Entra ID
- Microsoft 365 groups, Microsoft Entra security groups created in or synchronized to Microsoft Entra ID, or distribution groups. Groups must be mail-enabled (have an associated email address). The membership type can be either dynamic or assigned.
- The [role required for the specific app and feature](/viva/feature-access-management#features-available-to-manage).


> [!IMPORTANT]
> Viva feature access management isn’t available to customers who have Microsoft 365 GCC, GCC High, or DOD plans.

## Create and manage access policies for Viva features
[See which features you can manage and who can manage them](/viva/feature-access-management#features-available-to-manage).

### Get the featureID for the feature
Before you can create an access policy, use the ModuleID to get the **featureID** for the specific feature you want to control access to.

Use the [**Get-VivaModuleFeature**](/powershell/module/exchange/get-vivamodulefeature) PowerShell cmdlet to get a list of all of the features available in a specific Viva app and their associated IDs.

1. Install Exchange Online PowerShell Version 3.2.0 or later:

   ```PowerShell
   Install-Module -Name ExchangeOnlineManagement
   ```

2. Connect to Exchange Online with admin credentials:

   ```PowerShell
   Connect-ExchangeOnline
   ```

   Complete the authentication as the role required for the specific feature you're creating the policy for.

3. Run the [Get-VivaModuleFeature](/powershell/module/exchange/get-vivamodulefeature) cmdlet to see the features that you can manage by using an access policy.  

   For example, to see which features are supported in Viva Insights, run the following cmdlet:

   ```PowerShell
   Get-VivaModuleFeature -ModuleId VivaInsights
   ```
4. Find the feature that you'd like to create an access policy for and make note of its **featureID**.

### Create an access policy

Now that you have the **featureID**, use the [**Add-VivaModuleFeaturePolicy**](/powershell/module/exchange/add-vivamodulefeaturepolicy) PowerShell cmdlet to create an access policy for the feature.

You can assign a maximum of 10 policies per feature to users and groups. Each policy can be assigned to a maximum of 20 users or groups. You can assign one additional policy per feature to the entire tenant by using the *-Everyone* parameter, which will function as a global default state for that feature across your organization.

Run the [Add-VivaModuleFeaturePolicy](/powershell/module/exchange/add-vivamodulefeaturepolicy) cmdlet to create a new access policy.

> [!NOTE]
> If your feature supports user controls for opt out, make sure you set the *IsUserControlEnabled* parameter when you create the policy. If you don't, user controls for the policy uses the default state for the feature.

For example, run the following to create an access policy, called *UsersAndGroups*, to restrict access to the Reflection feature in Viva Insights.

   ```powershell
   Add-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -Name UsersAndGroups -IsFeatureEnabled $false -GroupIds group1@contoso.com,group2@contoso.com -UserIds user1@contoso.com,user2@contoso.com    
   ```
This example adds a policy for the Reflection feature in Viva Insights. The policy disables the feature for the specified users and group members. If you want to disable the feature for all users, use the *-Everyone* parameter instead.



### Manage access policies

You can update an access policy to change whether a feature is enabled or disabled, as well as to change who the policy applies to (everyone, a user, or a group).

For example, building on our last example, to update who the policy applies to, run the following cmdlet:

```powershell
Update-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -PolicyId xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx -GroupIds group1@contoso.com,group2@contoso.com
```

Just like when you create the policy, if your policy supports user controls, include the *IsUserControlEnabled* parameter when you change the policy.

> [!IMPORTANT]
> Values that you specify for the *-UserIds* and *-GroupIds* parameters or the *-Everyone* parameter overwrite any existing users or groups. To preserve the existing users and groups, you need to specify those existing users or groups *and* any additional users or groups that you want to add. Not including existing users or groups in the command effectively removes those specific users or groups from the policy. You can't update a policy for a particular user or group to include the entire tenant if a policy for the entire tenant already exists for the feature - only one tenant-wide policy is supported.

To check what features are disabled for a specific user or group, run the [Get-VivaModuleFeatureEnablement](/powershell/module/exchange/get-vivamodulefeatureenablement) cmdlet. This cmdlet returns what's called the *enablement status* for the user or group.

For example:

```powershell
Get-VivaModuleFeatureEnablement -ModuleId VivaInsights -FeatureId Reflection -Identity user@contoso.com
```

### Delete an access policy

Use the [Remove-VivaModuleFeaturePolicy](/powershell/module/exchange/remove-vivamodulefeaturepolicy) cmdlet to delete an access policy.

For example, to delete the Reflection feature access policy, start by getting the specific UID for the access policy - you can get that by running [Get-VivaModuleFeaturePolicy](/powershell/module/exchange/get-vivamodulefeaturepolicy). Then, run the following cmdlet:

```powershell
Remove-VivaModuleFeaturePolicy -ModuleId VivaInsights -FeatureId Reflection -PolicyId xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
```
### Troubleshooting

If you have issues creating or using access policies for Viva app features, confirm the feature you're trying to set a policy for is listed in the [feature table](#features-available-for-feature-access-management) and is available to your tenant.



## More resources

[Microsoft Viva Privacy](/Viva/viva-privacy)

[Microsoft Viva Security](/Viva/microsoft-viva-security)

[Viva admin roles and tasks](/viva/microsoft-viva-admin-roles)
