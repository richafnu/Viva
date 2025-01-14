---
title: "Manage Viva Engage security settings"
f1.keywords:
- NOCSH
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 01/14/2025
audience: Admin
ms.topic: article
ms.service: viva-engage
ms.localizationpriority: medium
ms.custom: Adm_Yammer
ms.collection: essentials-security
search.appverid: 
- MOE150
- MET150
ms.assetid: a5f747cc-1306-450e-b8e2-23f465756f1e
description: "Control how people access Viva Engage, set password policies, control who can create external networks, and enforce Microsoft 365 identity."
---

# Manage Viva Engage security settings

Viva Engage security settings control how people access Viva Engage. You can set password policies, control external network access and information, and enforce Microsoft 365 identity.
  
## Allow access to Viva Engage only from the office or VPN (logical firewalls)

Admins can define network prefixes as trusted IP ranges. You can use IPv4 or IPv6 ranges. You can also allow or disallow remote clients from outside those authorized ranges from being able to connect.

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **IP Range** section, specify the IP ranges of your corporate network or other trusted networks.

3. Select whether to allow sign-in to users outside the specified ranges.

    Typically, users that use mobile clients are outside of any authorized IP ranges unless the mobile client uses Wi-Fi on a trusted network. To allow access from mobile clients, select **Allow login**. Doing so restricts web sign-ins outside of your trusted IP range, but allows mobile client logins from outside the IP range. If you select **Deny login**, users outside of the trusted IP range can't access Viva Engage through clients.

## Set password policies

Admins can define password management policies to control the length and complexity of required passwords, and frequency of password changes.

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **Password Policies** section, specify the password length and complexity requirements, and when passwords need to be changed.

    If you change any password settings at a later time and select **Save**, users whose passwords don't meet these requirements are prompted to change their passwords upon their next sign-in. If you select **Force All Users to Change their Passwords Immediately** all users must change their passwords the next time they sign in, regardless of any password requirement changes.

    > [!NOTE]
    > External networks can't configure password policies. This practice prevents external users from facing multiple password strength requirement policies when they want to sign in. Users must comply with the password strength policies of their home network.
  
## Configure security settings for all external networks

You can define Viva Engage network settings that govern all external networks. Clients in those external networks will all use the resulting policies.

1. In Microsoft 365, go to **Admin** \> **Viva Engage** \ **External Networks**. Or, in Viva Engage, select your home network settings icon, and go to **Network Admin** \> **External Networks**.

2. Select **External Networks**.
  
3. Select ways to limit access by all external networks:

   - **Require admin approval for users to join other companies' external networks:** When you select this box, users must request approval before they join external networks created by other organizations.

   - **Disable Related External Networks directory:** The Related Networks directory is a list of external networks to which one or more of your users belong. Selecting this box removes the directory from the External Network page.

   - **Disable our External Networks directory:** The Our External Networks directory lists all external networks attached to your Viva Engage network. Select if you want to prevent users from viewing (and requesting to join) external networks.
  
## Prevent intellectual property from being shared with external participants and on external networks

You can take steps to prevent Microsoft intellectual property data leakage from your Viva Engage network.

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **External Messaging** section, select the option that makes sense for your organization.

## Enforce Microsoft 365 (formerly Office 365) identity in Viva Engage

To streamline user management, you can maintain a single identity for all Microsoft 365 users by enforcing Microsoft 365 identity in Viva Engage. It's a quick way to support single sign-on (SSO) capabilities for your Viva Engage network users.

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. In the **Office 365 Identity Enforcement** section, select **Enforce Office 365 identity in Viva Engage**.

    For information about this setting, see [Enforce Microsoft 365 identity for Viva Engage users](../configure-your-viva-engage-network/enforce-office-365-identity.md)

## Learn the status of Microsoft 365 Connected Groups

You can check the curent status of your Viva Engage network's Microsoft 365 groups. Those groups originate from Microsoft 365 and use Microsoft 365 as the cross-application membership service.

1. In the Viva Engage admin center, go to **Content and Security** \> **Security Settings**.

2. Look in the **Office 365 or Microsoft 365 Connected Viva Engage Groups** section to see the status for your connected groups.
