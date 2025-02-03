---
title: Program setup in Program Summary
description: In Program Setup, define the basics of your program, such as its name and what languages are needed, along with confidentiality directives.
ms.author: JudithWeiner
author: JudyWeiner
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: confidentiality setup, basics setup, automatic survey question scrolling, survey comment expansion
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms: custom: CELA-approved
ms.date: 02/03/2025
---

# Program Setup in Program Summary

The **Program Setup** page is the first configuration page within **Program Summary**, where you define the basics of your program.

:::image type="content" source="../../media/glint/setup/program-setup-from-program-summary.png" alt-text="Screenshot that shows the Program Setup page for configuration within the Program Summary.":::

## Define the basics  

:::image type="content" source="../../media/glint/setup/program-setup-2.png" alt-text="Screenshot that The Basics section of Program Setup." lighbox="../../media/glint/setup/program-setup-2.png":::

Select **Edit** to configure or change setup in this section.

|Field|Description|Examples/Tips|
|-------|------------|-----------|
|**Program Name**|Used in survey and email communications, reporting, and is visible to survey respondants|Engagement, Manager Effectiveness, 30-day Onboarding|
|**Administrators**| This role can set up, manage, edit, and report on all surveys in the entire program|*Manage Programs* must be enabled for the name to appear in the search box.| 
|**Default Language**|Appears as set up in General Settings|
|**Additional Languages**| Populated with languages set up for your organization in General Settings.| Be sure survey items are available in all languages chosen. To remove languages, select the **X** next to the language name.|
| **Admin Notifications to** |These admins are notified of upcoming surveys and are determined in General Settings.|Each survey should have at least one admin in this role who is notified before the survey goes Live. Use the **Search** add names.|
|**Suggested Action Available** |Enables Users to create goals.|Toggle to enable or disable|
|**Eligible for Nudges** |Timely messages designed to help managers take action| Toggle to enable or disable. | 
|**Allow Survey Resubmission** |Allow survey takers to retake their surveys. All previous responses are deleted|  Toggle to enable or disable.|
|**Enable [Team Conversations](/../../viva/glint/reports/team-conversations-administrator-setup)**|Helps managers and survey takers feel like their feedback is heard and acted upon.|Managers receive a personalized summary presentation of survey results. Helps your managers share results, pick Focus Arteas, and identify next steps throught a guided interactive conversation.|
|**Auto-expand comments input**|With this enabled, a comment box shows after each survey item posed to a survey taker. Disabled, the survey automatically moves to the next item.|Disabled by default. Toggle to enable. This feature prompts more detailed and actionable insights by survey takers, increasing survey engagement.|
|**Enable Team Conversations Sharing**|Allows managers to share a read-only version of their feedback summary presentation before or after meetings with their team.| Enabled by default when Team Conversations is enabled. |
|**Enable Viva Pulse Integration** |Enabling this feature sends Glint data for every closed program cycle and future cycles.| See the Reporting page to specificy which roles have access to this integration.  

Select **Save Changes** or the **right-facing arrow symbol** to save and continue.

## Confidentiality

:::image type="content" source="../../media/glint/setup/program-setup-confidentiality-2.png" alt-text="Screenshot that shows the Confidentiality setup within Program Setup.":::

|Field|Description|Examples/Tips|
|-------|------------|-----------|
|**Confidential responses** | Promotes accurate feedback| Enabled to **Custom Confidential** by default|
|**Enable Export of Raw Survey Responses** | Enabling this functionality allows admins to export ungrouped, identifiable survey responses. Disabling this function permanently disallows access to or export of those responses, including the ability to transfer the data to a third party.| [Learn more about raw survey access](/../../viva/glint/setup/employee-raw-data-export)|
|**Company Message to Survey Participants** |Allows organizations to add more details tailored to their organization, aiming to ensure that individuals participating in surveys are well informed. Clients may wish to append information like specifying the organizational roles with access to identifiable responses or designating appropriate points of contact within the organization for inquiries  or concerns related to the survey. You can also add guidelines on the proper utilization of the survey and direct respondents towards their company-specific resources for more details. This text gets added at the beginning of the survey under the title "Message from [<Client_Name>]," directly following Glint's confidentiality statement.|<li>Translations for the Company Message must be done manually.</li><li>The character limit for the Company Message to Survey Participants is 1,024</li><li>**Survey level custom messaging takes precedence.** Custom messaging set up in General Settings but edited at the survey level, overrides the initial messaging.</li><li>Employee Lifecycle surveys often target only a few individuals. For this reason, reducing your confidentiality threshold helps protect their privacy.</li>|

### Next Step
> [!div class="nextstepaction"]
> [Distribution setup in Program Summary](../../glint/setup/distribution-program-summary.md)

