---
title: FAQs for deleting User data
description: In order to comply with a General Data Protection Regulation (GDPR) data subject request, a Microsoft Viva Glint administrator can delete User data from the platform.
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: 
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.custom: CELA-approved
ms.date: 02/18/2025
---

# FAQs for deleting User data

**Q: Following the LinkedIn Glint to Viva Glint migration, what User records are immediately removed?** 

**A:** No User records are immediately removed following the completion of the migration.

<br>**Q: What happens to existing INACTIVE User records in LinkedIn Glint after the Viva Glint migration?**

**A:**  If a User record was updated to INACTIVE in LinkedIn Glint and deleted from the client's Entra prior to the Viva Glint migration, the User record remains INACTIVE and unchanged in Viva Glint. 

<br>**Q: When are User records deleted from Viva Glint?** 

**A:**  When Viva Glint receives the delete signal from a Data Subject Request (DSR) or Microsoft Entra ID for a user, they're not immediately deleted. A User's employee record is in a soft-deleted state for 30 days. During this period, the employee record may be modified from its soft-deleted state and updated to the status provided in the HRIS file per the client's User Data control setting at Disregard Employee IDs of previously deleted employees. After the 30-day period, all data related to the employee is permanently deleted in alignment with the client's User Data control settings at Delete survey data for deleted Users.

<br>**Q: What does “all data related to the requester” mean?** 

**A:** This refers to the User's first name, last name, employee ID, email address, and personal email address (if used) associated with the survey responses and reporting. 

<br>**Q: What is the impact of selecting "Erase all data related to the requester, excluding attributes and survey responses"?** 

**A:**  This option corresponds to User Data control in General Settings. "Delete survey data for deleted users" = Off. This setting deletes the user's first name, last name, employee ID, email address and personal email (if used) associated with the survey responses and reporting. The User's other attributes and survey responses are retained. If the deleted user is a manager, this change impacts the manager hierarchy reporting as the manager's name is listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for other attributes **isn't impacted.**

<br>**Q: What is the impact of setting "Delete survey data for deleted users" as "Off" in User Data control (General Settings)?** 

**A:** This setting deletes the User's first name, last name, employee ID, email address and personal email (if used) associated with the survey responses and reporting. The User's other attributes and survey responses are retained. If the deleted User is a manager, this change impacts the manager hierarchy reporting as the manager's name is listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for other attributes **isn't impacted.**

<br>**Q: What is the impact of selecting "Erase all data related to the requester, including survey responses"?**

**A:**  This option corresponds to User Data control in General Settings. "Delete survey data for deleted users" = On. This setting deletes the User's first name, last name, employee ID, email address, personal email (if used), all other attributes, all survey responses and comments from all reporting. If the deleted User is a manager, this change impacts the manager hierarchy reporting as the manager's name is listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for all associated attributes **is impacted**, including response rates.

<br>**Q: What is the impact of setting "Delete survey data for deleted users" as "On" in User Data control (General Settings)?** 

**A:**  This setting deletes the User's first name, last name, employee ID, email address, personal email (if used), all other attributes, all survey responses and comments from all reporting. If the deleted User is a manager, this would impact the manager hierarchy reporting as the manager's name will be listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for all associated attributes would be impacted including response rates.

<br>**Q: What is the impact of setting "Disregard Employee IDs of previously deleted employees" as "Off" in User Data control (General Settings)?**

**A:**

<br>**Q: What is the impact of setting "Disregard Employee IDs of previously deleted employees" as "On" in User Data control (General Settings)?** 

**A:**

<br>**Q: What does the statement “Users deleted from Entra are automatically deleted from Viva Glint” mean in the Technical Migration Checklist Pre-Migration, Step 16?**  

**A:** When Viva Glint receives the delete signal from Microsoft Entra ID for a user, they're not immediately deleted. Users deleted from Entra are updated to the deleted soft-state for 30 days in Viva Glint after the delete signal is received. A User's employee record is in a soft-deleted state for 30 days. During this period, the employee record may be modified from its soft-deleted state and updated to the status provided in the HRIS file per the client's User Data control setting at Disregard Employee IDs of previously deleted employees. After the 30-day period, all data related to the employee is permanently deleted in alignment with the client's User Data control settings at Delete survey data for deleted Users.

<br>**Q: What happens when an employee is terminated?**

**A:** While the actual steps vary by client, an employee's termination is typically updated in the client's HRIS system, which triggers notifications to other service systems (i.e. Entra and Viva Glint). After the User is disabled in the client's HRIS, the User's record may be removed or updated to INACTIVE in the file loaded into Viva Glint. Similarly, Entra may be updated to reflect the User's termination. Viva Glint receives the delete signal from Entra 30 days later and the terminated user's employee record goes into a soft-deleted state for 30 days. During this period, the employee record may be modified per the client's User Data control setting at Disregard Employee IDs of previously deleted employees. After the 30-day period, all data related to the employee is permanently deleted in alignment with the client's User Data control settings at Delete survey data for deleted Users. 

1. A user must be ACTIVE in both Viva Glint and Entra in order to access Viva Glint. *Exception: personalized survey links and attribute-based login for survey takers.
   
1. Example scenario when both Entra and Viva Glint receive an update regarding the terminated user on the same day:
   1. Day 1 Entra - the user's record begins 30-day soft delete
   1. Day 1 Glint - the user's record becomes INACTIVE
   1. Day 31 Entra - the user's record is permanently deleted, delete signal goes out to applications
   1. Day 31 Glint - recognizes delete signal from Entra, begins 30-day soft delete
   1. Day 61 Glint - user's record is permanently deleted
   
1. Example scenario when Glint receive an update regarding the terminated user before Entra does:
   1. Day 1 Glint - the user's record becomes INACTIVE
   1. Day 10 Entra - the user's record begins 30-day soft delete
   1. Day 41 Entra - the user's record is permanently deleted, delete signal goes out to applications
   1. Day 41 Glint - recognizes delete signal from Entra, begins 30-day soft delete
   1. Day 71 Glint - user's record is permanently deleted
      
1. Example scenario when Entra receive an update regarding the terminated user before Glint does:
   1. Day 1 Entra - the user's record begins 30-day soft delete
   1. Day 10 Glint - the user's record becomes INACTIVE
   1. Day 31 Entra - the user's record is permanently deleted, delete signal goes out to applications
   1. Day 31 Glint - recognizes delete signal from Entra, begins 30-day soft delete
   1. Day 61 Glint - user's record is permanently deleted

