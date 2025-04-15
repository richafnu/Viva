---
title: "Work with external networks in Viva Engage"
description: "Describes integration of external networks for partners and consultants."
ms.reviewer: blyttle
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 04/15/2025
audience: Admin
f1.keywords:
- NOCSH
ms.topic: how-to
ms.service: viva-engage
ms.localizationpriority: high
ms.collection: 
- M365initiative-viva
- highpri
search.appverid:
- MET150
---

# Work with external networks in Viva Engage

Viva Engage networks support a format called M365 Native Mode which uses Microsoft Entra identities and policies. Native mode operation is **required** for all Viva Engage networks in the enterprise. It enables users, groups, and content to map to their counterparts in Microsoft Entra and Microsoft 365. Native Mode also supports eDiscovery through the Microsoft Purview portal, so your organizations safely and securely collaborate in your Engage network.

Viva Engage legacy external networks require alignment to Microsoft Entra to operate in M365 Native Mode. Customers benefit from the full suite of Microsoft Security and Compliance features.

As of April 2025, nearly all customer organizations with significant Viva Engage networks observe the Native mode standard. Any remaining customers have until June 1st 2025 to complete the alignment of their external network to Microsoft Entra. Use the following procedures to develop your new external network and to migrate data from their existing external network.

## Three-Phase external networks configuration

The following terms are used in this document:

- **Parent network**: Your current Viva Engage network
- **New Entra tenant**: The new Entra tenant that hosts the new external Viva Engage network
- **Legacy external network**: Your current external network
- **New external network**: The new native-on-M365 external network

### Set Up a new Microsoft Entra tenant

New Viva Engage networks always map to a new Microsoft Entra tenant. Every new external network requires its own Microsoft Entra tenant.

Permissions and License requirements include the following:

- Viva Engage external network v2 configuration requires Global Administrator privileges.

- Because the external network uses Microsoft 365 Groups, Entra B2B, and SharePoint Online storage, at least one user in the tenant requires a Microsoft SharePoint license.

- **Recommended license requirement:** Assigning a Microsoft 365 E5 license automatically supports the full Compliance Purview experience.

>[!NOTE]
> During tenant creation, select **Microsoft Entra ID** for the tenant. Avoid use of other values such as *Microsoft Entra ID (B2C)*.

The Global Administrator needs to follow the steps in the following **Create a New Tenant** link from Microsoft Entra.

[QuickStart - Access and create new tenant - Microsoft Entra | Microsoft Learn](./entra/fundamentals/create-new-tenant#create-a-new-tenant-for-your-organization)

After you finish configuring the new tenant, keep its Entra tenant ID handy, because you'll need it for later steps.

>[!NOTE]
> The creation of the new tenant automatically projects the creating user as a B2B Guest user and assigns the Global Administrator role and privileges.

### Connect Engage in the new Entra tenant with the parent Engage network

You apply two important procedures in this step:

- Generate a tenant association token

- Redeem the tenant association token to connect the two Viva Engage networks (the Parent network and the new external network).

#### Generate the tenant association token

In Engage, as a Global Administrator, log into the New Engage Network in the new Entra Tenant by going to engage.cloud.microsoft.

Do the following to access external networks setup:

1. In Engage, select the settings icon, and go to Admin center.

2. In the Admin center, on the Setup and Configuration tab, select external networks.

3. Select **Setup external network**.

4. Select the “Generate Code” tab to generate a one-time code to associate the new external network with the parent Engage network. After you generate the association code, take note as it's used in later steps.

#### Associate the new network with the parent Engage network

1. Log out of the new External network. (If you are using In-Private, or Saved Profiles you do not need to log-out.)

2. Log in to the parent Engage network by going to engage.cloud.microsoft. (Ensure that you're using the same Global Administrator account that's responsible for the new Entra tenant.) You now access external networks setup.

3. In Engage, select the settings icon and go to the admin center.

4. In the **Setup and configuration** tab, select **External networks**.

5. Select **Setup external network** to redeem the association code. Select the **Redeem code** tab and add the association token and Entra tenant ID saved from the previous steps.

6. After the association, you will see an *External network has been successfully setup* message.

### Connect the legacy Engage network to the new Engage network

1. From the parent Engage network, switch to the legacy external network.

2. To open the external network settings, select its Settings icon and select **Network admin** from the menu.

3. To associate the legacy external network to the new network, select **External network upgrade** from the menu.

4. Using the same Tenant ID and tenant association token from the previous steps, enter the information in the appropriate fields and select **Redeem Token**.

After the token redemption, the legacy Engage external network is now associated with the new external network. The user is logged out at this point to allow logging in with Microsoft Entra as your identity provider. You're ready to begin data migration to the new network.

## Data Migration from a legacy network to the new external network

You'll need to export or configure your user accounts for use in the new deployment.

1. Log in to the legacy external network using admin privileges.

2. In the Admin experience, select **Export users** to export the set of user accounts in the legacy external network. Entra produces a .CSV file containing your user information.

3. As the Global Admin for the new Entra tenant, log-in to the Entra Portal. To bulk-add the users from the legacy external network, provide the exported users CSV file to bulk-invite them as guests in the new network.

>[!NOTE]
> For more information, see [Bulk invite B2B users - Microsoft Entra External ID | Microsoft Learn](./entra/external-id/tutorial-bulk-invite)

### Move the network data

With the legacy external network now associated with the new external network, you can start the data move/data alignment.

After logging in to the external network, after you execute the external network upgrade step, you see the **M365 Native Mode** option in admin settings. Select this tab and follow its instructions to complete the M365 Native Mode alignment.

## Launch the new external network

>[!IMPORTANT]
> Update the policies of the Entra tenant that hosts your new external network based on your security requirements, including the policies to identify, respond to, and recover from security threats.

After completing the data move to the new external network, administrators must take the following actions:

- Confirm that all Communities are configured and operating as they did in the legacy network;

- Notify users of the new network through a communication channel applicable to your organization.

>[!NOTE]
> When you re-add guest accounts to the new network, it offers a feature to notify users of the new URL/domain.

## FAQ

**What happens to my users from the legacy external network?**

You can export the list of existing users in your legacy external network in a CSV file from the Native Mode setup flow. You can also use the CSV file to bulk invite the users to your new external network via the Microsoft Entra portal.

**I use external networks for Consumer Identities, are these still supported in modern external networks?**

Yes. Engage continues to support consumer identities in both External and Canonical Engage networks.

**What is the process for members joining the migrated external network?**

The updated external network supports adding members by using the invitation flow.

Admins can also use Cross-Tenant Sync to move users directly into Entra, and those users have access to the new external network.
