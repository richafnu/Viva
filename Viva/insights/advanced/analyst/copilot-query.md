---
ms.date: 12/02/2024
title: Set up your queries using Microsoft 365 Copilot in Viva Insights
description: Learn how to use Microsoft Copilot while setting up your custom queries
author: zachminers
ms.author: v-zachminers
ms.topic: how-to
ms.localizationpriority: medium 
ms.collection: 
- viva-insights-advanced 
- viva-copilot
- magic-ai-copilot
ms.service: viva-insights
search.appverid: 
- MET150 
manager: abelubetk
audience: Admin
---

# Set up your queries using Microsoft 365 Copilot in Viva Insights

With custom queries and Power BI templates, you can investigate and answer specific questions about Copilot adoption and impact, collaboration, and workplace activities within your organization. But sometimes, you might need help with translating your questions into queries that Viva Insights can run. That’s where Microsoft 365 Copilot in Viva Insights can help.

Copilot can help you choose a Power BI report or custom person query, and simplify the report building process by suggesting metrics, filters, and attributes relevant to your analysis. 

For example, you might want to understand more about how employees use Copilot in your organization. You can ask Copilot, "How does Copilot usage compare across organizations?" Copilot, in response, suggests using the Microsoft 365 Copilot adoption report or a custom person query. You can change the scope of your query at any point during the process. You can also use Copilot to add or modify metrics, filters, and attributes for the query. 

As you type your questions, Copilot also suggests words or phrases to help you complete your question.

>[!Note]
> This feature is currently only available to help you select your Power BI template or query, and within person queries.

## How to use Copilot to select a Power BI template or query

If you’re not sure what type of query to run, Copilot can suggest a predefined Power BI template or custom query to help you get started. Here’s how:

1. In the Viva Insights analyst experience, select **Create analysis** on the left. 

2. In the upper right of the page, select **Copilot**. 

3. A panel on the right will appear with suggested templates and queries to get you started. If one of those looks like a good fit, select it.

    :::image type="content" source="../images/copilot-analyst-create-analysis.png" lightbox="../images/copilot-analyst-create-analysis.png" alt-text="Screenshot that shows where to find specific queries suggested by Copilot.":::

4. Or, if the suggestions don’t seem like a good fit, type the question you’re looking to answer in natural language, such as, "How does Copilot usage compare across organizations?" Copilot will then suggest a template or query.

    :::image type="content" source="../images/copilot-analyst-create-analysis-02.png" alt-text="Screenshot that shows how Copilot can suggest queries based on your question.":::

5. If the suggestion looks like a good fit, select **View report** or **Set up analysis**. Or, type a new question, and Copilot will suggest something different. To view the report's analysis immediately, select **View report**.

    :::image type="content" source="../images/copilot-analyst-view-report.png" lightbox="../images/copilot-analyst-view-report.png" alt-text="Screenshot that shows how to view the report's insights.":::

6. If you select **Set up analysis**, you're brought to the main setup page. Under **Query setup**:
    1. Type a **Query name**. 
    2. Select a **Time period**. **Time period** defaults to **Last 6 months**. 
    3. Set **Auto-refresh** (optional). You can set the query to automatically update by selecting the **Auto-refresh** box. When you select the **Auto-refresh** option, your query automatically runs and computes a new result every time Viva Insights gets updated collaboration data for licensed people.

    >[!Note]
    > If organizational data used in an auto-refreshing query changes (for example, an attribute name is altered or an attribute is removed), the query might stop auto-refreshing.

    4. Type a **Description** (optional).
    5. Change the metric rule (optional). To set a new metric rule, select **More settings**. Then, pick a new rule from the list. For more information about metric rules, refer to [Metric rules](..//analyst/metric-rules.md).

    >[!Note]
    > The **More settings** pane also contains **Group by** settings. Power BI queries are set to **Group by Week**, and you can't edit this field.

7. Under **Metrics, filters, and organizational attributes**, view the list of preselected parameters, which appear as gray tags. These parameters are required to set up the query and you can't remove them. You can, however, add other parameters, and Copilot can help with this too. Use the [steps outlined below](#how-to-use-copilot-to-build-your-person-query).

8. When you're ready to run the query, in the screen's upper right, select **Run**.

## How to use Copilot to build your person query

First, to access custom person queries, follow this navigation in the [advanced insights app](https://analysis.insights.cloud.microsoft/):

**Analysis** > **Custom queries** > **Person queries** > **Start analysis**

Then, use [these steps](..//analyst/person-query.md#set-up-your-query) to enter basic information like the query name, time period, and description.

Next, you need to add metrics, filters, and attributes. This is where Copilot comes in. In the upper right of the page, select **Copilot**.

1. If you already have a specific question in mind, type it in natural language, and Copilot will suggest metrics, filters, and attributes for the question you’re looking to answer.

2. If you have a question like "Are employees in India building social capital?" Copilot can also help you auto-fill the query with suggestions.

    :::image type="content" source="../images/copilot-analyst-suggestions.png" alt-text="Screenshot that shows how Copilot can help with suggested questions.":::

3. If you want to use Copilot's suggestions, select **Add to this query**. Those metrics, attributes, and filters will appear in their designated areas on the setup page, where you can also remove individual parameters from the query.

4. Or, if you want to rephrase your question or ask a different question for a different set of suggested parameters, type the new question in the Copilot panel.

    :::image type="content" source="../images/copilot-analyst-person-query.png" alt-text="Screenshot that shows how Copilot can help with suggested parameters.":::

5. After you've chosen your new parameters, if you want to ask another question, type it in the panel. To use the new suggestions instead of the parameters you've already chosen, select **Replace the current query**.

6. When you’re ready to run the query, in the screen's upper right, select **Run**. You can [access the query's results](./query-results.md) just like you normally would.

## Administrator controls

This feature is on by default. If you don't want users to access Copilot, you as a Viva Insights admin can disable this feature using the Microsoft 365 admin center. [Learn more](/copilot/microsoft-365/microsoft-365-copilot-page).

### Related topics

* [Data, Privacy, and Security for Microsoft 365 Copilot in Viva Insights](../../copilot-data-privacy-security.md)