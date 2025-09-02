# E-commerce Customer Churn Analysis

## Project Overview
This project simulates a real-world data analysis scenario for an e-commerce company. The primary goal was to understand the key factors driving customer churn. By using a data-driven approach, the project identifies specific customer segments at high risk of churn, providing the business with actionable insights for targeted retention strategies.

## The Problem
The company was experiencing a significant number of customer churns, but standard analysis of demographic data (age, gender) and basic purchasing metrics provided no clear, actionable patterns. The business needed to move beyond surface-level metrics to identify the "why" behind customer churn and pinpoint which customers were most at risk.

## The Approach: A Transparent Look at the Process
My approach involved a multi-step analytical process, meticulously documented in the accompanying Jupyter Notebook:

**Data Loading and Cleaning:** I began by loading the raw `ecommerce_customer_data.csv` dataset. The data was inspected for missing values and inconsistencies. The `Purchase Date` column was converted to a proper datetime format to enable time-based analysis.

**Feature Engineering (RFM Analysis):** This was a critical step in which I went beyond the provided data to create new, behavioral features based on the RFM (Recency, Frequency, Monetary) model. These new features measured:
*   **Recency:** The number of days since a customer's last purchase.
*   **Frequency:** The total number of purchases a customer has made.
*   **Monetary:** The total amount of money a customer has spent.

**Binning and Segmentation:** To create meaningful customer profiles from the continuous data, I binned the Recency, Frequency, and Monetary values into logical categorical groups. This process transformed raw numbers into powerful business segments (e.g., Monetary Group: 50K+, Frequency Group: 11-15).

**Combined-Feature Analysis:** This was the core of the analysis. I used a pivot table to examine how combinations of Product Category, Monetary Group, and Frequency Group correlate with churn rates. This cross-tabulation of multiple features was the key to uncovering a hidden, at-risk customer segment.

**Visualization and Reporting:** Using a business intelligence tool, Tableau, I created an interactive dashboard to visually represent the findings. The dashboard highlights the specific customer segments that are most vulnerable to churn, making the insights accessible and actionable for a non-technical audience.

## The Result: The Insight
The analysis uncovered a powerful and surprising finding: a specific customer segment with a 100% churn rate.

The at-risk customer profile is consistent across all product categories:
*   **Monetary Group:** Customers with a high monetary value ($50K+)
*   **Frequency Group:** Customers with a medium-high purchase frequency (11-15 transactions)

This insight provides a direct and immediate opportunity for the business to create a targeted retention strategy for this valuable yet highly volatile customer segment.

See the full interactive dashboard and visualizations here:
[https://public.tableau.com/views/CustomerChurnRatebyProductCategoryMonetaryValueandPurchaseFrequency_/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link](https://public.tableau.com/views/CustomerChurnRatebyProductCategoryMonetaryValueandPurchaseFrequency_/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Tools Used
*   **Jupyter Notebook:** For data cleaning, feature engineering, and analysis.
*   **Python Libraries:** Pandas for data manipulation and NumPy for numerical operations.
*   **Tableau Public:** For creating compelling and interactive data visualizations.

## Next Steps
Based on this analysis, the next steps for a real-world project would be:
1.  Develop and implement a predictive model to identify at-risk customers in real-time.
2.  Create and A/B test a targeted retention campaign for the high-risk customer segment.
3.  Present findings to stakeholders with a focus on business impact and ROI.
