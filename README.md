# Superstore Sales Performance Analysis 📊

## 📌 Project Overview
This project provides a strategic analysis of the Sample Superstore dataset to identify revenue drivers and optimize regional performance. By leveraging **SQL (BigQuery)** for data transformation and **Tableau** for visualization, I uncovered key insights into regional dominance, segment profitability, and product demand.

## 🎯 Key Findings
* **Regional Dominance:** The **West Region** is the top revenue driver.
* **Segment Profitability:** The **Consumer** segment generates the highest volume, while the Home Office segment shows high efficiency.
* **Top Products:** **Phones** and **Chairs** lead in sub-category revenue.
* **Strategic Recommendation:** Reallocate marketing budget toward the West/East regions and optimize inventory for high-demand electronics.

## 🛠️ Tech Stack & Workflow
* **Data Source:** Sample Superstore Dataset.
* **Data Warehouse:** Google BigQuery (SQL) for cleaning and aggregation.
* **Visualization:** Tableau (Trend Analysis & Dashboards).
* **Process:** 1. Ingested raw CSV into BigQuery.
    2. Wrote SQL queries to aggregate sales by Region, Segment, and Category.
    3. Exported clean data to Tableau for executive-level storytelling.

## 📁 Project Contents
* [data](./data): Raw dataset and cleaned versions.
* [analysis](./analysis): SQL scripts used for data extraction and business logic.
* [visuals](./visuals): Interactive Tableau workbook and dashboard previews.
* [report](./report): Final PDF report with strategic recommendations.

## 📊 Sample SQL Logic
```sql
-- Aggregating Total Sales and Profit by Region
SELECT 
    Region, 
    SUM(Sales) AS Total_Sales, 
    SUM(Profit) AS Total_Profit
FROM `project_id.superstore.sales`
GROUP BY Region
ORDER BY Total_Sales DESC;
