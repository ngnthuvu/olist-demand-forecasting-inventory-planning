\# Data Dictionary



\## forecast\_summary.csv



| Column | Description |

|---|---|

| category | Product category |

| demand\_class | Demand pattern classification |

| forecast\_risk | Forecast risk level |

| avg\_demand | Average demand in test period |

| mae\_ma | MAE for Moving Average |

| mae\_wma | MAE for Weighted Moving Average |

| mae\_es | MAE for Exponential Smoothing |

| mape\_ma | MAPE for Moving Average |

| mape\_wma | MAPE for Weighted Moving Average |

| mape\_es | MAPE for Exponential Smoothing |

| bias\_ma | Bias for Moving Average |

| bias\_wma | Bias for Weighted Moving Average |

| bias\_es | Bias for Exponential Smoothing |

| best\_by\_mae | Forecast method with lowest MAE |

| best\_mae | Lowest MAE among compared methods |

| best\_mape | MAPE of the best method |

| best\_bias | Bias of the best method |

| bias\_concern\_flag | Whether bias exceeds threshold |

| avg\_lead\_time | Average total lead time |

| lead\_time\_stddev | Lead time variability |

| otd\_rate | On-time delivery rate |

| freight\_ratio | Freight cost relative to product price |

| operational\_risk | Operational risk level |

| implied\_min\_safety\_buffer | Lower planning buffer estimate |

| implied\_max\_safety\_buffer | Upper planning buffer estimate |

| final\_recommendation | Final planning action |



\## timeseries\_full.csv



| Column | Description |

|---|---|

| category | Product category |

| period\_start | First day of the month |

| year\_month | Year-month period |

| set\_flag | Train or test period |

| actual\_quantity | Actual monthly demand measured by order item count |

| actual\_revenue | Monthly product revenue |

| order\_count | Number of unique orders |

| avg\_item\_price | Average item price |

| total\_freight | Total freight value |

| avg\_freight\_value | Average freight value |

| freight\_ratio | Freight value divided by product price |

| ma\_forecast | Moving Average forecast |

| wma\_forecast | Weighted Moving Average forecast |

| es\_forecast | Exponential Smoothing forecast |



\## ops\_metrics.csv



| Column | Description |

|---|---|

| category | Product category |

| period\_start | First day of the month |

| year\_month | Year-month period |

| avg\_processing\_days | Average days from purchase to carrier handoff |

| avg\_delivery\_days | Average days from carrier handoff to customer delivery |

| avg\_total\_lead\_time | Average days from purchase to customer delivery |

| lead\_time\_stddev | Standard deviation of total lead time |

| otd\_rate | Percentage of orders delivered on or before estimated delivery date |

| avg\_freight\_value | Average freight value |

| avg\_item\_price | Average item price |

| freight\_ratio | Freight value divided by product price |

| order\_count | Number of unique orders |

| item\_count | Number of order items |

| same\_state\_rate | Percentage of orders where seller and customer are in the same state |



\## error\_metrics.csv



| Column | Description |

|---|---|

| category | Product category |

| period\_start | First day of the month |

| year\_month | Year-month period |

| actual\_quantity | Actual monthly demand |

| ma\_forecast | Moving Average forecast |

| wma\_forecast | Weighted Moving Average forecast |

| es\_forecast | Exponential Smoothing forecast |

| ma\_error | Actual demand minus MA forecast |

| wma\_error | Actual demand minus WMA forecast |

| es\_error | Actual demand minus ES forecast |

| ma\_abs\_error | Absolute MA error |

| wma\_abs\_error | Absolute WMA error |

| es\_abs\_error | Absolute ES error |

| ma\_abs\_pct\_error | Absolute percentage error for MA |

| wma\_abs\_pct\_error | Absolute percentage error for WMA |

| es\_abs\_pct\_error | Absolute percentage error for ES |



\## ts\_quality\_check.csv



| Column | Description |

|---|---|

| category | Product category |

| periods\_total | Number of months in the time series |

| avg\_demand | Average monthly demand |

| stddev\_demand | Standard deviation of monthly demand |

| cv | Coefficient of variation |

| zero\_periods | Number of months with zero demand |

| zero\_pct | Percentage of months with zero demand |

| high\_cv\_flag | Whether CV exceeds threshold |

| intermittent\_flag | Whether zero-demand percentage exceeds threshold |

| demand\_class | Demand pattern classification |

| forecast\_risk | Forecast risk level |

