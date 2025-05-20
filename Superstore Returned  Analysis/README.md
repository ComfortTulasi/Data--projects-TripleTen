
# Superstore Returned Orders Analysis

## Project Overview

This project, "Storytelling with Data: Project" (Sprint 5), focuses on analyzing the causes of a high number of returned orders at
a Superstore. The primary goal was to prepare a comprehensive analysis for the CEO to understand the root causes of customer returns
and propose actionable strategies to reduce their volume. The analysis involved preparing various data visualizations and culminates 
in a Tableau dashboard and presentation.

## Key Questions Explored

The analysis delved into several key areas to identify the root causes of returns:

* **Correlation between Sales and Returns**: Investigating if higher sales correlate with higher returns across product
* subcategories.
* **Return Rate by Product Category**: Analyzing which product categories exhibit the highest return rates.
* **Return Rate by Customer**: Identifying customers who are more prone to making returns, excluding those with only one order.
* **Geographic Concentration of Returns**: Mapping return rates by geographic measures (state, city) to identify areas with
*  concentrated returns.
* **Seasonal Effect on Returns**: Examining return rates over time (month, week) to determine if there's a seasonal pattern.
* **Multi-Factor Analysis**: Creating composite charts to show return rates influenced by a mix of multiple factors (e.g., date, geography, product category).

## Data and Methodology

The project utilized the `Superstore.xls` dataset. A crucial step involved left joining the `Returns` table onto the `Orders` table.
A calculated field was created for "Returned" where null values were set to `0` and "Yes" values to `1`, allowing for the calculation 
of return rates (average of this field) and total returns (count or sum).

## Key Visualizations and Insights

The analysis leveraged various visualizations to uncover insights:

* **Scatter Plot of Total Sales & Total Returned by Sub-Category**: This plot shows the relationship between sales and returns. The
* trend indicates that an increase in sales often corresponds to an increase in returns.
* **Bar Chart of Returned Rate by Product Category**: This chart reveals that Technology has the highest return rate, though only by a small margin (0.02). At this category level, no immediate actions are recommended to reduce returns.
* **Returned Rate by Customers**: Bar charts display the return rate by customer, filtered to include only customers with more than one order.
    * **Recommendation**: For the top 5 customers with high return rates, it is suggested to consider discontinuing free returns, as it appears to be a costly abuse of policy for the company.
* **Returned Rate Geographical (Map)**: A geographical map visualization shows return rates by state, highlighting areas with
* concentrated returned orders. Utah, for example, has the highest return rate.
    * **Recommendation**: Implement a return policy pop-up before purchase in areas with high return rates like Utah.
* **Returned Rate by Time (Month)**: A chart displaying return rates by month indicates if returns are affected by seasonality. August
* has the highest return rate.
    * **Recommendation**: Implement extra quality control checks and use tamper-proof packaging to ensure product safety during shipping, especially in high-return months like August.
* **Composite Charts for Returned Rate Mix**: Two composite charts (Line and Bar) show the return rate and total returned orders across multiple factors. The line chart shows a higher return in August, while the bar chart shows a higher return in September.
    * **Recommendation**: Consider offering exchange options to encourage customers to swap products instead of returning them,
    *  especially during peak return months.

## Dashboard for Monitoring Returns

The project included the creation of a Tableau dashboard for monitoring returns. This involved:

1.  **Low-Fidelity Mock-ups**: Three variations of pen-and-paper sketches for the dashboard design.
2.  **Dashboard Template**: A template created in Tableau using empty containers to match the chosen mock-up.
3.  **Finalized Dashboard**: Worksheets were added to the template, and the dashboard was finalized with relevant markers, images, and titles.

## Presentation of Analysis and Dashboard

A Tableau Story was constructed to present the analysis and dashboard, following a structured story arc:

1.  **Summary of Analysis**: Discussing how returns should be measured (return rate, total cost, or total number of returns) and when
2.  each measure is most appropriate.
3.  **Key Root Causes**: Highlighting the primary reasons for returned orders identified through the analysis.
4.  **Dashboard Overview**: Explaining each component of the dashboard, its interpretation, and how to use filters to identify root
5.   causes.
6.  **Actionable Steps**: Describing practical actions that can be taken after using the dashboard to address the identified root
7.  causes.
8.  **Conclusion and Next Steps**: Summarizing the findings and proposing future actions, such as dashboard implementation.

## Tableau Public Workbook

The finalized Tableau workbook is published on Tableau Public.

[Returns dashboard by Comfort Tulasi](https://www.loom.com/share/5b8848f9c92e45fea541dbe09acf0495?sid=421997db-9c72-4578-ac7d-3198742a5033) 

## Technologies Used

* Tableau Public
* Microsoft Excel (for data)
* PDF (for report/presentation submission)
