---
title: Color coding in Viva Glint reports
description: Color coding logic differs in various Viva Glint reports. Learn why here.
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: viva strengths and opportunities
ms.collection:  
- m365initiative-viva
- selfserve 
search.appverid: MET150 
ms.topic: article
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 01/30/2025
---

# Color coding in Viva Glint reports

Color coding logic differs between the manager Team Summary report and other executive summary report options. 

## Color coding Strengths & Opportunities in the Team Summary Report

In a manager's Team Summary report, a color is assigned to item scores which are considered Strengths or Opportunities (S&Os). An impact analysis is conducted for each driver item to determine its impact on the outcome (typically, Engagement).
-	Items with High or Very High impact are considered potential Strengths or Opportunities.
-	Items with Low or Medium Impact aren’t considered either a Strength or an Opportunity. These items are colored gray.
-	The outcome items - typically the items that comprise the Engagement Score - are also colored gray.

The items with High or Very High Impact on the outcome (for example, Engagement) are first compared to the benchmark selected. Then, the differences for each item from the benchmark are ranked to determine which are Strengths and which are Opportunities.
-	The half of items with scores highest above the benchmark are considered Strengths. These will be colored blue. 
-	Because not all items in this half may be above benchmark, it’s possible that some items are both below the benchmark and displayed as Strengths.*
-	The half of items with scores furthest below the benchmark are considered Opportunities and are colored red. 
-	Because not all items in this half may be below benchmark, it’s possible that some items are both above the benchmark and displayed as Opportunities.*


> [!TIP]
> To decrease confusion, there is an optional account setting called “Exclude Negative Strengths & Positive Weaknesses” which can be enabled at the account level. 

> [!NOTE]
> If the respondent size of the report is too small, impact is calculated based on the overall company level. See HERE for more information. 


Color Coding for the Strengths & Opportunities Sections of Other Executive Summary Reports

The processes to determine which items are Strengths and which are Opportunities are identical to the process described for the manager’s Team Summary Report, with one exception related to the color coding. In these reports’ table, a blue or red dot is displayed next to each strength and opportunity. Blue dots represent items above the benchmark. Red dots represent items below the benchmark. 

Note! If the majority of items are below the benchmark:
•	Strengths may have a red dot indicating the item is below the benchmark. 
•	If the majority of items are above the benchmark, Opportunities may have a blue dot. 

Color Coding for the Favorability Scale

Favorability is calculated from responses that fall within a specific range along the rating scale.

Glint’s best practice is to use a 5-point rating scale (Viva Glint’s best practice) and the color representation looks like this:
-	Blue represents the percentage of respondents who scored a question 4 or 5. 
-	Red represents the percentage of respondents who scored a question 1 or 2.
-	Gray represents the percentage of respondents who scored a question 3.

Color coding for the Heat Map report

The colors in the Heat Map allow quick identification of systemic patterns and outliers. Color coding is relative and not absolute. To determine the relative coloring in a Heat Map, Glint looks at the range of scores displayed:.

•	Maximum and minimum scores are always displayed as dark blue and dark red.
•	Scores between the maximum and minimum are evenly bucketed in up to seven differently colored buckets. The median score shows in gray.

For example: If the minimum and maximum scores are 52 and 80, then Glint creates seven evenly spaced buckets between 52 and 80.
o	Dark red would be 52-55
o	Dark blue would be 77-80
o	Gray would be 64-68 with the other shades being in between (For changes and differences, the middle gray is used for 0 change or difference. Dark red is used for the biggest negative difference/change, and dark blue for the biggest positive change, and the other color buckets are evenly spaced between the maximum/minimum values and 0 on either side.)

![image](https://github.com/user-attachments/assets/71f44c02-d278-4074-afe4-cb7755f4760f)
