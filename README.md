# Pharmaceutical Sales Analysis (Tableau | Excel)

An end-to-end sales analysis for a pharmaceutical manufacturer in Germany and Poland. I cleaned about 205K sales records in Excel and built four Tableau dashboards for three management levels.

## Business Problem

The company does not sell directly to customers. It sells through distributors, who share their sales data as CSV files. Management wants to understand sales performance at three levels:

| Audience | What they need to see |
|---|---|
| Executive Committee | Overall sales by year, month, channel, sub-channel, and product class |
| Sales Manager / Sales Rep | Sales by distributor, product, customer, and city |
| Head of Sales | Sales by team, manager, and sales rep |

## Dataset

- **Source:** DataMatrix training project (`pharma-data.csv`)
- **Size:** 204,971 sales records, 2017 to 2020, Germany and Poland
- **Fields:** distributor, customer, city, country, channel, sub-channel, product, product class, quantity, price, sales, month, year, sales rep, manager, sales team

## Process

1. Cleaned and prepared the raw data in **Excel**, and used Pivot Tables to check totals.
2. Built calculated fields and four dashboards in **Tableau**.
3. Wrote insights and recommendations for each audience.

**What I cleaned:** [ 
- Removed duplicate records.
- Used TRIM and proper capitalization on most text columns, because many names had extra spaces and inconsistent letters.
- Fixed incorrect data types in several columns.
- Handled many null values: replaced some with suitable values and removed the rows where the data could not be filled.]

---

## Dashboards and Insights

### 1. Top-Level Management Dashboard
**Audience:** Executive Committee | **Question:** How is the company performing, and where do sales come from?

![Top Level Management Dashboard]( https://public.tableau.com/views/Farmastoresalesanalysis/Dashboard6?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

- Total sales are **$9.2B** from **22.3M units**, at an average price of **$412.78** per unit.
- Sales grew **30%** from 2017 to 2018 ($2.70B to $3.51B), then fell **16%** in 2019 ($2.93B). 2020 has data for only [ADD MONTHS COVERED] ($61.7M), so it cannot be compared with full years.
- **August** ($992M) and **March** ($901M) are the strongest months. January is the weakest ($565M).
- **Analgesics** is the top product class ($1.89B, 20.5%). No class is above 21%, and the smallest (Antimalarial) still has 12.4%.
- Sales are split almost evenly between **Pharmacy (52%)** and **Hospital (48%)**. **Retail** is the largest sub-channel (28%) and **Private** is the smallest (22%).

**Takeaway:** Sales are well spread across products and channels, but the 2019 decline is a warning sign that needs follow-up.

### 2. Operational Level Dashboard
**Audience:** Sales Manager / Sales Rep | **Question:** Who and what drive our sales?

![Operational Level Dashboard]( https://public.tableau.com/views/Farmastoresalesanalysis/Dashboard7?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

- **Gerlach LLC** is the largest distributor with **$2.69B (29.3%)**. **Koss** is second with **24.6%**. Together, two distributors handle **54%** of all sales.
- The third distributor, **Erdman**, has only **10.0%** ($924M), far behind the top two.
- The largest customer, Mraz-Kutch Pharma Plc, is only **1%** of sales ($91M). The top 5 cities together make up just 2.9% ($265M).
- The top product, **Ionclotide**, is only 1.7% of sales ($157M). The top 5 products together are 5.4%.

**Takeaway:** Demand is spread across many customers, cities, and products, but it flows through very few distributors. The main risk is in distribution, not in customers.

### 3. Sales Force Performance Dashboard
**Audience:** Head of Sales | **Question:** Which teams and reps perform best?

![Sales Force Performance Dashboard]( https://public.tableau.com/views/Farmastoresalesanalysis/Dashboard5?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

- **Delta** is the top team with **$2.90B (31.5%)**, followed by Charlie ($2.15B), Bravo ($2.14B), and Alfa ($2.02B).
- Each team has exactly one manager, so the manager ranking is the same as the team ranking.
- Delta has **4 reps** while the other teams have **3**. Sales per rep are close: Delta $724M, Charlie $716M, Bravo $713M, Alfa $673M. So Delta's lead comes mostly from team size, not from stronger reps.
- Rep sales range from **$635M** (Stella Given) to **$793M** (Jimmy Grey). The top rep is only 8.6% of total sales, so no single rep drives the business.

**Takeaway:** The sales force is balanced. Comparing teams by total sales is misleading because team sizes are different.

### 4. Geographical Sales Dashboard
**Audience:** Executive Committee / Head of Sales | **Question:** Where are our sales?

![Geographical Sales Analysis Dashboard]( https://public.tableau.com/views/Farmastoresalesanalysis/GeographicalSalesAnalysisDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

- **Germany** generates **$8.52B (92.6%)** of sales and **Poland** only **$681M (7.4%)**.

**Takeaway:** Poland is a very small market. Sales data alone cannot tell if this is low demand or a missed opportunity.

---

## Key Findings

1. Sales fell **16% in 2019** after growing 30% in 2018.
2. **Two distributors handle 54%** of all sales.
3. **Germany is 92.6%** of sales and Poland is 7.4%.
4. Customers, cities, and products are fragmented, and the sales team is balanced per rep.

## Recommendations

1. **Reduce distributor dependency.** Protect the relationship with Gerlach and Koss with clear long-term agreements, and grow mid-size distributors such as Erdman in the same regions.
2. **Find the cause of the 2019 decline.** Compare 2019 with 2018 by month, distributor, and product class. Confirm which months 2020 covers.
3. **Study the Polish market.** Compare the number of distributors and customers in Poland with Germany, and estimate the potential.
4. **Set sales targets per rep, not per team,** because team sizes are different.

## Limitations

- The data has sales only. There are no cost or profit figures, so I cannot judge profitability.
- 2020 is a partial year.
- This is a training dataset, so the findings are for portfolio purposes.

## Tools

Excel (data cleaning, Pivot Tables) and Tableau Public (calculated fields, dashboards).

## Credits

Project brief and dataset by DataMatrix (training project).
