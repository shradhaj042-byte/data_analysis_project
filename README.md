# BharatKart — India E-Commerce Sales & Customer Analytics

A complete, end-to-end Python data analytics case study built on a synthetic but statistically
realistic Indian e-commerce transaction log (Jan 2024 – Dec 2025). The project covers data
cleaning, exploratory data analysis, geographic/map analysis, and business recommendations —
delivered as a Jupyter notebook, a Word report, and a PowerPoint presentation.

## Headline numbers

| Metric | Value |
|---|---|
| Total orders | 13,522 |
| Total sales | ₹110.2M |
| Total profit | ₹7.3M |
| Profit margin | 6.63% |
| Unique customers | 3,021 |
| States / Cities covered | 17 / 25 |
| Avg. order value | ₹8,148 |
| Avg. delivery time | 3.95 days |

## Project files

| File | Description |
|---|---|
| `project_final.ipynb` | The full analysis notebook — data cleaning, EDA, geographic analysis, and conclusions, with all outputs pre-executed and rendered inline. |
| `BharatKart_Ecommerce_Analytics_Report.docx` | 16-page written report: executive summary, KPIs, all findings, maps, and recommendations. |
| `BharatKart_Ecommerce_Analytics_Presentation.pptx` | 17-slide stakeholder presentation covering the same analysis in a boardroom-ready format. |
| `clean_sales_ecommerce.csv` | The cleaned dataset (13,522 rows × 29 columns) used throughout the analysis. |
| `india_states.geojson` | Public-domain Indian state boundary file used to render the offline maps (no API key required). |
| `chart_*.png` | Every chart used in the report/deck, exported individually. |
| `state_sales_summary.csv`, `top_cities_by_sales.csv`, `bottom_cities_by_sales.csv` | Supporting aggregation tables behind the geographic analysis. |

## How to run the notebook

```bash
pip install pandas numpy matplotlib seaborn geopandas shapely mapclassify jupyter
jupyter notebook project_final.ipynb
```

The notebook is self-contained: the geographic-analysis section reloads
`clean_sales_ecommerce.csv` directly, so it can be re-run independently of the earlier cleaning
cells. `india_states.geojson` must sit in the same folder as the notebook.

## Analysis structure

1. **Data Collection** — loading the raw transactional log.
2. **Data Cleaning** — null/duplicate removal, type fixes, text standardisation, outlier
   removal (13,522 valid rows retained).
3. **Exploratory Data Analysis** — category, region, state, product, payment-method,
   order-status, and time-series breakdowns.
4. **Geographic / Map-Based Analysis** *(new)* — three offline maps built with GeoPandas:
   - State-wise sales choropleth
   - City-wise sales-volume & profit-margin bubble map
   - Regional (North/South/East/West/Central) classification map
5. **Conclusion & Business Recommendations** — six actionable recommendations tied directly
   to the findings above.

## Key findings

- **Electronics** drives the most revenue (₹54.9M, 49.8% of sales) despite **Fashion** having
  the highest order count — Electronics carries a much higher average order value.
- **Maharashtra** is the single largest state market (₹24.9M); five states account for a
  disproportionate share of national sales.
- **UPI** dominates payment method share at 39.7%, reflecting India's digital-payments shift.
- **85.8%** of orders are delivered successfully; a **5.7%** return rate is worth investigating.
- Geographically, **Tier-2 cities like Lucknow and Hyderabad post stronger profit margins**
  (7.5–7.8%) than high-volume metros like Mumbai (6.0%) — a volume-vs-margin trade-off.
- Festive-season months (Sep–Nov) show revenue peaks paired with **margin compression**,
  indicating heavy seasonal discounting.

## Recommendations

1. Protect the core five states while investing in East/North for diversification.
2. Re-price or re-bundle high-revenue, low-margin electronics SKUs.
3. Lean into Tier-2 city profitability (Lucknow, Hyderabad, Pune).
4. Investigate the 5.7% return rate, especially in Fashion and Electronics.
5. Cap festive-season discount depth to protect margin.
6. Extend UPI-first payments and EMI options on high-ticket categories.

## Tech stack

Pandas · NumPy · Matplotlib · Seaborn · GeoPandas · Jupyter Notebook

---
*Data Analytics Project — prepared September 2026.*


