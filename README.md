\# Forecasting Spare Parts Inventory



\## Data Science Project



\*\*Client:\*\* NewX Services  

\*\*Project Category:\*\* Forecasting Spare Parts Inventory  

\*\*Project Reference:\*\* PM-PR-0027



\---



\## Project Overview



This project focuses on forecasting spare parts demand for service centres of NewX Services.



Inventory management is a major challenge for service centres because maintaining excess spare parts increases inventory holding costs, while insufficient inventory can result in spare parts availability problems.



The objective of this project is to develop a predictive time-series forecasting model that can help service centres estimate future spare parts demand and support Just-in-Time (JIT) inventory management.



\---



\## Business Problem



Service centres need to maintain sufficient spare parts to meet customer requirements. However, maintaining too much inventory increases costs, while maintaining insufficient inventory can lead to stock shortages.



Accurate demand forecasting can help service centres make better inventory planning and replenishment decisions.



\---



\## Project Goal



The primary goal of this project is to:



> Create a predictive model for inventory forecasting so that service centres can achieve Just-in-Time (JIT) inventory standards.



\---



\## Dataset



The project uses historical service data containing \*\*28,484 records\*\* and \*\*7 features\*\*.



\### Features



| Feature | Description |

|---|---|

| Invoice Date | Date associated with the invoice |

| Job Card Date | Date associated with the service/job card |

| Business Partner Name | Business partner information |

| Vehicle No. | Vehicle identification number |

| Vehicle Model | Vehicle model information |

| Current KM Reading | Current kilometre reading |

| INVOICE LINE TEXT | Invoice/spare-parts line description |



\---



\## Project Workflow



```text

Data Collection

&#x20;     ↓

Data Understanding

&#x20;     ↓

Data Cleaning \& Preprocessing

&#x20;     ↓

Exploratory Data Analysis

&#x20;     ↓

Weekly Spare Parts Demand Aggregation

&#x20;     ↓

Train / Test Split

&#x20;     ↓

ARIMA Model

&#x20;     ↓

SARIMAX Model

&#x20;     ↓

SARIMAX Hyperparameter Tuning

&#x20;     ↓

Model Evaluation

&#x20;     ↓

ARIMA vs SARIMAX Comparison

&#x20;     ↓

Best Model Selection

&#x20;     ↓

Full Data Refit

&#x20;     ↓

14-Week Future Forecast

&#x20;     ↓

Forecast Visualization

&#x20;     ↓

Business Interpretation

````



\---



\## Models Used



\### ARIMA



ARIMA was developed as the baseline time-series forecasting model to capture non-seasonal patterns in spare parts demand.



\### SARIMAX



SARIMAX was developed to capture both non-seasonal and seasonal patterns in the weekly spare parts demand.



The SARIMAX model is represented as:



```text

SARIMAX(p,d,q) × (P,D,Q,s)

```



\---



\## Hyperparameter Tuning



Different combinations of SARIMAX parameters were evaluated.



The tuning process was:



```text

Parameter Combinations

&#x20;       ↓

SARIMAX Model Fitting

&#x20;       ↓

Test Data Prediction

&#x20;       ↓

RMSE Calculation

&#x20;       ↓

Model Comparison

&#x20;       ↓

Best Model Selection

```



The best-performing configuration was selected based on forecasting performance and model stability.



\---



\## Model Evaluation



The models were evaluated using:



\* AIC – Akaike Information Criterion

\* MAD – Mean Absolute Deviation

\* MSE – Mean Squared Error

\* RMSE – Root Mean Squared Error

\* MAPE – Mean Absolute Percentage Error



\---



\## ARIMA vs SARIMAX



| Metric |   ARIMA |     SARIMAX |

| ------ | ------: | ----------: |

| AIC    | 404.184 | \*\*346.251\*\* |

| MAD    |   3.937 |   \*\*2.896\*\* |

| MSE    |  21.736 |  \*\*14.309\*\* |

| RMSE   |   4.662 |   \*\*3.783\*\* |

| MAPE   | 28.359% | \*\*23.535%\*\* |



Lower values indicate better performance for the error metrics.



\---



\## Final Model



\### SARIMAX



SARIMAX was selected as the final forecasting model because it achieved better performance than ARIMA across the major evaluation metrics.



The final SARIMAX model achieved:



\* \*\*AIC:\*\* 346.251

\* \*\*MAD:\*\* 2.896

\* \*\*MSE:\*\* 14.309

\* \*\*RMSE:\*\* 3.783

\* \*\*MAPE:\*\* 23.535%



\---



\## Future Forecast



The selected SARIMAX model was used to generate forecasts for the \*\*next 14 weeks\*\*.



The future predictions can support:



\* Spare parts demand planning

\* Inventory replenishment

\* Stock availability

\* Reduction of excess inventory

\* Just-in-Time inventory management



\---



\## Final Conclusion



The project successfully developed a time-series forecasting solution for spare parts inventory planning. ARIMA was initially developed as a baseline model, followed by SARIMAX modelling and hyperparameter tuning.



Based on the evaluation results, SARIMAX performed better than ARIMA, achieving a lower RMSE of \*\*3.783\*\* compared with \*\*4.662\*\* for ARIMA and a lower MAPE of \*\*23.535%\*\* compared with \*\*28.359%\*\*.



Therefore, \*\*SARIMAX was selected as the final forecasting model\*\*. The model can help service centres estimate future spare parts demand and support better inventory planning and Just-in-Time inventory management.



\---



\## Future Scope



Future improvements can include:



\* Forecasting multiple spare parts simultaneously

\* Developing vehicle-model-wise forecasting

\* Including additional business and vehicle-related variables

\* Comparing SARIMAX with machine-learning models

\* Developing an automated forecasting pipeline

\* Creating an inventory forecasting dashboard

\* Implementing automated model retraining

\* Integrating forecasts with inventory replenishment systems







