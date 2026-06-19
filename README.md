# PowerBI-Superstore-Sales-Analysis

> **An Interactive Power BI Business Intelligence Solution for Executive & Operational Decision-Making.**

## 🔗 Project Overview
This repository contains a professional-grade, multi-page Power BI dashboard designed to analyze and optimize retail business performance using the classic Kaggle **Sample - Superstore.csv** dataset. 

The project focuses on converting raw transactional data into actionable executive insights, addressing macro-level business growth, regional performance leaks, seasonal profitability trends, and product-level inventory velocity.

---

## 🚀 Key Features & Dashboard Pages

### 1. Executive Summary Page (`Dashboard Summary.png`) - https://github.com/Rahul-1435/PowerBI-Superstore-Sales-Analysis/blob/main/Dashboard%20Summary.png
*Focuses on high-level business health, macro growth, and regional breakdown.*
*   **Macro Trend Analysis:** A Line and Stacked Column combo chart tracking Total Sales, Profit, and Order Volume concurrently to verify real growth trajectory over time.
*   **Seasonality Tracking:** A Month-over-Month trend visual tracking historical Profit Margin % fluctuations to pinpoint seasonal revenue patterns.
*   **Diagnostic Scatter Plot Analysis:** A dedicated Sales-vs-Profit matrix isolating regional performance to instantly identify anomalies (e.g., high-revenue, low-profit underperforming zones).
*   **Demographic Segmentation:** Visualizing distribution across Consumer, Corporate, and Home Office demographics.

### 2. Product Sales Performance Page (`Dashboard Sales Performance.png`) - https://github.com/Rahul-1435/PowerBI-Superstore-Sales-Analysis/blob/main/Dashboard%20Sales%20Performance.png
*Focuses on granular product diagnostics, geographic reach, and inventory velocity.*
*   **Product Pareto Analysis:** Highlighting the Top 10 revenue-driving items alongside a micro-scaled, data-labeled Bottom 10 visual to identify stagnant stock.
*   **Geographic Sales Concentration:** Interactive bubble map tracking regional penetration across the United States.
*   **Categorical Deep-Dives:** A structural Tree Map analyzing product composition across Technology, Furniture, and Office Supplies.
*   **Detailed Performance Matrix:** A tabular lookup grouping product data by sales, profit volume, and exact item-level profit margin ratios.

---

## 🛠️ Data Architecture & DAX Measures Developed
To ensure a high-performing and dynamic user experience, native column aggregation was avoided in favor of customized DAX (Data Analysis Expressions) modeling:

*   **Total Sales:** 
```DAX
    Total Sales = SUM('Sample - Superstore'[Sales])
    ```
*   **Total Profit:** 
```DAX
    Total Profit = SUM('Sample - Superstore'[Profit])
    ```
*   **Total Orders (Volume):** 
```DAX
    Total Orders = DISTINCTCOUNT('Sample - Superstore'[Order ID])
    ```
*   **Profit Margin %:** 
```DAX
    Profit Margin = DIVIDE([Total Profit], [Total Sales], 0)
    ```

---

## 💡 Business Insights Uncovered
*   **The Central Region Anomaly:** While the Central region ranks 3rd in revenue contribution ($501.24K), the diagnostic scatter plot isolates it as heavily underperforming in profitability ($39.71K) relative to its sales volume due to structural margin compression.
*   **Core Revenue Drivers:** Technology and Furniture subcategories (specifically Phones and Chairs) represent the vast majority of organizational revenue weight.
*   **The Bottom 10 Reality:** Several low-velocity office supplies are generating individual product sales under $10, highlighting opportunities to streamline supply chains or bundle low-value SKUs.

---

## 🎨 UI/UX & Formatting Framework
*   **Consistent Theming:** Designed with a sleek, dark carbon executive header styling to emphasize critical KPI cards (`Total Sales`, `Total Profit`, `Total Orders`, `Profit Margin`).
*   **Scannability:** Used explicit horizontal bar charting for text-heavy categorical titles to ensure complete left-to-right legibility without vertical truncation.
*   **Cross-Filtering Environment:** Fully interactive slicers for `Date of Order`, `Category`, `Segment`, and `Region` allow stakeholders to completely isolate independent filter contexts seamlessly.

