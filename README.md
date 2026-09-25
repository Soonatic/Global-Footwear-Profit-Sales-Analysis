# Global Footwear — Sales Analytics Dashboard

## Project Overview

This project presents an end-to-end **Global Sports Footwear Sales Analytics solution** built around a 30,000-order transactional dataset covering **2018–2026**.

The solution demonstrates the complete analytics workflow:

**Raw Data → Data Cleaning → Data Organization → KPI Development → Interactive Dashboard → Trend Analysis → Product & Market Analysis → Business Insights & Recommendations**

The project combines a structured Excel data model with a responsive **HTML/Chart.js interactive dashboard** titled **Global Footwear Sales Analytics**.

---

## 1. Client Requirements & Business Problem

The business operates across multiple international footwear markets and sells sports footwear through both **Online** and **Retail Store** channels.

The source data contains order-level information covering:

- Brand
- Model
- Category
- Gender
- Size
- Color
- Base Price
- Discount
- Final Price
- Quantity
- COGS
- Net Sales
- Gross Profit
- Payment Mode
- Sales Channel
- Country
- Customer Rating

The objective is to convert the transactional data into an analysis-ready model and provide management with an interactive view of **sales, profitability, pricing, products, customers, geography, and trends**.

### Client Requirements

![image alt](https://github.com/Soonatic/Global-Footwear-Profit-Sales-Analysis/blob/52471bb151fafeb3035ec61a8668c86bf517e2f3/Screenshot%202026-09-25%20193201.png)

| Requirement | Deliverable |
|---|---|
| **Data Cleaning** | Standardize field names, dates, numeric fields, discount percentages, and analytical measures. |
| **Data Organization** | Create a structured clean dataset with calculated COGS, Net Sale, and Gross Profit fields. |
| **Sales Analysis** | Analyze sales by time, brand, category, country, channel, gender, payment method, and model. |
| **Profitability Analysis** | Measure Gross Profit and Gross Margin across products, brands, categories, markets, and discount levels. |
| **Pricing Analysis** | Evaluate the relationship between discount depth, sales, order volume, and gross profit. |
| **Dashboard** | Build an interactive HTML dashboard with filters, KPIs, charts, tables, and insights. |
| **Business Insights** | Surface portfolio, pricing, trend, product, customer, and market observations. |
| **Recommendations** | Translate analytical findings into practical commercial actions. |

---

## 2. Data Cleaning & Quality Assurance

The workbook contains two main data layers:

- **global_sports_footwear_Raw**
- **global_sports_footwear_Clean**

The raw dataset contains **30,000 order records** and **18 columns**. The cleaned dataset contains **30,000 records** and **19 analytical columns**.

No blank values were found in the inspected raw or cleaned fields, and the raw order IDs are unique.

### Cleaning and transformation activities

- Standardized column names
- Standardized date fields
- Converted discount values into percentage values
- Standardized product, brand, category, gender, payment, channel, and country fields
- Organized numeric price, quantity, COGS, sales, and profit fields
- Added calculated **COGS**
- Added calculated **Net Sale**
- Added calculated **Gross Profit**
- Renamed transactional fields into business-friendly analytical names
- Preserved the underlying numerical values for analysis

### Data-quality summary

| Quality Check | Result |
|---|---:|
| Raw transaction records | 30,000 |
| Clean transaction records | 30,000 |
| Raw columns | 18 |
| Clean columns | 19 |
| Duplicate full rows detected | 0 |
| Duplicate Order IDs detected | 0 |
| Blank values in inspected datasets | 0 |
| Date coverage | Jan 2018 – Dec 2026 |
| Brands | 6 |
| Categories | 5 |
| Countries | 6 |
| Sales channels | 2 |

---

## 3. Data Organization & Analytical Model

The cleaned dataset is structured around the following fields:

- Order-ID
- Order-Date
- Brand
- Model
- Category
- Gender
- Size
- Color
- Base-Price
- Discount %
- Final-Price
- Qty
- COGS
- Net Sale
- Gross Profit
- Payment-Mode
- Channel
- Country
- Rating

### Key business calculations

**Final Price**

`Base Price × (1 − Discount %)`

**Net Sale**

`Final Price × Qty`

**Gross Profit**

`Net Sale − COGS`

**Gross Margin**

`Gross Profit ÷ Net Sale`

The analytical model supports slicing the business across time, brands, products, categories, customer attributes, countries, channels, payment modes, and pricing tiers.

---

## 4. Executive Dashboard

The interactive HTML dashboard is titled **Global Footwear Sales Analytics** and is designed as a multi-section analytical application. fileciteturn0file0L1-L5

### Dashboard capabilities

- KPI cards
- Interactive filters
- Clear-all filtering control
- Light/Dark theme switch
- Responsive layout
- Interactive Chart.js visualizations
- Dynamic tables
- Recalculated insights based on selected filters
- Latest matching order records

### Dashboard filters

Users can filter the analysis by:

- Brand
- Category
- Country
- Channel
- Gender
- Payment Mode
- Discount Tier
- Year

### Dashboard sections

| Section | Main Analysis |
|---|---|
| **Dashboard** | Monthly sales/profit, yearly sales, category mix, discount vs margin, brand sales |
| **Trends** | Yearly performance, seasonality, YoY change, quarterly sales |
| **Geography** | Country sales/profit, AOV, channel mix, order distribution |
| **Products** | Brand performance, category balance, gender/category mix, top models |
| **Customers** | Gender, channel, payment mode, rating distribution, brand ratings |
| **Pricing** | Orders by discount, gross profit per order, brand discount mix, annual discount |
| **Records** | Latest 100 filtered order records |

---

## 5. Key Business Insights

The cleaned dataset contains:

- **30,000 orders**
- **75,006 units**
- **$9.081M Net Sales**
- **$3.841M Gross Profit**
- **42.3% Gross Margin**
- **$5.241M COGS**
- Average order value of approximately **$302.71**
- Average customer rating of approximately **4.00 / 5**

### Brand Performance

The six brands are:

- ASICS
- Adidas
- New Balance
- Nike
- Puma
- Reebok

ASICS generates the highest Net Sales in the full dataset at approximately **$1.561M**, followed by Nike and New Balance.

The overall brand distribution is relatively balanced, with no single brand dominating the portfolio.

### Category Performance

The five categories are:

- Basketball
- Gym
- Lifestyle
- Running
- Training

**Lifestyle** generates approximately **$1.845M** in Net Sales, followed closely by Training and Basketball.

The category mix is also relatively balanced, allowing management to evaluate category performance without relying on one category alone.

### Geography

The dataset covers:

- Germany
- India
- Pakistan
- UAE
- UK
- USA

The **UAE** records the highest Net Sales at approximately **$1.546M**, while Pakistan records the lowest among the six markets at approximately **$1.466M**.

### Sales Channel

Sales are almost evenly split between:

- **Retail Store:** approximately $4.541M
- **Online:** approximately $4.541M

This provides a useful basis for comparing digital and physical channel performance.

### Customer Gender

Women generate approximately **$3.085M** in Net Sales, followed by Men at approximately **$3.027M** and Unisex at approximately **$2.970M**.

### Payment Methods

Net Sales by payment method are distributed across:

- Bank Transfer
- Wallet
- Card
- Cash

Bank Transfer contributes the largest amount at approximately **$2.346M**.

---

## 6. Pricing & Discount Analysis

The dataset includes six discount tiers:

- 0%
- 5%
- 10%
- 15%
- 20%
- 30%

The analysis shows a clear relationship between increasing discount depth and profitability.

| Discount | Net Sales | Gross Profit |
|---:|---:|---:|
| 0% | $1.724M | $0.862M |
| 5% | $1.695M | $0.803M |
| 10% | $1.565M | $0.696M |
| 15% | $1.443M | $0.594M |
| 20% | $1.428M | $0.535M |
| 30% | $1.226M | $0.350M |

Gross profit per order declines substantially as discount depth increases. The dashboard therefore treats **discount strategy as a key commercial lever**.

The dashboard's automated insights specifically examine whether deeper discounts generate additional order volume and compare margin performance across discount tiers.

---

## 7. Product Performance

The cleaned dataset contains **899 distinct models**, ranging from Model-100 through Model-998.

The dashboard includes a **Top 10 Models** analysis and uses model-level sales contribution to understand product concentration.

Examples of higher Net Sales models include:

- Model-863
- Model-855
- Model-604
- Model-342
- Model-335

The model distribution is broad, so the dashboard recommends using model-level margin and inventory analysis before making product-pruning decisions.

---

## 8. Trend Analysis

The dataset covers nine calendar years:

**2018 → 2019 → 2020 → 2021 → 2022 → 2023 → 2024 → 2025 → 2026**

Annual Net Sales are relatively stable across the period, with annual totals ranging from approximately **$970K to $1.032M**.

The dashboard provides:

- Yearly Net Sales
- Yearly Gross Profit
- Gross Margin %
- Year-over-Year change
- Monthly seasonality
- Quarterly sales
- Selected-year comparisons

This allows users to distinguish structural business trends from shorter-term monthly or quarterly fluctuations.

---

## 9. Business Recommendations

Based on the analytical model and dashboard logic, the project supports recommendations around:

### Pricing

- Monitor margin impact before increasing discount depth.
- Use deep discounts selectively rather than as a default pricing strategy.
- Compare order volume against profitability when evaluating promotions.

### Product Portfolio

- Monitor top models for availability and inventory planning.
- Investigate low-performing models using sales, margin, rating, and demand together.
- Avoid product-pruning decisions based on sales alone.

### Brand & Category Management

- Maintain balanced investment across brands and categories.
- Identify category-specific opportunities using both Net Sales and Gross Profit.
- Use customer and channel filters to understand where individual categories perform differently.

### Geography

- Compare country performance using both sales and profitability.
- Investigate differences between high- and low-performing markets.
- Evaluate channel mix within each country before reallocating resources.

### Channel Strategy

- Continue monitoring Online and Retail Store performance separately.
- Compare channel performance by country, category, brand, and product.
- Use the near-even channel split as a basis for detailed channel-level analysis.

---

## 10. Workbook Structure

| Sheet | Purpose |
|---|---|
| **global_sports_footwear_Raw** | Original 30,000-row transactional dataset. |
| **global_sports_footwear_Clean** | Cleaned and organized 30,000-row analytical dataset with 19 columns. |

### Dashboard File

**`footwear_dashboard-C(1).html`**

The HTML dashboard provides the interactive analytical presentation layer with filters, charts, tables, themes, and dynamic insights.

---

## 11. Dashboard Architecture

The HTML dashboard uses:

- HTML
- CSS
- JavaScript
- Chart.js
- Responsive CSS Grid
- Dynamic filtering
- Client-side aggregation
- Interactive charts
- Dynamic insight generation
- Theme switching

The dashboard uses Chart.js for the visual analytics layer. fileciteturn0file0L1-L8

### Interactive analytical flow

**Select Filters → Recalculate Dataset → Update KPIs → Update Charts → Update Tables → Recalculate Insights**

This makes the dashboard suitable for exploratory analysis rather than being limited to static reporting.

---

## 12. Tools & Techniques

### Tools

- Microsoft Excel
- Excel data cleaning and organization
- HTML
- CSS
- JavaScript
- Chart.js

### Analytics Techniques

- Data cleaning
- Data standardization
- Duplicate validation
- Missing-value validation
- KPI development
- Gross profit analysis
- Gross margin analysis
- Trend analysis
- YoY analysis
- Seasonality analysis
- Geographic analysis
- Product analysis
- Customer analysis
- Channel analysis
- Payment-method analysis
- Pricing and discount analysis
- Interactive dashboard development
- Dynamic business insights

---

## 13. Project Outcome

This project transforms a **30,000-order global sports footwear dataset** into a structured analytics solution combining Excel data preparation with an interactive web dashboard.

The final solution provides:

**Raw Transactions → Clean Analytical Dataset → Calculated KPIs → Interactive Dashboard → Trend & Portfolio Analysis → Pricing Analysis → Business Insights → Recommendations**

The project demonstrates practical capabilities in:

- Excel data analytics
- Data cleaning
- Business KPI development
- Profitability analysis
- Interactive dashboard development
- JavaScript data visualization
- Commercial pricing analysis
- Product and market analytics
- Business storytelling

---

## 14. Repository Description

**End-to-end Global Sports Footwear Sales Analytics project featuring 30K orders, cleaned Excel data, an interactive HTML dashboard, KPI analysis, profitability insights, pricing analysis, product performance, geography, customer trends, and business recommendations.**

---

## 15. Project Highlights

- **30,000** global footwear orders
- **2018–2026** data coverage
- **6** brands
- **5** product categories
- **899** footwear models
- **6** countries
- **2** sales channels
- **4** payment methods
- **3** gender segments
- **6** discount tiers
- **75,006** units sold
- **$9.081M** Net Sales
- **$3.841M** Gross Profit
- **42.3%** Gross Margin
- Interactive filters
- Dynamic KPI cards
- Multi-section HTML dashboard
- Pricing and discount analytics
- Product and geographic analysis
- Automated business insights
- Responsive light/dark dashboard theme
