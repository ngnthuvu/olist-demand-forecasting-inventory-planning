# Demand Forecasting & Inventory Planning Decision Dashboard

An Excel-based demand planning dashboard using the Olist Brazilian E-Commerce dataset.

This project forecasts monthly demand by product category, evaluates forecast reliability, and combines forecast risk with operational metrics such as lead time, on-time delivery rate, and freight ratio to recommend category-level planning actions.

A Python-DuckDB Colab notebook is also included to replicate the Excel workflow and export clean analysis outputs.

---

## Business Question

Which product categories can be trusted for statistical forecasting, which categories need monthly planner review, and which categories require manual review due to forecast or operational risk?

---

## Tools Used

- Microsoft Excel
- Power Query
- PivotTables & PivotCharts
- Python
- DuckDB
- Google Colab
- pandas
- matplotlib

---

## Project Scope

Dataset: Olist Brazilian E-Commerce Public Dataset

Scope:

- 10 selected product categories
- January 2017 to August 2018
- Forecasting grain: Category × Month
- Train period: January 2017 to February 2018
- Test period: March 2018 to August 2018

Main forecasting methods:

- Moving Average
- Weighted Moving Average
- Exponential Smoothing

Main decision outputs:

- Trust Statistical Forecast
- Forecast + Monthly Override
- Manual Review Required

---

## Dashboard Views

### Analyst View

The Analyst View is designed to diagnose forecast and operational risk.

It helps answer:

- Which categories have high forecast error?
- Which forecasting method performs best by category?
- Is the model under-forecasting or over-forecasting?
- Does demand variability explain forecast error?
- Are lead time and on-time delivery stable enough to support planning?

![Analyst Dashboard 1](dashboard_screenshots/dashboard%20screenshot%201.png)

![Analyst Dashboard 2](dashboard_screenshots/dashboard%20screenshot%202.png)

---

### Manager View

The Manager View is designed to summarize recommended planning actions.

It helps answer:

- How many categories can trust the statistical forecast?
- How many categories require monthly override?
- Which categories require manual review?
- Which categories should planners prioritize?

![Manager Dashboard 1](dashboard_screenshots/dashboard%20screenshot%203.png)

![Manager Dashboard 2](dashboard_screenshots/dashboard%20screenshot%204.png)

![Manager Dashboard 3](dashboard_screenshots/dashboard%20screenshot%205.png)

---

## Colab Automation Extension

The Colab notebook replicates the Excel workflow using Python and DuckDB.

It exports clean output files for validation and documentation:

- `timeseries_full.csv`
- `ops_metrics.csv`
- `forecast_summary.csv`
- `error_metrics.csv`
- `ts_quality_check.csv`

Notebook: `notebooks/Olist_Demand_Forecasting_DuckDB_Colab.ipynb`

---


## Repository Structure

```text
olist-demand-forecasting-inventory-planning/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── excel/
│   └── Excel workbook available upon request / stored separately due to GitHub browser upload size limits.
│
├── notebooks/
│   └── Olist_Demand_Forecasting_DuckDB_Colab.ipynb
│
├── outputs/
│   ├── forecast_summary.csv
│   ├── timeseries_full.csv
│   ├── ops_metrics.csv
│   ├── error_metrics.csv
│   └── ts_quality_check.csv
│
├── figures/
│   ├── actual_vs_forecast.png
│   ├── best_mae_by_category.png
│   ├── planning_action_distribution.png
│   ├── cv_vs_best_mae.png
│   └── otd_rate_by_category.png
│
├── dashboard_screenshots/
│   ├── dashboard screenshot 1.png
│   ├── dashboard screenshot 2.png
│   ├── dashboard screenshot 3.png
│   ├── dashboard screenshot 4.png
│   └── dashboard screenshot 5.png
│
└── docs/
    ├── methodology.md
    └── data_dictionary.md
```

---

## Additional Documentation

Detailed methodology and data definitions are available in:

- [`docs/methodology.md`](docs/methodology.md)
- [`docs/data_dictionary.md`](docs/data_dictionary.md)

---

## Limitations

- Category is used as a SKU proxy because product-level demand is sparse.
- Quantity is measured by order item count, not actual inventory units.
- The dataset does not include live inventory levels, supplier constraints, promotions, or stockout records.
- This project is a demand planning decision dashboard, not an inventory optimization model.

---

## Future Improvements

- Inventory replenishment simulation
- Safety stock and reorder point modeling
- Service level scenario analysis
- Holding cost and stockout cost trade-off analysis

---

## License

This project is licensed under the MIT License.

The original Olist dataset is not owned by this repository. It is used as a public dataset source for educational and portfolio purposes.
