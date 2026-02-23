# ☕ Coffee Shop Sales Analysis

> *Analyzing retail sales data to uncover actionable insights that enhance Coffee Shop performance.*

---

## 📌 Business Problem

The stakeholder — a coffee shop operating across three locations — wanted to better understand their sales patterns to make smarter business decisions. Specifically, they needed answers to:

- When are customers buying the most? (by hour and day)
- Which months are the strongest for revenue?
- How are the three store locations performing compared to each other?
- What is the average spend per customer?
- Which products are driving the most sales — in quantity and in revenue?
- How do different product categories and types contribute to overall revenue?

The goal was to turn raw transaction data into clear, actionable insights.

---

## 📂 Dataset

| Detail | Info |
|---|---|
| **Source** | Internal retail transaction records |
| **Time Period** | January 2023 – June 2023 |
| **Number of Rows** | 1,49,116 transactions |
| **Number of Columns** | 18 columns |

**Key columns used in the analysis:**

| Column | Description |
|---|---|
| `transaction_date` | Date of purchase |
| `transaction_time` | Time of purchase |
| `store_location` | One of 3 store locations |
| `product_category` | High-level product group (e.g., Coffee, Tea, Bakery) |
| `product_type` | Sub-category (e.g., Barista Espresso, Brewed Chai Tea) |
| `product_detail` | Specific product name |
| `transaction_qty` | Number of units sold |
| `unit_price` | Price per unit |
| `Total Bill` | Revenue from each transaction |
| `Hour` | Extracted hour from transaction time |
| `Day Name` | Day of the week |
| `Month Name` | Month of the transaction |

---

## 🛠 Tools Used

- **Microsoft Excel** — Data cleaning, pivot tables, calculated columns, and analysis
  - Pivot Tables for aggregating sales by day, hour, month, location, and product
  - Formulas for calculated fields (`Total Bill`, `Hour`, `Day Name`, `Month Name`)
  - Filters and sorting for top product identification

---

## 🔍 Analysis & Insights

**Question 1: How do sales vary by day of the week?**
→ Sales are fairly consistent across all 7 days. Monday ($1,01,677) and Friday ($1,01,373) are the top performers, while Saturday ($96,894) sees the lowest revenue — likely because weekday commuters drive more regular morning purchases.

---

**Question 2: Are there any peak times for sales activity?**
→ Yes — the peak sales window is clearly **8 AM to 10 AM**, with 10 AM being the single highest-grossing hour at **$88,673**. After 11 AM, sales drop sharply and stay relatively flat through the evening. The shop is strongly a morning-driven business.

---

**Question 3: What is the total sales revenue for each month?**
→ Revenue grew consistently every month (except a slight dip in February). The shop went from **$81,677 in January** to **$1,66,485 in June** — more than doubling in 6 months. Total revenue for the period: **$6,98,812**.

| Month | Revenue |
|---|---|
| January | $81,677.74 |
| February | $76,145.19 |
| March | $98,834.68 |
| April | $1,18,941.08 |
| May | $1,56,727.76 |
| June | $1,66,485.88 |

---

**Question 4: How do sales vary across different store locations?**
→ All three locations perform remarkably similarly. Hell's Kitchen leads at **$2,36,511**, followed by Astoria (**$2,32,243**) and Lower Manhattan (**$2,30,057**). The gap between the highest and lowest is less than $7,000 over six months — showing consistent performance across all branches.

---

**Question 5: What is the average price/order per person?**
→ The average transaction value is **$4.69 per order**. This indicates the business runs on high transaction volume with relatively small individual purchases — typical for a coffee shop model.

---

**Question 6: Which products are the best-selling in terms of quantity and revenue?**

*By Quantity:*
→ **Ethiopia** tops the chart with 13,271 units sold, followed by Our Old Time Diner Blend (13,074) and Columbian Medium Roast (13,068). Coffee beans dominate the top 5 by volume.

