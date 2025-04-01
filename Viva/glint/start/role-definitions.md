---
title: Key roles for Viva Glint
description: Assigning roles for Viva Glint leadership is among the first tasks for the Microsoft 365 Global Admin. Using consistent terminology for all roles helps support your Viva Glint programs.
ms.author: JudithWeiner
author: JudyWeiner
manager: mbarry
audience: admin
f1.keywords: NOCSH
keywords: Microsoft 365 Global Administrator, Viva Glint Administrator, Viva Glint manager, Viva Glint end user, Viva Glint Tenant Administrator
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: concept-article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 04/01/2025
---

# Key roles for Viva Glint

Assigning roles for Viva Glint leadership is among the first tasks for the Microsoft 365 Global Administrator. Using consistent terminology for Viva Glint roles helps support your Viva Glint programs.




|Role  | Assigned by | Grants access to the Microsoft 365 admin enter to submit support requests  | Grants access to the Viva Glint app |
|:----------|:-----------|:------------|:------------|
| [Microsoft 365 Global Administrator](/entra/identity/role-based-access-control/permissions-reference#global-administrator)   |  | Yes | No  |
|[Viva Glint Tenant Administrator](/entra/identity/role-based-access-control/permissions-reference#viva-glint-tenant-administrator)     |  | Yes | No  |
|Viva Glint Administrator             |  | No  | Yes |
|Viva Glint manager                   |  | No  | Yes |
|Viva Glint end user                  |  | No  | No  |

## Microsoft 365 Global Administrator

- Provisions Viva Glint tenants
- Represents your organization, initiates, and controls Viva Glint product subscriptions and licenses
- Assigns Viva Glint Tenant Administrators

## Viva Glint Tenant Administrator

- Assigned by the Microsoft 365 Global Administrator to manage Viva Glint settings in the Microsoft 365 admin center
- Assigns Viva Glint Administrators
- Views message center information in the Microsoft 365 admin center
- Files Microsoft 365 and Azure support tickets
- Views service health information
- Views Usage Reports
- Can be assigned with the Viva Glint Administrator role to allow a user to manage settings in the Microsoft 365 admin center and in the Viva Glint app

## Viva Glint Administrator

- Assigned by the Viva Glint Tenant Administrator to have responsibility for admin tasks in the Viva Glint platform
- Can access all data
- Sets up programs and surveys, distribution lists, and reporting features
- Supports managers in all aspects of action taking
- Best practice is to assign no more than five Viva Glint Admins
- Can be assigned with the Viva Glint Tenant Administrator role to allow a user to manage settings in the Microsoft 365 admin center and in the Viva Glint app

## Viva Glint manager

- Organizational team leader who works directly with a Viva Glint Admin to assist with survey administration
- Is assigned reporting access and can develop action plans

## Viva Glint end user

- Survey takers within your organization
