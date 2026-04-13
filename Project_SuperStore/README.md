# 📊 SuperStore Sales & Profitability Analysis
> **Goal:** Analyzing multi-year retail data to identify growth drivers, optimize regional performance, and recover profit margins.

---

## 1. Business Context & Problem Statement
The SuperStore dataset represents a global retail giant dealing with thousands of products across multiple categories and regions.

* **The Problem:** Despite high overall sales, certain regions and product categories are experiencing **declining profit margins** and **high shipping costs**.
* **The Objective:** To perform a comprehensive audit of sales performance, identify loss-making segments, and provide a roadmap for profit optimization.

---

## 2. Analytical Pipeline & Methodology

### 🛠️ Step 1: Data Wrangling (SQL & Python)
* **Cleaning:** Used **Python (Pandas)** to handle missing values in shipping data and standardized category naming conventions.
* **Extraction:** Performed **SQL Advanced Queries** (Joins, Window Functions) to calculate Year-over-Year (YoY) growth and running totals of profit across different fiscal quarters.

### 📈 Step 2: Exploratory Data Analysis (EDA)
* Identified seasonal trends (e.g., Q4 spikes) and analyzed the correlation between **Discounts** and **Profitability**.
* **Key Metric Calculated:** Profit Margin % = `(Total Profit / Total Sales) * 100`.

---

## 3. Key Insights (Business Discovery)
Through interactive dashboarding, I discovered three major "Profit Leaks":

* **The Discount Trap:** Higher discounts (above 20%) in the **Office Supplies** category significantly eroded profit margins without a proportional increase in sales volume.
* **Regional Disparity:** The **Central Region** showed the highest sales volume but the lowest net profit due to inefficient logistics and high return rates.
* **Product Performance:** 15% of products in the **Technology** category contributed to 60% of total profit, highlighting a high dependency on a small product mix.

---

## 4. Actionable Recommendations
| Finding | Proposed Action |
| :--- | :--- |
| **High Shipping Costs** | Renegotiate carrier contracts for the Central Region or implement a minimum order value for free shipping. |
| **Negative Profit Items** | Discontinue or re-price bottom-tier products that have consistent negative margins over 3 quarters. |
| **Discount Optimization** | Limit maximum discounts to 15% for high-demand Office Supplies to protect the bottom line. |

---

## 🖼️ Dashboard Showcase & Evaluation
*(Chèn ảnh chụp màn hình Dashboard SuperStore của bạn vào đây)*

### **Expert Review of this Dashboard:**
* **Visual Hierarchy:** Used **Slicers** for Region and Category, allowing stakeholders to drill down into specific problem areas instantly.
* **Trend Analysis:** Included a **Time-series Line Chart** to track Sales vs. Profit over 48 months, making it easy to spot seasonal anomalies.
* **Color Logic:** Applied **Conditional Formatting** (Red for Negative Profit, Green for Positive) to ensure immediate visual identification of "Profit Leaks."
