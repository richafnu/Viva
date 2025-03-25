---
title: Manager Quick Guide for comment summarization in Microsoft 365 Copilot in Viva Glint
description: A guide designed especially for managers using Microsoft 365 Copilot in Viva Glint to summarize comments in survey feedback. 
ms.author: JudithWeiner
author: JudyWeiner
manager: MelissaBarry
audience: admin
f1.keywords: NOCSH
keywords: manager quick guide, comments reporting with Copilot, Comments Report, comment prompts for managers, Glint Manager PDF
ms.collection:  
- m365initiative-viva
- selfserve
- viva-copilot
- magic-ai-copilot
search.appverid: MET150 
ms.topic: how-to
ms.service: viva-glint
ms.localizationpriority: high
ms.date: 3/25/2025
---

# Manager Quick Guide for comment summarization in Microsoft 365 Copilot in Viva Glint

> [!IMPORTANT]
> Copilot in Viva Glint is designed to help managers analyze feedback comments from Viva Glint surveys.. Download this page as a PDF to help your managers get valuable insights from Copilot in Viva Glint.

Copilot in Viva Glint can:
- Summarize comments to identify key themes 
- Summarize comments by demographics
- Summarize comments by survey items
- Identify what actions your employees are asking for
- Summarize non-English comments

## Manager process for reviewing feedback results 

Follow these tasks, in the order that they appear.

| **Task**| **Where to find it**|
|:-----------|:-----------|
| **Review your scores** on the Viva Glint Team Summary dashboard before jumping directly into Copilot. Consider: <br> <ul><li>Where are your high and low scores?<br></li><li>What items have high comment counts? <br></li><li>Are there teams or subgroups scoring higher or lower than others?</ul>|**Manager Team Summary dashboard** <br><br>:::image type="content" source="../../media/glint/setup/copilot-team-summary-1.png" alt-text="Screenshot of the Manager Team Summary dashboard.":::|
|**Review the Strengths & Opportunities section** on the Viva Glint Team Summary dashboard to understand strengths to celebrate and opportunity areas to improve upon.<br> <ul><li>What opportunity items do you want to better understand through the comments?<br></li><li>What themes do you want to explore more?<br></li><li>Select 1-2 Focus Areas to explore for taking action.</ul>|**Strengths & Opportunities section of Team Summary** <br><br>:::image type="content" source="../../media/glint/setup/copilot-strengths-opps.png" alt-text="Screenshot of Strengths & Opportunities on the Manager Team Summary dashboard.":::|
|**Ask Copilot in Viva Glint to dive deeper** to uncover insights around your areas of interest. <br>Examples of Copilot prompts: <br> </li><li> What are people saying about my [top opportunity]?  <br> </li><li> What are people in [region] saying about [topic]?  <br> </li><li> What are people recommending leaders do to improve [topic]? </ul> |**Copilot button** <br><br>:::image type="content" source="../../media/glint/setup/copilot-button-1.png" alt-text="Screenshot of the Copilot button on the Manager Team Summary dashboard.":::|

## Copilot prompt quick tips

||**Recommendation**| **Benefit**| 
|----|:-----------|:-----------|
|:::image type="icon" source="/office/media/icons/search-blue.png":::|**Browse ready-to-use prompts.**|The prompt guide suggests questions to get you started on data exploration.|
|:::image type="icon" source="/office/media/icons/lightbulb-idea-capture-blue.png":::|**Experiment writing your own prompts.**|Try using prompts on different topics, survey items, and demographic groups. Rephrase a comment or word that didn’t work right away.*|
|:::image type="icon" source="/office/media/icons/paragraph-writing-blue.png":::|**Be specific in prompt writing.**|Copilot understands your intended prompt best when you use detailed prompts.|
|:::image type="icon" source="/office/media/icons/paragraph-writing-blue.png":::|**Bundle requests into a single prompt.** Ask multi-step prompts, building up to your anticipated follow-up question.| Copilot can't summarize its own summary!|
|:::image type="icon" source="/office/media/icons/shopping-cart-blue.png":::|**Deep dive into a specific follow-up topic.**| From the summary, choose one or two insights to ask Copilot for more information.|
|:::image type="icon" source="/office/media/icons/sign-up-blue.png":::|**Keep queries to Viva Glint data.**|Copilot in Viva Glint doesn't acess data beyond what's on your dashboard.|

