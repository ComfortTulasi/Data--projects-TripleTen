# E-commerce Business Analytics: Conversion Funnel & Cohort Analysis

## Project Overview

This project, "Business Analytics Project" (Sprint 3), involved acting as a junior analyst for an e-commerce company to analyze 
raw transaction logs. The core objective was to derive meaningful business metrics from user activity data, specifically focusing 
on building a conversion funnel and performing a cohort analysis to understand user behavior and retention.

## Data Source

The analysis utilized an `event_logs` dataset from the company's website, provided in a Google Spreadsheet. Each row in the 
`raw_user_activity` tab represents an event or activity by a user.

The dataset includes the following columns:

* `user_id`: Unique customer IDs
* `event_type`: Type of activity (e.g., `view`, `shopping_cart`, `purchase`)
* `category_code`: Category of the product
* `brand`: Product brand
* `price`: Product price in USD
* `event_date`: Date of user activity (YYYY-MM-DD format)

## Key Analyses Performed

### Part 1: Build a Conversion Funnel

The executive team sought to understand the effectiveness of product page views converting into purchases.

* **Objective**: Create a conversion funnel to visualize user interaction through different stages.
* **Methodology**:
    * A pivot table was created in a new sheet named `conversion_funnel`.
    * Unique users were counted for each of the three funnel stages (view, shopping cart, purchase).
    * Formulas were used to calculate both total conversion rates and step-by-step conversion rates to the next stage.
* **Insights**: The conversion funnel revealed a total conversion rate of 29% from `view` to `shopping_cart`, and 10% from
* `shopping_cart` to `purchase`. The overall conversion rate from `view` to `purchase` was low.

### Part 2: Prepare Data for Cohort Analysis

The company aimed to build acquisition cohorts based on the month of a user's first purchase and track their metrics over time.
This section involved extensive data preparation.

* **Filter Purchases**:
    * A new sheet, `purchase_activity`, was created.
    * Only `purchase` event types were filtered from `raw_user_activity` and pasted into `purchase_activity` (resulting in 4,845 rows).
* **Calculate First Purchase Dates**:
    * A pivot table was inserted into a new sheet, `first_purchase`, to calculate the minimum `event_date` for each unique `user_id`.
    * The `first_purchase_date` for each user was then transferred to the `purchase_activity` sheet using the `VLOOKUP()` function.
* **Set Up Monthly Data for Cohorts**:
    * Three new columns were created in `purchase_activity`:
        * `event_month`: Month of the event (`YYYY-MM` format) using `TEXT()` function.
        * `first_purchase_month`: Month of the first purchase (`YYYY-MM` format) using `TEXT()` function.
        * `cohort_age`: Number of months between `first_purchase_date` and `event_date` using `DATEDIF()` function (ranging from 0 to
        * 4 months).

### Part 3: Calculate Retention Rates

The final steps involved aggregating purchase data into cohorts and calculating month-by-month retention rates.

* **Group Data into Cohorts**:
    * Another pivot table was inserted into a new sheet, `cohort_analysis`, configured to group data into 6 cohorts based on
    * `first_purchase_month`.
    * The pivot table displayed the count of unique users for each `cohort_age` in the columns.
* **Calculate Overall Retention Rates**:
    * A new sheet, `retention_rates`, was created to present retention data.
    * Row labels for each cohort (chronological order) and column labels for `cohort_age` (1 to 4 months) were added.
    * Formulas were used to calculate the retention rate for each cohort at each `cohort_age`, based on the starting cohort sizes.
* **Insights**: The retention rate analysis showed a general decrease in purchases for subsequent months within cohorts.

### Part 4: Organize and Document Spreadsheet

To ensure a polished and professional deliverable, the spreadsheet was organized and documented according to best practices.

* **Executive Summary**:
    * Brief summary of results and conclusions from the `conversion_funnel` and `retention_rates` sheets.
    * Explanation of the raw data (timespan, event types, collection methods).
    * Clarification on data used for conversion rate calculations (unique user counts).
    * Detailed explanation of cohort analysis decisions (cohort formation, tracking period, retention rate calculation).
* **Sheet Organization**: Tabs were reordered as per a legend: `Table of Contents`, `Executive Summary`, `Analytical Results`
*  (conversion_funnel, retention_rates), `Calculations` (purchase_activity, first_purchase), and `Raw Data`.
* **Formatting**: Consistent formatting applied, including number and date formats, table borders, bold column headers, frozen rows,
*  and highlighted calculation cells.

## Conclusion

This project provided critical insights into user behavior on the e-commerce platform. The conversion funnel highlighted areas for
improvement in the user journey, while the cohort analysis offered a clear view of customer retention trends over time. These findings
are crucial for the executive team to make data-driven decisions to optimize the website, enhance conversion, and improve long-term 
customer engagement and loyalty.

## Technologies Used

* Google Sheets (for data storage, cleaning, pivot tables, and analysis)
