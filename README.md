# DataCo Supply Chain — Dashboard Project

A multi-page analytics dashboard built on the **DataCo Smart Supply Chain** dataset (18,000 order
line items, 2015–2017), exploring both **operational performance** (delivery, shipping, order
status) and **statistical analysis** (distributions, correlations, trends).

This repo contains working HTML/Chart.js prototypes used to design the layout and chart selection
before building the final dashboards in Power BI.

---

## Project status

| Dashboard | Status |
|---|---|
| **Operations Dashboard** | ✅ Complete |
| **Statistical Analysis Dashboard** |  In progress |

---

## 1. Operations Dashboard

Split into two pages for clarity — process/delivery datail on one page, commercial/sales detail
on the other.

### Page 1 — Order & Delivery Performance Overview
`

Focus: is the operation running well?

- KPI row: Total Orders, Total Sales, Profit Margin, Late Delivery Rate, canceled order rate
- Delivery outcome by shipping mode (100% stacked column)
- Scheduled vs. actual shipping days (grouped bar)
- Choropleth map — late delivery rate by region
- Order volume share by shipping mode (donut)
- Order status mix (grouped: Healthy / In-progress / At-risk)

### Page 2 — Sales, Profitability & Regional Detail


Focus: where is the money, and who are the customers?

- KPI row: Total Sales, Total sales without discount, Discount rate, Top Department
- Bubble map — sales by region
- Department performance — sales vs. profit margin (combo chart)
- Sales by customer segment (donut)
- Regional performance summary table (with status badges)

---

## 2. Statistical Analysis Dashboard

In progress —  covering descriptive statistics
(distributions, spread, summary stats) and inferential statistics (correlations, relationships,
time trends). Final version will be built out in Power BI.

---
## 📸 Previews

### 1. Order & Delivery Performance
![Order & Delivery Performance](images/Order%20&%20Delivery%20Performance_dashboard.jpeg)

### 2. Sales Profitability & Regional Detail
![Sales Profitability & Regional Detail](images/Sales%20Profitability%20&%20Regional%20Detail_dashboard.jpeg)

### 3. Star Schema Data Model
![Star Schema Model View](images/Star_schema_model_view.jpeg)

---
## Tech stack

- **Power BI Desktop** — target platform for the final production dashboards
- **DAX** — measures for Power BI `

---

## Data model

Star schema with one fact table and supporting dimensions:

```
FACT_Orders ──< DIM_Customers (Customer ID)
            ──< DIM_Products  (Product Card ID)
            ──< DIM_Date      (Order Date)
            ──< DIM_Geography (Order Region)
            ──< DIM_Order(Order ID)

---

## Roadmap

- [x] Operations dashboard — Order & Delivery Performance Overview
- [x] Operations dashboard — Sales, Profitability & Regional Detail
- [x] Operations dashboard — choropleth + bubble map design
- [ ] Statistical dashboard — descriptive statistics page
- [ ] Statistical dashboard — inferential statistics & trends page
- [ ] Power BI `.pbix` file with both dashboard sets, slicers synced across pages
- [ ] Published report link (Power BI Service)

---

## License / Data source

Dataset: DataCo Smart Supply Chain (publicly available sample dataset, used for educational and
portfolio purposes).