*By Revenue:*
→ **Ethiopia** again leads at $42,304. However, **Sustainably Grown Organic** jumps to 2nd by revenue ($39,065) due to its higher unit price — showing that volume alone doesn't tell the full story. **Latte** and **Dark Chocolate** also feature in the top 10 by revenue despite lower unit counts.

---

**Question 7: How do sales vary by product category and type?**

*By Category:*
→ **Coffee** dominates with **$2,69,952 (38.6%)** of total revenue. **Tea** is second at $1,96,405 (28.1%), followed by Bakery ($82,315) and Drinking Chocolate ($72,416). The core beverages clearly power the business.

*By Product Type:*
→ **Barista Espresso** is the highest-earning product type at **$91,406**, followed by Brewed Chai Tea ($77,081) and Hot Chocolate ($72,416). Among food items, **Scone** leads at $36,866, suggesting strong pairing potential with morning coffee orders.

---

## 📊 Visualizations

> The following visuals were created using **Pivot Charts in Microsoft Excel** as part of the analysis workbook.

- 📈 **Line Chart** — Monthly Revenue Trend (Jan–Jun 2023)
- 📊 **Bar Chart** — Sales by Day of the Week
- 🕐 **Column Chart** — Sales by Hour of the Day (Peak Hours)
- 🗺 **Bar Chart** — Revenue by Store Location
- 🥧 **Pie Chart** — Revenue Share by Product Category
- 📊 **Horizontal Bar Chart** — Top 10 Products by Revenue

*(Screenshots of the dashboard are available in the Excel workbook attached to this repository.)*

---

## 💡 Recommendations

Based on the analysis, here are actionable suggestions for the business:

1. **Staff up during 8–10 AM** — This is peak hour across all stores. Ensuring adequate staffing and stocked inventory during this window will prevent lost sales and improve customer experience.

2. **Investigate the February dip** — Revenue dipped slightly in February. Understanding whether this is seasonal or operational can help plan promotions or campaigns to offset it in future years.

3. **Study Hell's Kitchen's edge** — Since it slightly outperforms the other two locations, it's worth identifying what's working there (layout, staff, local promotions) and replicating it.

4. **Launch a Coffee Bean subscription or loyalty program** — Ethiopia, Brazilian, and Columbian Medium Roast are top sellers by volume. A subscription model or rewards program for repeat buyers could significantly increase retention and revenue.

5. **Promote Scone + Espresso pairings** — Barista Espresso is the #1 product type, and Scone is the top food item. A bundled morning combo offer could increase average order value beyond the current $4.69.

6. **Explore evening promotions** — Sales drop sharply after 11 AM and nearly vanish by 8 PM. Happy hour discounts or evening-specific menu items could help capture more revenue in the off-peak hours.

---

## 🚀 How to Run This Project

This project was done entirely in **Microsoft Excel**. To reproduce the analysis:

1. **Download** the Excel file (`Coffee_Shop_Sales_Data_Analysis_Sheet.xlsx`) from this repository.

2. **Open** the file in Microsoft Excel (2016 or later recommended).

3. Navigate to the **`Sheet1`** tab — this contains the raw transaction data with all calculated columns already in place:
   - `Total Bill` = `transaction_qty × unit_price`
   - `Hour` extracted from `transaction_time`
   - `Day Name` and `Month Name` derived from `transaction_date`

4. Navigate to the **`Pivot`** tab to explore all the pivot tables used for the analysis:
   - Sales by Day of Week
   - Sales by Hour
   - Monthly Revenue
   - Revenue by Store Location
   - Top Products by Quantity and Revenue
   - Sales by Category and Type

5. Navigate to the **`Dashboard`** tab to view the visual summary of all findings.

> **No coding required.** Everything is built with Excel formulas, Pivot Tables, and Pivot Charts.

---

## 👤 Connect With Me

Ashish Sharma
Aspiring Data Analyst | 2nd Data Analysis Project
📧 itsashishsharma1814@gmail.com
🔗 [LinkedIn Profile](www.linkedin.com/in/ashish-sharma-0146481b6)

---

*This project was completed as part of my data analysis learning journey. Feedback and suggestions are welcome!*
