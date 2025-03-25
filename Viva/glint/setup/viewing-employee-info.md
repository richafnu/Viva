---
title: Use Viva Glint's People page to view employee information
description: 
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 03/25/2025
---

# Use Viva Glint's People page to view employee information

To find and view information about a specific person, from the admin dashboard, select the **People** tile. 

Use one of the two following methods: 

- Begin to type the name of the employee in the search bar. When the name appears as a dropdown, select the name.   
- Scroll down the alphabetized list of names. With hundreds or thousands of employees, this method isn't as efficient! 

For each employee, the following information is visible: 

- **Employee Name**: Editable by admin by selecting the pencil symbol. 
- **Email**: Editable by admin by selecting the pencil symbol.
- **Manager Reports**
- **Team**

This example is a small snapshot of a fictious employee's People page:

:::image type="content" source="../../media/glint/setup/people-header-row.png" alt-text="Screenshot of fictious employee People page.":::

## Manage User Roles

View and manage what data and people a user has access to. This section is editable by selecting the **pencil symbol**. The **Customize User Role** dialog box opens. To add a User Role to a profile, select from the list that appears in the dialog box. Changes made override any previous role exclusions. Select **Save.**

:::image type="content" source="../../media/glint/setup/people-customize-role.png" alt-text="Screenshot of the Customize User Role dialog box in the People feature.":::

## View attributes

In the Attributes section, attributes show for this user as defined in your latest Employee Attribute File upload.

### Hierarchy attributes

- **Location hierarchy**
- **Manager hierarchy:** The organization’s highest-ranking employee (generally the CEO) is listed first. The hierarchy progresses downward, following the organizational chart flow, ending with the employee’s immediate manager. Not editable. 
- **Old Manager hierarchy**, if it exists

### Standard attributes

Your organization may not use all of these attributes and may also refer to the attributes using other terminology. Whichever attributes you sent to Glint show here. These are common examples of Standards attributes:
- **Manager email**
- **Employee ID**: Editable. [Learn how here](/../../viva/glint/setup/people-page).
- **Sub-Department**
- **Department**
- **Start Date**
- **Hire Date**
- **Level**
- **Tenures** 

## Manage and understand other access 

For employees with extended roles, these sections are visible:

### Admin Access


### Focus Area Access

### Survey Access


### Survey programs

- **Focus Area Access**: Defines which people's data this user sees in Focus Area reports. Editable by selecting the **pencil** symbol.  
- **Survey Acces**s: Defines which people's data this user can see in selected survey programs. Editable by selecting the **pencil** symbol.

>[!CAUTION]
> Viewing and exporting raw data are governed by Microsoft rules protecting employee confidentiality. Review the guidance on [raw data exports](https://go.microsoft.com/fwlink/?linkid=2239587) within our Security and Privacy documents.

## Use the View As function 

The **View As** functionality allows you to open your Glint program as if you were another employee. You can view another user’s dashboard based on their User Role and data access.

**To view as another person**: 

1. Locate the person you want to view as and open their page by hovering over and selecting their name. 

1. Select  **View As**. 

1. The dashboard indicates **You are seeing `<other person name>` Viva Glint experience.** 

To return to your own account, select  **Return to your account**. 

## Use the Actions function 

The Actions button dropdown menu allows you to send surveys, send user data, and delete users.

### Send Survey 

You can send a survey to one employee (manually) from the People page. Use the Actions button and then  **Send Survey**. 

>[!IMPORTANT]
>You'll need to send a survey manually when an employee wasn't part of the Distribution List for that survey during the initial send but should now receive the survey.
>
>A Distribution List is a snapshot in time, so any employee who becomes eligible for a survey after its initial send requires a manual invite. Add them to the Distribution List thereafter, and upload the new Employee Attribute File to Viva Glint.

- Enabled and live surveys are displayed. Select the survey to send.  

   > [!NOTE]
   >A survey won't appear if it's not enabled or live. Go back into the program to re-enable or change the date of the survey, noting that it takes a few minutes for a survey to become live.

- Select **Send**.

### Send User Data

Send a user's survey response and attributes directly to a user, without viewing data. [Learn more](https://go.microsoft.com/fwlink/?linkid=2230875).

### Delete User

Delete a user from Viva Glint. [Learn more](https://go.microsoft.com/fwlink/?linkid=2236554).

## Import your Employee Data File 

Use the **Import** button on the People page to import a *.csv* (UTF-8 or UTF-8 with BOM encoded) or an *xlsx* (single tab) file to update employee details.

Follow the on-screen guidance for uploading the file and then select  **Import File**. [Learn more](https://go.microsoft.com/fwlink/?linkid=2230742).

   > [!NOTE]
   >If you upload a user file during a live survey, employee information won't be altered for that survey. 

## Export an Active Employees report 

To make changes to an employee file, it's often easier to start with what's in the system first. Exporting from within the system, making changes, and then reimporting begins in the Export feature. 

Select **Export** and then follow the on-screen guidance.
