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

The Viva Glint People Success Taxonomy database contains survey items - questions and statements - that each measure a distinct employee experience. The items are available to help customers construct powerful and predictive surveys. Viva Glint standardized template surveys (Engagement, Onboarding, Culture, Diversity & Inclusion, etc.) are constructed using items that are the best predictors of engagement. The Microsoft Viva People Science Research team tests and validates all survey items. 

Each item has a unique Item Name and Question Universally Unique Identifier (UUID) to distinguish it in the Viva Glint platform. Because an item may appear in more than one type of survey (for example, Engagement and Exit), it shows more than once in the Question Library. It shows separately because the identically phrased item is used for templates with different frames of reference and context. 

A question can appear more than once for other reasons as well. An item could appear as both a Viva Glint validated item and an item customized by your organization. This image reflects the eSat survey item - "How happy are you working for your company?", with that scenario:

:::image type="content" source="../../media/glint/setup/question-library-identicals.png" alt-text="Screenshot of the eSat item appearing twice in the Question Library.":::

## Survey item tags

Items have associated tags associated to help you sort and filter them. These tags are helpful to understand:

|Tag| Definition and Need-to-Knows|
|-------|------|
|**Referent**| The group or population (Manager, Coworkers, Company, etc.) a respondent should think about when rating an item.|
|**Program**|The Viva Glint survey this item is used in. For example: Engagement, Exit, Onboarding. All items listed by program are loaded into the Viva Glint platform, our survey templates, and the Question Library.|
|**Question Type**|<ul><li>**Rating items** use a 5- or 7-point scale.</li><li>**Open ended items** are items that require text responses. </li><li> **Options** are items that require a selection of single- or multiple-choice responses.</ul>|
|**Action Plan Template**| The action plan content aligned to this item. If shown as "default," the item is using the generic template. If empty, this item has no Action Plan content aligned to it.|
|**Option Text**|The list of response choices for Options items.|
|**# of Alternate Forms**|How many differently worded item choices are available for the "same" item. No number listed indicates that no alternate items are available. There are three types of alternate items: <ul><li> **Substitute items:** have slightly different wording but are an equal substitute for the originally recommended items. These alternatively worded items are still comparable to the original item benchmark.</li><li>**Related items:** similar to the original recommended items, but could be interpreted differently by employees. These items can't be compared to the original item benchmark. </li><li> **Referent items:** ask employees to think about specific referents (responsible level of management) when measuring this experience. These items can't be compared to benchmarks.</ul>|

### More about referents

Throughout the taxonomy, certain items may contain a *Referent* which directs the respondent to think specifically about *who* they're rating when they answer the survey item. About half of the Viva Glint items have Referents. If the Referent column status is **None**, this item describes an experience with no clear referent. 

> Example **with** a referent: “I feel cared about as a person on my team.” 
>
> Example **without** a referent: “At work, I feel cared about as a person.”

#### Not all survey items have Referents

Unless a theme or topic is predominantly experienced through a referent, Viva Glint recommends using items that focus on the experience itself. This practice allows for the fact that most experiences can have multiple influences. It's important to include items without referents because:
- It gives Viva Glint the ability to compare how the customer scored on the item to our external benchmarks.
- It ensures the item is relevant to employees across the customer organization. This is important for using the comparison scores to the Overall Company. Comparisons to benchmarks or company norms are essential to interpreting results, They're an important indicator in determining whether your scores are strong or need improvement.
- Narrative Intelligence (NLP) is built into the platform to pull meaning from comment data. This ability connects the dots between what employees think about broader topics and how they feel about it. 


### Referent definitions

|Referent|Description|
|--------|--------|
|**(My) Team**|These items may read "my team" or "on my team." The items refer to a group of people that the respondent is a member of and who all work either in the same department or for the same manager.|
|**Teams**|These items may read "teams" or "work team(s)." The items refer more generally to groups of people across the company, not necessarily the team the respondent is on.|
|**Coworkers**|These items may read "Coworkers" or "people" or "employees." The items refer to other people, in general not necessarily on the same team as the respondent.|
|**Manager**|These items may read "my manager" or "my Supervisor." The item refers to the person the respondent reports to directly and who most likely has the most influence over the respondent's job and provides the respondent feedback and employment reviews.|
|**Leadership**| These items may read "executive team" or "top leaders" or "leadership team." The items generally refer to the executive team - the CEO and their direct reports.<ul><li>"Leaders" or "leadership" can also be a general reference to leaders at various levels in the company.</li><li>"Leaders in my organization" refers to the management chain above the responder within their larger department or unit.</ul>|
|**Company**| These items may also be stated as "where I work" or "at this company" or "here." The items refer to an experience of the entire company overall.|
|**Industry specific job referent**| Some companies may use specific job titles or common abbreviations. "RN" is an example - Registered Nurse|

With all of the above referents, customers often customize the item by inserting the actual name or using parentheses to clarify who is to be rated. 
> For example, "The leadership team" might be replaced with "Fred Smith and his directs"
> Another example is to simply state the name(s) where the referent would be: I get the support I need from Fred Smith."


>[!NOTE]
>Some items have customized text versions listed as "Referent." These versions allow the user to choose to assign responsibility at a level that is different than the Viva Glint recommended items. Based on industry best practices, benchmarking, and the best judgment of Viva People Science, a referent is included only when it's clear where the onus for taking action is typically assigned.

## Metrics

Items have metrics to help determine when to use them.

|Item|Need-to-know|
|-------|------|
|**Benchmark**|Reads **TRUE** if the item has a benchmark.|
|**Item Popularity**|The number of customers who used this item in the past 12 months.|
|**Correlation with eSat**|The *Pearson coefficient (r)* measuring the item's correlation to eSat (happiness at work). *The Pearson coefficient is a measurement quantifying the strength of the association between two variables. Pearson’s correlation coefficient appears as r.* |

## Item tag categorization

Item tags are categorized in either of these ways:

- **According to the People Success Elements they measure:** The People Success Elements (Purpose, Growth, Clarity, Empowerment, Connection, and Wellbeing) are six categories that summarize the fundamental needs and expectations most critical to a person’s holistic life experience. These needs don't only include their work experience. These needs are those that best shape the environment for high engagement. 

- **According to the domains of employee experience and 14 main topic areas (Leadership, Job, Communication, Growth, Rewards, etc.) that, based on Viva People Science  research, are the most typical industry categories for employee survey items.**





