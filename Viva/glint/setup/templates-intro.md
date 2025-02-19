---
title: Viva Glint survey templates introduction and terminology
description: The Viva Glint People Success database contains survey items - questions and statements - that each measure a distinct employee experience. Read this introduction to Viva Glint survey templates and learn the terminology associated with them.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva glint, recurring surveys, engagement, Referents, tags, 
ms.collection: 
 - m365initiative-viva
 - selfserve
 - essentials-overview
 - essentials-get-started
 - essentials-navigation
search-appverid: MET150
ms.topic: overview
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 2/19/2025
---

# Viva Glint survey templates introduction and terminology

The Microsoft Viva Glint People Success database contains survey items - questions and statements - that each measure a distinct employee experience. The database is found in the Question Library on your admin dashboard. 

:::image type="content" source="../../media/glint/setup/question-library.png" alt-text="Screenshot of the Question Library on an admin dashboard.":::

## Understand the Viva Glint Question Library 

Question Library items are available to help construct powerful and predictive surveys. Viva Glint standardized template surveys (Engagement, Onboarding, Culture, Diversity & Inclusion, etc.) are developed using items that are the best predictors of engagement. The Microsoft Viva People Science Research team tests and validates all survey items. 

Each item has a unique **Item Name** and **Question ID** to distinguish it in the Viva Glint database. 

### Add an Question Library item to your template

You may choose to use a template "as is" or you may choose, for example, to delete one item and find another item that better represents the key driver you want data for.

>[!IMPORTANT]
> If an item appears in more than one type of survey, it shows more than once in the Question Library. This scenario occurs because the identically phrased item is used for templates with different frames of reference and context. If you'd like to add an item to a template, be sure to choose the correct item!

Let's look at an example where you want to replace an existing template item with an item about career goals:

:::image type="content" source="../../media/glint/setup/question-library-dups.png" alt-text="Screenshot of two identically phrased items in the Question Library.":::

1. In the search box, key in **Career Goals.** Many different items come up. Decide which one works for you. Here we've chosen "My career goals can be met at <Company Name>.
2. Notice that two of the identically phrased statements exist.  You need to investigate why the item exists twice. From looking at the column headers, we know that:
   -  In the **Name and ID** column, they are both called **Career Goals** but they have a different Question ID.
   -  In the **Question** column, the text is identical.
   -  In the **Used In** column, you see that you haven't used the item in any survey
   -  In the **Tags** column, you see:
      - The item isn't customized, as the status reads Viva Glint and not Custom)
      - Both items are rating questions
      - Both items are both linked to the 2021 Global benchnmark.
   <br>
   There must be a difference. What is it? :::image type="icon" source="/office/media/icons/get-started-blue.png"::: 
3. Hover over the first entry and select it to open the slider panel.
4. Hover over the second item and look for these key settings to discover differences:
   - Rating Scale
   - Program Type

 :::image type="content" source="../../media/glint/setup/question-library-discover-difference.png" alt-text="Screenshot of a slider panel in the Question Library.":::

5. You can see that:
   - The first item is intended for a survey using a 7-point rating scale
   - The second item is intended for a survey using a 5-point rating scale
   - Both items are intended for Engagement surveys
6. Choose the item with the rating scale that matches your survey.


## Survey item terms

Items can be filtered to help you find exactly the item to support your survey driver. These terms are helpful to understand:

|Terms| Definition and Need-to-Knows|
|-------|------|
|**Referent**| The group or population (Manager, Coworkers, Company, etc.) a respondent should think about when rating an item|
|**Program**|The Viva Glint survey this item is used in. For example: Engagement, Exit, Onboarding. All items listed by program are loaded into the Viva Glint platform, our survey templates, and the Question Library.|
|**Question Type**|<ul><li>**Rating items** use a 5- or 7-point scale.</li><li>**Open ended items** are items that require text responses. </li><li> **Options** are items that require a selection of single- or multiple-choice responses.</ul>|
|**Action Plan Template**| The action plan content aligned to this item. If shown as "default," the item is using the generic template. If empty, this item has no Action Plan content aligned to it.|
|**Option Text**|The list of response choices for Options items|
|**Tags**|Unique identifiers belonging to a Question Library item|
|**# of Alternate Forms**|How many differently worded item choices are available for the "same" item. No number listed indicates that no alternate items are available. There are three types of alternate items: <ul><li> **Substitute items:** have slightly different wording but are an equal substitute for the originally recommended items. These alternatively worded items are still comparable to the original item benchmark.</li><li>**Related items:** similar to the original recommended items, but can be interpreted differently by survey takers. These items can't be compared to the original item benchmark. </li><li> **Referent items:** ask employees to think about specific referents (responsible level of management) when measuring this experience. These items can't be compared to benchmarks.</ul>|

## Referent definitions

|Referent|Description|
|--------|--------|
|**Team**|These items may read "my team" or "on my team." The items refer to a group of people that the respondent is a member of and who all work either in the same department or for the same manager.|
|**Teams**|These items may read "teams" or "work team." The items refer more generally to groups of people across the company, not necessarily the team the respondent is on.|
|**Coworkers**|These items may read "Coworkers" or "people" or "employees." The items refer to other people, in general not necessarily on the same team as the respondent.|
|**Manager**|These items may read "my manager" or "my Supervisor." The item refers to the person the respondent reports to directly and who most likely has the most influence over the respondent's job and provides the respondent feedback and employment reviews.|
|**Leadership**| These items may read "executive team" or "top leaders" or "leadership team." The items generally refer to the executive team - the CEO and their direct reports.<ul><li>"Leaders" or "leadership" can also be a general reference to leaders at various levels in the company.</li><li>"Leaders in my organization" refers to the management chain above the responder within their larger department or unit.</ul>|
|**Company**| These items may also be stated as "where I work" or "at this company" or "here." The items refer to an experience of the entire company overall.|
|**Industry specific job referent**| Some companies may use specific job titles or common abbreviations. Registered Nurse (RN) is an example.|

With all of the above referents, you can customize the item by inserting the actual name of who is to be rated. 
> For example:
> Viva Glint item: "I get the support I need from <leadership and their directs."
> Customized item: "I get the support I need from Fred Smith."
> The item now shows in your Question Library tagged as both a Viva Glint item and a customized item.

### More about referents

In the Question Library database, certain items contain a *Referent* which directs the survey taker to think specifically about *who* they're rating. About half of the Viva Glint items have referents. If the Referent column status is **None**, the item describes an experience with no clear referent. 

> Example **with** a referent: “I feel cared about as a person on my team.” 
> Example **without** a referent: “At work, I feel cared about as a person.”

#### Not all survey items have referents

Unless a theme or topic is predominantly experienced through a referent, Viva Glint recommends using items that focus on the experience itself. This practice allows for the fact that many experiences have multiple influences. It's important to include items without referents because:
- It gives Viva Glint the ability to compare how the customer scored on the item to our external benchmarks.
- It ensures the item is relevant to employees across the customer organization. This relevancy is important when using the comparison scores to the Overall Company. Comparisons to benchmarks or company norms are essential to interpreting results. They're an important indicator in determining whether your scores are strong or need improvement.
- Narrative Intelligence (NLP) is built into the platform to pull meaning from comment data. This ability connects the dots between what employees think about broader topics and how they feel about them. 

## More information

[Validated items in the Viva Glint Question Library](/../../viva/glint/setup/question-library)

[Link customized questions to Viva Glint benchmarks](/../../viva/glint/setup/custom-question-benchmark)

[Change survey item IDs](/../../viva/glint/setup/change-item-id)







