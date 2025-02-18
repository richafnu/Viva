---
title: FAQs for deleting User data
description: 
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

**Q: Following the LinkedIn Glint to Viva Glint migration, what user records are immediately removed?** 
A: No user records will be immediately removed following the completion of the migration.

What happens to existing INACTIVE user records in LinkedIn Glint after the Viva Glint migration? If a user record was updated to INACTIVE in LinkedIn Glint and already deleted from the client's Entra prior to the Viva Glint migration, the user record will remain INACTIVE and unchanged in Viva Glint. 

When will user records be deleted from Viva Glint? When Glint receives the delete signal from a Data Subject Request (DSR) or Microsoft Entra ID for a user, they're not immediately deleted. A user's employee record is in a soft-deleted state for 30 days. During this period, the employee record may be modified from its soft-deleted state and updated to the status provided in the HRIS file per the client's User Data control setting at Disregard Employee IDs of previously deleted employees. After the 30-day period, all data related to the employee is permanently deleted in alignment with the client's User Data control settings at Delete survey data for deleted users.

What does “all data related to the requester” mean? This refers to the user's first name, last name, employee ID, email address, and personal email address (if used) associated with the survey responses and reporting. What is the impact of selecting "Erase all data related to the requester, excluding attributes and survey responses"? This option corresponds to User Data control (General Settings) "Delete survey data for deleted users" = Off. This setting would delete the user's first name, last name, employee ID, email address and personal email (if used) associated with the survey responses and reporting. The user's other attributes and survey responses would be retained. If the deleted user is a manager, this would impact the manager hierarchy reporting as the manager's name will be listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for other attributes would not be impacted.

What is the impact of setting "Delete survey data for deleted users" as "Off" in User Data control (General Settings)? This setting would delete the user's first name, last name, employee ID, email address and personal email (if used) associated with the survey responses and reporting. The user's other attributes and survey responses would be retained. If the deleted user is a manager, this would impact the manager hierarchy reporting as the manager's name will be listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for other attributes would not be impacted.
What is the impact of selecting "Erase all data related to the requester, including survey responses"? This option corresponds to User Data control (General Settings) "Delete survey data for deleted users" = On. This setting would delete the user's first name, last name, employee ID, email address, personal email (if used), all other attributes, all survey responses and comments from all reporting. If the deleted user is a manager, this would impact the manager hierarchy reporting as the manager's name will be listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for all associated attributes would be impacted including response rates.
What is the impact of setting "Delete survey data for deleted users" as "On" in User Data control (General Settings)? This setting would delete the user's first name, last name, employee ID, email address, personal email (if used), all other attributes, all survey responses and comments from all reporting. If the deleted user is a manager, this would impact the manager hierarchy reporting as the manager's name will be listed as "Deleted User" and "Deleted User's Team" for any associated cycles. The reporting for all associated attributes would be impacted including response rates.
What is the impact of setting "Disregard Employee IDs of previously deleted employees" as "Off" in User Data control (General Settings)? 
What is the impact of setting "Disregard Employee IDs of previously deleted employees" as "On" in User Data control (General Settings)? 
What does the statement “Users deleted from Entra are automatically deleted from Viva Glint” mean in the Technical Migration Checklist Pre-Migration Step 16?  When Glint receives the delete signal from Microsoft Entra ID for a user, they're not immediately deleted. Users deleted from Entra would be updated to the deleted soft-state for 30 days in Glint after the delete signal is received. A user's employee record is in a soft-deleted state for 30 days. During this period, the employee record may be modified from its soft-deleted state and updated to the status provided in the HRIS file per the client's User Data control setting at Disregard Employee IDs of previously deleted employees. After the 30-day period, all data related to the employee is permanently deleted in alignment with the client's User Data control settings at Delete survey data for deleted users.
What happens when an employee is terminated? While the actual steps will vary by client, an employee's termination is typically updated in the client's HRIS system which triggers notifications to other service systems (i.e. Entra and Glint). After the user is disabled in the client's HRIS, the user's record may be removed or updated to INACTIVE in the file loaded into Glint. Similarly, Entra may be updated to reflect the user's termination. Glint receives the delete signal from Entra 30 days later, the terminated user's employee record goes into a soft-deleted state for 30 days. During this period, the employee record may be modified per the client's User Data control setting at Disregard Employee IDs of previously deleted employees. After the 30-day period, all data related to the employee is permanently deleted in alignment with the client's User Data control settings at Delete survey data for deleted users. 
A user must be ACTIVE in both Viva Glint and Entra in order to access Viva Glint. *Exception: personalized survey links and attribute-based login for survey takers
example scenario when both Entra and Glint receive an update regarding the terminated user on the same day:
Day 1 Entra - the user's record begins 30-day soft delete
Day 1 Glint - the user's record becomes INACTIVE
Day 31 Entra - the user's record is permanently deleted, delete signal goes out to applications
Day 31 Glint - recognizes delete signal from Entra, begins 30-day soft delete
Day 61 Glint - user's record is permanently deleted
example scenario when Glint receive an update regarding the terminated user before Entra does:
Day 1 Glint - the user's record becomes INACTIVE
Day 10 Entra - the user's record begins 30-day soft delete
Day 41 Entra - the user's record is permanently deleted, delete signal goes out to applications
Day 41 Glint - recognizes delete signal from Entra, begins 30-day soft delete
Day 71 Glint - user's record is permanently deleted
example scenario when Entra receive an update regarding the terminated user before Glint does:
Day 1 Entra - the user's record begins 30-day soft delete
Day 10 Glint - the user's record becomes INACTIVE
Day 31 Entra - the user's record is permanently deleted, delete signal goes out to applications
Day 31 Glint - recognizes delete signal from Entra, begins 30-day soft delete
Day 61 Glint - user's record is permanently deleted

