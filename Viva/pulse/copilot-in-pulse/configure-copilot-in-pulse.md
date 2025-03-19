---
title: "Set up Microsoft 365 Copilot in Viva Pulse"
f1.keywords:
- NOCSH
ms.author: hasrivas
author: hasrivas
manager: alisaliddle
ms.date: 03/19/2025
audience: Admin
ms.topic: install-set-up-deploy
ms.service: viva-pulse
ms.collection: 
- viva-copilot
ms.localizationpriority: medium
search.appverid:
- MET150
ms.assetid: 
description: "Learn how to configure and incorporate Microsoft 365 Copilot in Viva Pulse within your organization."
---

# Set up Microsoft 365 Copilot in Viva Pulse

Microsoft 365 Copilot in Viva Engage is your everyday AI partner, empowering you to communicate in ways that create value for you and your organization. Copilot gives users access to Large Language Model (LLM) technology with [Microsoft Responsible AI protections](https://www.microsoft.com/en-us/ai/responsible-ai). LLM is a type of AI that can process and produce natural language text. Copilot helps users get the most out of Viva Engage by collaborating on written communications and suggesting where to post.

## Licensing requirements

By default, Copilot is enabled for all users who are assigned a premium Viva Engage license (purchased as part of _Microsoft Viva Suite_ or _Microsoft Viva Employee Communications and Communities_).

For details on Microsoft Viva plans and pricing, visit the [Employee Experience Platform Plans and Pricing page](https://www.microsoft.com/microsoft-viva/pricing).

|**Process commands to Copilot**|User interactions with Copilot through chat collaboration are currently processed, but not stored, with services aligned to Data center regional elections (US/EU Region).|

## Control access to Copilot and AI Summarization services

Access to Copilot and AI Summarization is managed separately through the [Viva feature access management platform](/viva/feature-access-management). Feature access management allows admins to create three types of access policies (tenant, users, and groups) for each feature through PowerShell commandlets. Policies provide a flexible and scalable approach to deployment.

Policy settings apply anytime a user signs in, allowing the user access to all enabled features. Because you can set multiple access policies--targeting the tenant, groups, and individual users--a user can be impacted by more than one policy. Individual user and group level policies always take priority over a tenant-level policy. For instructions, see [Control access to features in Viva](/viva/feature-access-management).

Learn more about [AI Summarization](/viva/engage/engage-ai-summarization) and how it works with other Viva Engage features.

#### Copilot and AI Summarization enablement states

Copilot and AI Summarization can be turned on or off. Changes to Copilot may require 48 hours to take effect. Changes to AI Summarization generally take effect within 24 hours.

| Pulse feature | State | Description |
|:-------------|:------------------:|:----------------------|
|**AI Summarization** |**Enabled**| This state enables background processing for Engage threads within the tenant.|
| |**Disabled**|If you disable AI Summarization, it stops processing the users' Engage threads. If you disable AI Summarization for the tenant and provide no enablement policies for user or group access, all historic background processing data is deleted retroactively. To avoid deletion of summarization data for all users in the tenant, accompany this setting change with a policy that enables the feature for at least each group.|

**Example**

If an admin needs to  disable Copilot only for users in Germany, they can accomplish that task with the following steps:

1. Create a group access policy in feature access management using PowerShell cmdlets.
1. Assign the Microsoft 365 group that contains all Germany users to the group policy.  
1. Set the group policy to OFF (disabled).

    As a result, all remaining users in the organizations (except Germany) can now use Copilot in Viva Engage.

**Important considerations for feature access management**

- There can be a maximum of one tenant policy per Viva Engage feature. In other words, you can set a single tenant policy for Copilot and a single tenant policy for Summarization.

- Creating a disabled (OFF) tenant policy for Summarization deletes all history data within the tenant.

    To avoid deletion of Summarization data for all users within the tenant, admins should immediately accompany a feature _disable_ (OFF) tenant policy with at least one feature _enable_ (ON) group policy.

## Access Copilot in Viva Engage

Users can access Copilot anywhere they write posts in Engage: the home feed, storyline, and on community and campaign pages.

:::image type="content" source="/viva/media/engage/admin/copilot-engage-home-start.png" alt-text="Screenshot shows the Open Copilot link on the Viva Engage Home page.":::

On the home page, Copilot generates proactive, personalized suggestions about posts the user might want to create.





