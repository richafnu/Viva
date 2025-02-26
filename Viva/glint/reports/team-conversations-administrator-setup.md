---
title: Set up Viva Glint Team Conversations
description: Microsoft Viva Glint Administrators can set up Team Conversations for managers. Team Conversations allow managers to meet with their teams and have meaningful discussions on their team's results and choose Focus Areas.
ms.author: SarahBerg
author: SarahAnneBerg
manager: elizapo
audience: admin
f1.keywords: NOCSH
keywords: set up team conversations, team conversations, conversation sharing, take action
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article![image](https://github.com/user-attachments/assets/2e559fe8-ea01-475b-bda4-5d40f0ffba25)

ms.service: viva-glint
ms.localizationpriority: high
ms.date: 02/26/2025
---

# Set up Viva Glint Team Conversations

Microsoft Viva Glint Administrators can set up Team Conversations for managers. Team Conversations allow managers to meet with their teams and have meaningful discussions on their team's results and choose Focus Areas. [Learn more](take-action-team-conversations.md).

## Setting up Team Conversations in Program Summary

To enabled Team Conversations as a Viva Glint Admin:

1. Select **Configuration** and select **Survey Programs** from the Surveys section.
1. Select a survey program that should have Team Conversations to be enabled.

> [!NOTE]
> Team Conversations are only available for Recurring surveys.

### Program Setup page

There are two enablement options to consider on this page: 

- Enable Team Conversations – Toggle to **YES**. 
- Team Conversations sharing - managers can share their Team Conversations Presentation Kit with users who have **View My Surveys** permissions. 


>[!TIP]
>Team Conversations are only generated for managers with survey results that meet confidentiality threshold requirements.  

   > [!NOTE]
   >Ensure user roles have the permissions of "View My Surveys" and "View Dashboard and Reports.

### Schedule page 

Indicate how many days the Team Conversations Window should remain open for. This drives the reminder schedule for Team Conversations. Even after the Team Conversation window closes users can still access their Team Conversation via My Surveys. Once set, the program indicates the conversation start and end date scheduled and how many days remain. 

>[!TIP]
>The default response window is 28 days, although the window can be set for up to 180 days. Response window refers to the number of days the survey is open to responders and is not specific to Team Conversations.  

### Reporting page 

There are two items to configure on the Reporting page for each User Role that should have access to Team Conversations. Select the down-facing arrow next to the User Role in the **Program Roles** section and then: 

1. Enable Team Conversations for that role by toggling Team Conversations button to **ON**. 
1. Select **Team Summary** as the default dashboard from the dropdown menu for that role. 

### Communications page 

Default Team Conversations email presets:  

- Conversation Start Notification: Seven days after survey results are released 
- Reminder 1: If conversation isn't done, send seven days before due date 
- Reminder 2: If conversation isn't done, send three days before due date 
- Conversation Summary Notification 
- Conversation Overdue Reminder 1: Sent three days after conversation due date

#### Rules for when to edit communications 

Emails send if these circumstances are met:
 
- Team Conversations is ON 
- The cycle is closed 
- A User Role moved to live access at least seven days ago
- The survey close date is within the last 45 days

Emails won't send under these circumstances:
 
- Team Conversations is OFF
- The cycle is open 
- A User Role moved to live access fewer than seven days ago
- The survey close date is more than 45 days in the past

If you enable Team Conversations for a User Role after the conversation start date, emails immediately send once Team Conversations is switched to **ON**. 

   > [!NOTE]
   > Nudges can coexist with Team Conversations but don't send when the Team Conversation window is open.

> [!TIP]
> When Team Conversations are enabled, don't enable Nudges for that User Role.


| **Are Team Conversations on?** | **Is the cycle Live** |**Have 7 days passed since live access?**|**Can emails be edited?**
|---|---|---|---|
| Yes | Yes|N/A|Yes|
| No | Yes|N/A|Yes|
| Yes | No|No|Yes |
| Yes | No|Yes|No, emails already sent|
| No| No|No|Yes, Team Conversations can be turned on and emails can be edited|
| No| No|Yes|No, but emails send if Teams Conversations is switched to ON|  

## Edit communications 

Edit and preview by selecting **Edit**. Edits made to notifications are only for the current program. Switching from Edit to **Preview** (and languages) automatically saves changes. 

### Conversation Start Notification 

- Can be enabled or disabled 
- Can be edited for the number of days after survey results are released 
- Our default and Best Practice are seven days after survey results are released 
- Can be sent in any languages enabled for this survey 
- Can be previewed 

### Conversation Reminders 

Reminders schedule when the User Role group gets Live access. If admins grant live access to roles at different times, their Team Conversations reminders are on different schedules. The Conversation Start email can be turned on or off until the day it's sent but not after the start of the Team Conversations. An existing Reminder email (before the Conversation End date) can be deleted or modified until the day before the last group of users is scheduled to receive it. 

Reminders:

- Can be sent any number of days before Conversation End date. Our default and Best Practice are to send both seven and three days before Conversation End date.  
- More reminders can be added by selecting **+ Conversation Reminder**  
- Can be sent in any language enabled for the survey 
- Can be previewed in the platform

### Conversation Summary Notification

This is an optional email that managers can send to their team before and/or after a conversation when Team Conversations sharing is enabled in Program Setup.

- Can only be enabled or disabled
- Can be sent in any language enabled for the survey
- Can be previewed in the platform

:::image type="content" source="../../media/glint/setup/conversation-summary.png" alt-text="Screenshot of the Conversation Summary email that managers can send before and/or after a conversation with their team.":::

### Conversation Overdue Reminder

The overdue reminder:

- Can be edited for a specified number of days after Conversation End date. The default and Viva Glint Best Practice is three days. 
- Can be sent in any language enabled for this survey 
- Can be previewed 

## Customize Team Conversations email content

[Learn more about customizing Team Conversations email content](team-conversations-content-cusomization.md).

### Coaching page 

When Team Conversations are enabled, admins can set up the Team Conversations presentation kit for your manager to share with their teams. See [Coaching Setup for Admins](https://www.microsoft.com). 

 