## Important need-to-knows

- For the most relevant summary results, include specific question titles, demographic attributes, prescriptive comments, or other available report filters in your prompt.
- The prompt character limit is 250 characters. You see a character countdown as you add your prompt.
- Copilot only summarizes up to 8000 comments. If you have more than 8000 comments, consider finding a more specific theme to study. Choose one highlight from the summary and ask Copilot to drill down on that theme by supplying more specific comments.
- Copilot can't summarize its own summary! 
- Copilot functions as a chatbot. Choosing the Copilot symbol opens a Copilot pane for you to interact with.
- Copilot is embedded within the existing reporting flow. Within any report, a new window opens so you can look at comments in that report.
- Copilot is only saved within your current user session. After logging out, it disappears. To save your summary, highlight the content, select **Save** and copy it to a document.
  
## Suggested high-level prompts for general comment summarization

Fill in your own attributes, filters, survey names, or employee names where the examples have square brackets examples.

- Summarize all comments for me.
- What are employees saying at my organization?
- Provide [three] actions based on the comments from my employees.
- Provide a summary of the comment themes.
- What are the top [five] topics from the comments?
- What are employees saying that is positive about the organization?
- Provide [three] actions based on comments from my employees for the [item name] item?
- Find comments from employees in the [department name] who have been with the company for [less than one year].
- Show feedback from employees [aged 50+] about our [onboarding] program.
- Tell me what people are saying about [wellbeing] at work.
- Show comments related to [career development].
- Tell me what employees in [APAC] are saying about [work-life balance].

### Deep-dive example

**Prompt:  Summarize the “Microsoft Viva People Success Elements.” Then suggest a few concrete actions for me, as a Department Manager, to improve my employee engagement score. Please use the comments in the [date/name] survey.**

**Consider**:
   - Swap Viva People Success Elements to your organization's core values and then ask Copilot to generate concrete actions based upon that statement to improve engagement scores.
   - Choose one highlight from the summary and ask Copilot to drill down on that theme, taking more from those specific comments.|

## Suggested prompts for specific comment summarization

Fill in your own attributes, filters, survey names, or employee names where the examples have square brackets.

|**Topic**|**Prompt**|
|--------|-----------|
|**Comment summarization/filter**|What are people in the [Marketing] department saying about the [item]?|
|**Comment summarization/compare**|Compare the sentiment of comments from [male] and [female] employees regarding [management support].|
|**Comment summarization/with Viva Insights integration enabled**|Find comments from employees who work [20+ after hours a week.]|
|**Comment summarization/with Viva Insights intgration enabled**|Show feedback on [manager support] from [employees with less than 10 minutes of 1:1 time per week].|
|**Diversity and Inclusion**|What are the common concerns raised by [women in engineering] regarding workplace [inclusion]?|
|**Diversity and Inclusion**|How do comments on the belonging item differ between [male] and [female] employees?|
|**Performance and Productivity**|What feedback do employees give about the current [performance evaluation] process?|
|**Performance and Productivity**|Are there any recurring themes in comments from [high-performing teams]?|
|**Retention and Turnover**|What reasons do employees give for considering [leaving the company]?|
|**Retention and Turnover**|How do comments from [long-tenured employees] differ from those with [less than a year of service]?|
|**Leadership and Management**|What are the common themes in feedback about [senior leadership?]|
|**Leadership and Management**|How do employees perceive the effectiveness of their managers?| 
|**Work Environment and Culture**|What are the main concerns employees have about [the current work environment]?|
|**Work Environment and Culture**|How do comments about [company culture] vary between [remote] and [on-site] employees?|

## Viva Glint values your feedback

If your manager has enabled the feature, you can submit feedback to Microsoft. Inlude screenshots and attachments.

## Find more detail information

[How managers use Microoft 365 Copilot in Viva Glint](/../../viva/glint/setup/copilot-managers)
