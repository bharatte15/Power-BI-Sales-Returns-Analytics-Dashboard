# 📊 Power BI Sales & Returns Analytics Dashboard

An interactive Power BI report designed to analyze sales performance, customer conversion funnels, return patterns, and key drivers influencing business outcomes.

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=power-bi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Data_Analysis_Expressions-blue?style=for-the-badge)
![Power Query](https://img.shields.io/badge/Power_Query-M_Code-green?style=for-the-badge)

---

## 🖼️ Dashboard Overview

![Main Dashboard Screenshot](screenshots/overview_dashboard.png)

---

## 🚀 Key Features & Insights

* **Key Drivers & Influencers:** Identified core drivers and factors behind return flags across sales channels, product categories, countries, and discount percentages using Power BI's AI Key Influencers visual.
* **Customer Journey Funnel Analysis:** Tracked conversion across funnel stages to isolate drop-off points in customer acquisition and engagement.
* **Sales & Returns Trend Analysis:** Evaluated volume trends (**Units Sold** vs. **Count of Return**) across years and geographical regions using dual-axis line and clustered column combo charts.
* **Dynamic Interactivity:** Integrated cross-filtering, dynamic slicers, and drill-through capabilities for granular data exploration across dimensions.

---

## 🛠️ Tech Stack & Skills Demonstrated

* **Business Intelligence:** Power BI Desktop (`.pbip` / `.pbix`)
* **Data Modeling & Calculations:** DAX (Measures, Calculated Columns, Time Intelligence)
* **Data Transformation:** Power Query / M Code
* **Core Analytics:** Key Drivers Analysis, Funnel Analysis, Diagnostic & Trend Analytics

---

## 📊 Key DAX Measures & Calculations

```dax
// Sum of Units Sold
Sum of Units Sold = SUM('Sales'[Units Sold])

// Count of Return
Count of Return = COUNT('Returns'[Return ID])

// Return Rate (%)
Return Rate % = 
DIVIDE(
    [Count of Return],
    [Sum of Units Sold],
    0
)
