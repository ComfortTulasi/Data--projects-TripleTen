# Shopify App Analysis with Power BI

## Project Overview

This project, "Power BI: Project" (Sprint 6), involved reviewing the landscape of applications on the Shopify platform using publicly
scraped data. The main objective was to identify key factors contributing to the success of a Shopify app. The analysis is presented 
through a Power BI report, with each numbered part corresponding to a separate page in the report.

## Data Source

The analysis utilizes the `shopify.xlsx` dataset, which comprises four interconnected tables:

* **`apps`**: Contains details about apps available on the Shopify apps marketplace.
* **`apps_categories`**: A join table connecting apps with their respective categories.
* **`categories`**: Lists the different categories for the apps (each app can belong to multiple categories).
* **`reviews`**: Provides information on user opinions about apps, including rating, comments, and developer responses.

## Key Areas of Analysis and Visualizations

The Power BI report is structured into three main sections, each on a dedicated page:

### Part 1: App Landscape

This section explores key statistics about the types of apps available on the Shopify platform, primarily using data from the `apps` 
table.

* **Total Unique Apps (KPI Card)**: A KPI card displaying the total count of unique apps on the platform.
* **Sum of Review Count by Last Modified Date (Line Chart)**: A line chart showing the sum of review counts over time, using the
* `lastmod` date on the X-axis (without date hierarchy).
* **Average Rating by Reviews Count (Scatterplot with Annotation)**: A scatterplot illustrating the relationship between
* `reviews_count` (X-axis) and `average rating` (Y-axis). An inserted text box provides interpretation of the observed correlation.

### Part 2: Reviews

This section delves deeper into the review data, introducing new calculated columns to derive more meaningful insights.

* **Helpful Reviews (Calculated Column & Card)**:
    * A new DAX column, `helpful_reviews`, is created in the `Reviews` table using the formula: `rating * (1 + helpful_count)`.
    * This weighs reviews by their perceived helpfulness.
    * A card visual displays the average value of this new `helpful_reviews` column.
* **Developer Answered (Calculated Column & Scatterplot)**:
    * A new DAX column, `developer_answered`, is created in the `Reviews` table. It returns `1` (or `TRUE`) if the `developer_reply`
    *  column is not blank, and `0` (or `FALSE`) otherwise.
    * A scatterplot compares the `average rating` (Y-axis) by the value of the `developer_answered` column (X-axis), indicating the
    *  impact of developer responses on ratings.

### Part 3: App Reviews

This section focuses on connecting app data with review data to analyze developer performance and responsiveness.

* **Developer by Sum of Rating (Bar Chart)**:
    * A many-to-one relationship is established in the data model between the `Reviews` table (`app_id`) and the `Apps` table (`id`).
    * A bar chart visualizes the `developer` (X-axis) against the `sum of rating` (Y-axis).
* **Developer by Helpful Review Average (Bar Chart)**:
    * To provide a more accurate view, a new bar chart is created showing `developer` (X-axis) against the `average of helpful_review`
    *  (Y-axis). This addresses the misleading nature of simply summing ratings.
* **Most Responsive Developers (Filtered Bar Chart)**:
    * A bar chart displays `developer` from the `apps` table against the `developer_answered` column (created in Part 2).
    * A visual-level filter is applied to include only rows where `reviews_count` is greater than 500, highlighting responsiveness for
    *  apps with substantial review volume.

## Project Deliverables

The project is submitted as a Power BI Desktop file (`.pbix`). The GitHub repository contains documentation and, ideally, screenshots 
of each of the 8 required visualizations from the Power BI report.

## Technologies Used

* **Power BI Desktop**: For data modeling, DAX calculations, and report visualization.
* **Microsoft Excel**: For the source dataset (`shopify.xlsx`).

## Conclusion

This Shopify App Analysis provides valuable insights into app success factors, review dynamics, and developer engagement. The Power BI
report serves as an interactive tool to explore these findings, helping stakeholders understand the app landscape and potentially 
identify strategies for app development and marketing on the Shopify platform.
