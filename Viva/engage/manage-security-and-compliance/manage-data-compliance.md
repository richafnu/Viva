---
title: "Manage Viva Engage data compliance"
f1.keywords:
- NOCSH
ms.author: donnabouldin
author: v-rgrace
manager: elizapo
ms.date: 12/19/2024
audience: Admin
ms.topic: how-to
ms.localizationpriority: medium
ms.service: viva-engage
ms.collection: essentials-compliance
search.appverid:
- MET150
- MOE150
- YAE150
ms.assetid: 8c4651fa-12c2-4ced-b4ea-2200c0a630ed
description: "Monitor your Viva Engage data with these features: keyword monitoring, security settings, data export, data retention, and analytics."
---

# Manage Viva Engage data compliance

As a Viva Engage admin, you can keep your users' Viva Engage posts appropriate and meet security and compliance requirements. You can set up alerts for content that matches keywords, set data retention policies, and if needed, view private content. You can also [export data from Viva Engage](../eac-as-manage-data.md).

<a name="MonitorKeywords"> </a> 

## Monitor keywords

Use keyword monitoring to detect sensitive or specific content for community and storyline conversations within Viva Engage.
  
 **Assign a verified admin to monitor, edit, and delete flagged posts**
  
1. In the Viva Engage admin center, go to **Content and security** > **Monitor Keywords**. In the **Recipient** field, enter an Entra ID-backed email address from the tenant to receive alerts on detected conversations.
    
2. Enter the words and phrases you want to monitor, each on their own line.
    
When a post in Viva Engage matches a keyword, the person listed in the recipient field receives an email. The subject of the email gives context on the monitored keyword along with the community/storyline storyline where it was detected in Engage. The body of the email also provides further context on the detected conversation.  
 
Improvements to the email template and user experience include:  

- **Public community or storyline conversations detected with keywords**: the email body contains the conversation, and any associated replies along with the name of the community/storyline.

- **Private community conversations detected with keywords**: the email provides a link to the conversation and the community where it was detected. Moderators can view the conversation by selecting the message link; those moderators have access to the community’s conversation only when they're a member.  

As part of our continued investment in security, we've added the following improvements to email notifications: 

- Viva Engage supports only Entra ID-backed email addresses within your tenant as email recipients. Consumer email addresses (such as Gmail) aren't supported. Unsupported email addresses receive a prompt to change to a compatible email address.

- The keyword alert system doesn't detect Private messages between individuals. These messages are confidential and must be discovered through appropriate compliance solutions, such as e-discovery, when necessary. 
    
   Use [regular expressions](/dotnet/standard/base-types/regular-expression-language-quick-reference) to match patterns.
    
    Here are some examples of regular expressions commonly used for monitoring.
    
|**Purpose**|**Pattern**|**Matches**|
|:-----|:-----|:-----|
|Word boundary |\bword\b |\btheme\b matches "theme" but not "themes" or "them" |
|Credit cards |\b(?:\d[ ‐]\*?){13,16}\b |1234 5678 90123  <br/> 1234 5678 9012 3456  <br/> 1234‐5678‐9012‐3456 |
|Social Security numbers |\b\d{3}[ -]\d{2}[ -]\d{4}\b |123 45 6789  <br/> 123‐45‐6789 |
Monitor group create|has created|Matthew has created the Easter Region Sales group.
  
<a name="DataRetention"> </a>
## Data retention

You can remove deleted data from the user's view. Engage preserves the deleted data for data export for the life of the tenant.

1. In the Viva Engage admin center, go to **Content and Security** > **Data Retention**.
1. Select **Archive** and save your changes.
<br> This setting applies to your entire network.

**To permanently remove already deleted data**, use the workflow for [general data protection regulation (GDPR)](gdpr-requests-in-viva-engage-enterprise.md) or the hard-delete API. Files uploaded through Engage and hosted in other Microsoft 365 resources (for example, SharePoint) are subject to the deletion policies of the hosting resource.

**To permanently delete retained data in Viva Engage storage**, [export the data](../eac-as-manage-data.md) to identify the data you need to delete permanently. Write a custom PowerShell script to loop through the candidates for deletion using the [REST API](/rest/api/yammer/rest-api-rate-limits).

**To permanently delete retained Viva Engage files saved in SharePoint**, you must use [data retention settings in Microsoft 365](/office365/securitycompliance/retention-policies).
    
<a name="ContentMode"> </a>
## Content mode

If you have a legal reason to view private messages, verified Engage admins can select to see them. For more information, see [Monitor private content in Viva Engage](monitor-private-content.md).
  
## See also

[Reduce visibility of a user's posts in Viva Engage](../work-with-external-users/mute-user-in-network.md)
