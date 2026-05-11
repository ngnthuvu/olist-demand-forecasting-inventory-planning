\# Demand Forecasting \& Inventory Planning Decision Dashboard

An Excel-based demand planning dashboard using the Olist Brazilian E-Commerce dataset.

This project forecasts monthly demand by product category, evaluates forecast reliability, and combines forecast risk with operational metrics such as lead time, on-time delivery rate, and freight ratio to recommend category-level planning actions.

A Python-DuckDB Colab notebook is also included to replicate the Excel workflow and export clean analysis outputs.

\---
\## Business Question
Which product categories can be trusted for statistical forecasting, which categories need monthly planner review, and which categories require manual review due to forecast or operational risk?
\---

\## Tools Used

\- Microsoft Excel
\- Power Query
\- PivotTables \& PivotCharts
\- Python
\- DuckDB
\- Google Colab
\- pandas
\- matplotlib
\---

\## Project Scope
Dataset: Olist Brazilian E-Commerce Public Dataset
Scope:
\- 10 selected product categories
\- January 2017 to August 2018
\- Forecasting grain: Category × Month
\- Train period: January 2017 to February 2018
\- Test period: March 2018 to August 2018

Main forecasting methods:

\- Moving Average
\- Weighted Moving Average
\- Exponential Smoothing

Main decision outputs:

\- Trust Statistical Forecast
\- Forecast + Monthly Override
\- Manual Review Required

\---

\## Dashboard Views
\### Analyst View
The Analyst View is designed to diagnose forecast and operational risk.
It helps answer:
\- Which categories have high forecast error?
\- Which forecasting method performs best by category?
\- Is the model under-forecasting or over-forecasting?
\- Does demand variability explain forecast error?
\- Are lead time and on-time delivery stable enough to support planning?

!\[Analyst Dashboard 1](dashboard\_screenshots/dashboard%20screenshot%201.png)

!\[Analyst Dashboard 2](dashboard\_screenshots/dashboard%20screenshot%202.png)

\---

\### Manager View
The Manager View is designed to summarize recommended planning actions.
It helps answer:
\- How many categories can trust the statistical forecast?
\- How many categories require monthly override?
\- Which categories require manual review?
\- Which categories should planners prioritize?

!\[Manager Dashboard 1](dashboard\_screenshots/dashboard%20screenshot%203.png)

!\[Manager Dashboard 2](dashboard\_screenshots/dashboard%20screenshot%204.png)

!\[Manager Dashboard 3](dashboard\_screenshots/dashboard%20screenshot%205.png)

\---

\## Colab Automation Extension
The Colab notebook replicates the Excel workflow using Python and DuckDB.
It exports clean output files for validation and documentation:
\- `timeseries\_full.csv`
\- `ops\_metrics.csv`
\- `forecast\_summary.csv`
\- `error\_metrics.csv`
\- `ts\_quality\_check.csv`

Notebook:

```text
notebooks/Olist\_Demand\_Forecasting\_DuckDB\_Colab.ipynb
Sample Figures
Forecast Error by Category
Planning Action Distribution
Demand Variability vs Forecast Error
Repository Structure
olist-demand-forecasting-inventory-planning/
│
├── README.md
│
├── excel/
│   └── Excel workbook available upon request / stored separately due to GitHub browser upload size limits.
│
├── notebooks/
│   └── Olist\_Demand\_Forecasting\_DuckDB\_Colab.ipynb
│
├── outputs/
│   ├── forecast\_summary.csv
│   ├── timeseries\_full.csv
│   ├── ops\_metrics.csv
│   ├── error\_metrics.csv
│   └── ts\_quality\_check.csv
│
├── figures/
│   ├── actual\_vs\_forecast.png
│   ├── best\_mae\_by\_category.png
│   ├── planning\_action\_distribution.png
│   ├── cv\_vs\_best\_mae.png
│   └── otd\_rate\_by\_category.png
│
├── dashboard\_screenshots/
│   ├── dashboard screenshot 1.png
│   ├── dashboard screenshot 2.png
│   ├── dashboard screenshot 3.png
│   ├── dashboard screenshot 4.png
│   └── dashboard screenshot 5.png
│
└── docs/
&#x20;   ├── methodology.md
&#x20;   └── data\_dictionary.md
Additional Documentation
Detailed methodology and data definitions are available in:
docs/methodology.md
docs/data\_dictionary.md

Limitations
Category is used as a SKU proxy because product-level demand is sparse.
Quantity is measured by order item count, not actual inventory units.
The dataset does not include live inventory levels, supplier constraints, promotions, or stockout records.
This project is a demand planning decision dashboard, not an inventory optimization model.
Future Improvements
Inventory replenishment simulation
Safety stock and reorder point modeling
Service level scenario analysis
Holding cost and stockout cost trade-off analysis

## License
This project is licensed under the MIT License.
The original Olist dataset is not owned by this repository. It is used as a public dataset source for educational and portfolio purposes.
