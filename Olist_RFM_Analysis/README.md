# 🛒 Olist E-commerce Customer Segmentation Analysis
> **Goal:** Analyzing 100,000+ orders to identify high-value customer segments and propose retention strategies using the RFM model.

---

## 1. Business Context & Problem Statement
Olist, the largest department store in Brazilian marketplaces, faced a common e-commerce challenge: **Stagnant revenue growth and high Customer Acquisition Costs (CAC).**

* **The Problem:** The marketing team lacked a clear understanding of who their "best" customers were and which customers were about to churn.
* **The Objective:** Implement an **RFM (Recency, Frequency, Monetary) Analysis** to segment the database and provide data-driven recommendations for personalized marketing campaigns.

---

## 2. Analytical Pipeline & Methodology

### 🔧 Step 1: Data Extraction & Engineering (MongoDB)
Instead of using a simple CSV, I built a complex **5-stage MongoDB Aggregation Pipeline** to merge data from `orders`, `order_payments`, and `customers` collections.
* **Challenges:** Handled over 90,000 records and standardized ISO date formats.
* **Key Logic:** Used `$lookup` for joins and `$group` to aggregate total spending and frequency per unique customer.

### 🧪 Step 2: RFM Scoring (Excel)
Calculated RFM scores using a **Percentile-based approach** (`PERCENTRANK.INC`) to ensure segments were statistically balanced.
* **Recency (R):** Days since the last purchase (Standardized from MongoDB ISO dates).
* **Frequency (F):** Total number of successful orders.
* **Monetary (M):** Total amount spent.
* **Scoring Logic:** Scaled each metric from 1-5, where 5 represents the top-performing 20%.

---

## 3. Key Insights (Business Discovery)
Based on the **Multi-axis Dashboard**, I uncovered critical insights:

* **The Revenue Imbalance:** Approximately **80% of Olist's revenue stems from "Standard" (One-time) buyers.** This indicates a highly unstable growth model dependent on constant new acquisition rather than loyalty.
* **The "At Risk" Alert:** A significant portion of historically high-value customers haven't purchased in over 180 days.
* **The Power of Champions:** While "Champions" (VIPs) represent a tiny fraction of the total base, their average order value is 5x higher than the average customer.

---

## 4. Actionable Recommendations
| Segment | Marketing Strategy |
| :--- | :--- |
| **Champions (VIP)** | Exclusive loyalty rewards, early access to new launches, and referral programs. |
| **At Risk** | Re-engagement "We Miss You" email campaigns with high-value discount vouchers. |
| **New Customers** | Onboarding welcome sequence and a "Second-purchase" discount code. |
| **Hibernating** | Low-cost automated win-back campaigns via email or app notifications. |

---

## 📊 Dashboard Showcase & Evaluation
![Olist Dashboard](Olist_RFM_Analysis/Dashboard.png)

### **Expert Review of this Dashboard:**
* **Visualization:** Used a **Combo Chart (Column + Line)** with a **Secondary Axis** to compare "Revenue" (Millions) and "Customer Count" (Thousands) on the same view.
* **Strategic Layout:** Sorted segments by Revenue to immediately draw focus to the most impactful groups.
* **Actionable Storytelling:** Integrated a dedicated Text Box to explain the "Why" behind the data, moving beyond simple descriptive statistics.



