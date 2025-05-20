# Superstore Profit & Loss and Returns Analysis

## Project Overview

This project, "Data Visualization with Tableau" (Sprint 4), involved a comprehensive analysis of Superstore operations to identify areas 
of profit and loss, assess advertising opportunities, and investigate product return rates. The ultimate goal was to provide actionable 
insights to increase the Superstore's profitability and prevent bankruptcy.

## Key Areas of Analysis

The project was divided into three main parts:

### Part 1: Profits & Losses

This section focused on identifying the most significant profit centers and loss-makers within the Superstore's operations.

* **Profit & Loss Centers**: Analysis of various dimension pairs (e.g., subcategory + region, shipping mode + product ID) to pinpoint the
* two biggest profit centers and two biggest loss-makers.
    * **Insights:**
        * **Profit Centers:** Copiers (West Region) and Chairs (East Region) were identified as major profit drivers.
        * **Loss Centers:** Tables (East Region) and Binders (Central Region) were significant loss-makers.
* **Product Performance**: Identification of products that should be discontinued due to low profitability and product subcategories to
*  focus on or stop selling.
    * **Recommendation:** Stop selling products that consistently generate losses. Focus on top-performing subcategories like Copiers and
    *  Chairs, and consider discontinuing or re-evaluating underperforming ones like Tables and Binders.

### Part 2: Advertising

This part explored the potential effectiveness of advertising strategies by identifying optimal combinations of states and months for 
advertising based on average profit per unit sold.

* **Optimal Advertising Locations & Times**: Identification of the top 3 combinations of states and months with high average profit to
*  justify advertising spend.
    * **Insights:** The analysis highlighted specific states and months where advertising would yield the best return on ad spend.
    * **Recommendation:** Allocate advertising budget (1/5 of profits) to these identified high-profit state-month combinations to
    *  maximize return on investment.

### Part 3: Returned Items

This section focused on analyzing product return rates to identify products and customers with abnormally high return rates, and to 
assess the impact of returns on overall profitability.

* **Data Preparation**: The `Returns` table was left-joined with the `Orders` table. A calculated field was created for "Returned"
* (0 for null, 1 for "Yes") to calculate return rates.
* **Key Questions on Returns**:
    * **Products with Highest Return Rate**: Identification of specific products exhibiting the highest return rates.
    * **Customers with Highest Return Rate**: Identification of customers who frequently return products.
    * **Profit vs. Return Rate Analysis**: Visualization of average profit against average return rate across a chosen dimension
    * (e.g., state, shipping mode, product type) to argue for or against continuing business based on this dimension.
    * **Insights**: The analysis revealed which products and customers contributed most to returns. It also showed the trade-off
    *  between profit and return rates across different dimensions.
    * **Recommendations**: Implement strategies to address high return rates, such as improving product quality for problematic items,
    *  reviewing return policies for high-frequency returners, or re-evaluating business segments with high return rates and low
    *   profitability.

## Data and Tools

* **Dataset**: `Superstore.xls`
* **Tool**: Tableau (for data visualization and dashboard creation)

## Project Deliverables

* **Tableau Workbook**: A comprehensive Tableau workbook containing all the visualizations and dashboards created during the analysis.
* **README.md**: This file, providing an overview of the project and its findings.

## Tableau Public Workbook

The finalized Tableau workbook is published on Tableau Public.

[Profit and Loss Analysis by Comfort Tulasi](https://public.tableau.com/views/ProfitandLossAnalysisbyComfortTulasi/ProfitandLossAnalysis?:language=en-US&:display_count=n&:origin=viz_share_link)
