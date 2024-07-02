---
title: "Microsoft Viva - Managing access policies in Microsoft Viva"
ms.reviewer: loreenl
ms.author: loreenl
author: lizap
manager: elizapo
ms.date: 06/20/2024
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
description: "Control who can access features in Microsoft Viva using the Microsoft 365 admin center"
---
# Managing access policies for Microsoft Viva

To control who has access to specific Viva features you can create and update policies in the [Microsoft 365 admin center](/Viva/control-access-admin-center) or in [Powershell](/Viva/feature-access-management).

Policies are used to enable or disable specific features or types of data processing for users or groups in your tenant.

> [!NOTE]
> These policies are not yet available to customers who have Microsoft 365 GCC, GCC High, or DOD plans.

## Creating and managing policies  

Policies can be created and managed by a Viva admin who has permissions to do so in the Microsoft 365 admin center or by using PowerShell. For more information, see the Who can manage access column in the feature table below.

Policies for copilots in Viva can also be managed through the Copilot settings page in the Microsoft 365 admin center. These policies remain in sync with those managed through Viva admin page.  

### Requirements
Before you can create a policy, you need:  

- A [supported version of Microsoft 365 or a Viva Suite license](https://www.microsoft.com/microsoft-viva/pricing)
- User accounts created in or synchronized to Microsoft Entra ID
- Microsoft 365 groups, Microsoft Entra security groups created in or synchronized to Microsoft Entra ID, or distribution groups.<br>
 Groups must be mail-enabled (have an associated email address). Membership can be either dynamic or assigned. If users are in nested groups and you apply access to the parent group, the users in the nested groups must be created in or synchronized to Microsoft Entra ID.  
- For [PowerShell](/Viva/feature-access-management) - access to Exchange Online PowerShell Version 3.2.0 or later


## Features available to manage

You can use feature access management to manage access to the following features:  

|App|Feature|Control for user opt-out?|Who can manage access|
|-|-|-|-|
|Engage|[Copilot in Engage](/viva/engage/configure-copilot-for-engage)|No|Engage admin|
||[AI Summarization](/viva/engage/configure-copilot-for-engage)|Yes| Engage admin|
|Insights|[Copilot Dashboard](/viva/insights/org-team-insights/copilot-dashboard)|No|Global admin|
||[Copilot Dashboard Auto Enablement](/viva/insights/org-team-insights/copilot-dashboard#remove-access-to-the-dashboard-for-the-entire-tenant-with-powershell)|No|Global admin|
||[Copilot Dashboard Delegation](/viva/insights/org-team-insights/delegate-access)*|No|Global admin|
||[Digest Welcome Email](/viva/insights/advanced/setup-maint/configure-personal-insights#configure-access-at-the-tenant-level)|No| Global admin|
||[Meeting cost and quality](https://aka.ms/meetingcostandqualitypost)|No|Insights admin|
||[Reflection](https://support.microsoft.com/topic/reflect-in-viva-insights-55379cb7-cf2a-408d-b740-2b2082eb3743)|No|Insights admin|
|Pulse|[Customization](/viva/pulse/setup-admin-access/set-up-in-app-pulse-experience#customization)|No|Global admin|
|Skills|[Skill suggestions](/viva/skills/skills-overview)*|Yes|Knowledge admin|

\* The feature or feature control might not yet be available for all tenants. Support will be added soon.

> [!NOTE]
> - For information on the impact of policies on your tenant or the users in your tenant or on the functionality of other features in your tenant, refer to the table below for documentation on the specific feature.  
> - You can control only the access to features that support access policies and that are available in your tenant. For example, if you have an EDU-based tenant, you cannot use policies to gain access to features that are not otherwise available to EDU tenants. Refer to the table below for documentation on the specific feature.
> - You can have multiple access policies for an active feature in your organization, which means a user could be impacted by multiple policies. In that case, the most restrictive policy assigned to the user or group takes precedence. For more information see Which policy takes precedence.
> - Changes to access policies take effect for the user within 24 hours, unless noted for a specific feature. Changes for Copilot in Viva Engage might take up to 48 hours.  
> - Features support org-wide and user/group policies, unless otherwise noted in that app’s feature documentation.

## Which policy takes precedence?  

A user has one effective policy for each feature. It’s possible, or even likely, that a user is directly assigned a policy and is also a member of one or more groups that’s assigned a policy for the same feature. In these kinds of scenarios, a user’s effective policy is determined according to the rules of precedence, as follows:  

If a user is directly assigned a policy as an individual or as a member of a group, that policy takes precedence. If a user has multiple of these policies assigned, then the most restrictive policy they are assigned applies: 

- Feature is disabled 

- Feature is disabled with option for user to opt out (if available for a given feature)  

- Feature is enabled  

If a user is not assigned a policy as an individual or member of a group, the org-wide policy applies. This is either the default setting for the feature or the tenant-wide/org-wide policy created by the admin.  
> [!NOTE]
> - Changes to policies can take up to 24 hours to go into effect for the majority of features. 
> - Changes to policies for the Copilot in Engage feature may take up to 48 hours to go into effect. 

## More
[Learn how to manage access to features in the Microsoft 365 admin center](/viva/control-access-admin-center)

[Learn how to manage access to features using Powershell](/Viva/feature-access-management)
