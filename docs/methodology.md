\# Methodology



\## 1. Data Preparation



The raw Olist CSV files were cleaned and joined into a delivered order-item mart.



Main joins:



\- order items joined with orders by `order\_id`

\- products joined by `product\_id`

\- category translation joined by `product\_category\_name`

\- customers joined by `customer\_id`

\- sellers joined by `seller\_id`



Only delivered orders from January 2017 to August 2018 were included.



\## 2. Time-Series Grain



The forecasting grain is Category × Month.



Product-level forecasting was avoided because product-level demand is too sparse for reliable time-series modeling in this dataset.



\## 3. Forecasting Methods



Three forecasting methods were applied:



\- Moving Average

\- Weighted Moving Average

\- Exponential Smoothing



The models were evaluated on the test period from March 2018 to August 2018.



\## 4. Error Metrics



Forecast performance was evaluated using:



\- MAE

\- MAPE

\- Bias



Positive bias means actual demand was higher than forecast, indicating under-forecasting risk.



Negative bias means forecast was higher than actual demand, indicating over-forecasting risk.



\## 5. Operational Risk



Operational risk was assessed using:



\- average lead time

\- lead time variability

\- on-time delivery rate

\- freight ratio



\## 6. Planning Recommendation



Each category was assigned one of three planning actions:



\- Trust Statistical Forecast

\- Forecast + Monthly Override

\- Manual Review Required



The recommendation combines demand class, forecast risk, bias concern, and operational risk.

