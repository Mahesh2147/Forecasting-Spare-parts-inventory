# Forecasting-Spare-parts-inventory

## 🎯 Project Goal & Domain Analysis
	
  * Business Case: Analyzing service order data to build a time series forecasting model.
	
  * Objective: Forecast the demand for service parts based on historical order data.

## 📚 Data Exploration & Preprocessing
	
  * Dataset Name: service_data.csv
	
  * Rows & Columns: 28,482 records with 7 columns
	
  * Key Columns Analyzed:
		
    * invoice_date and job_card_date (converted to datetime)
		
    * vehicle_model and invoice_line_text (categorical columns)
	
  * Data Cleaning Steps:
		
    * Dropped missing and duplicate records
		
    * Created a new feature: Orders_on_Demand to identify rows with orders

## 📊 Exploratory Data Analysis (EDA)
	
  * Visualization Highlights:
		
    * Count plots for vehicle_model and business_partner_name
		
    * Barplots comparing models and invoice text frequencies
		
    * Time series plot of daily order counts

## ⏰ Time Series Analysis
	
  * Stationarity Check:
		
    * Dickey-Fuller Test confirms data is stationary (p-value < 0.05).
	
  * Seasonal-Trend Decomposition:
		
    * Trend and seasonality components visualized using STL decomposition.
		
    * Autocorrelation (ACF) and Partial Autocorrelation (PACF) plots indicate lag patterns.

## 📡 Model Building & Evaluation
	
  * Models Implemented:
		
    * AR Model (AutoRegressive)
		
    * MA Model (Moving Average)
		
    * ARMA Model
		
    * ARIMA Model
		
    * SARIMA Model (Seasonal ARIMA)
		
    * Auto ARIMA for Best Hyperparameters
	
  * Model Evaluation:
		
    * Metrics Used: Mean Squared Error (MSE) & Root Mean Squared Error (RMSE)
		
    * Best Model: SARIMA with Auto ARIMA performed best with lowest AIC and RMSE.


## 🏆 Model Performance Summary
```
* Model          	          RMSE Score

* AR Model	                    30.63

* MA Model	                    33.11

* ARMA Model	                35.31

* ARIMA Model	                35.90

* ARIMA with Best Parameters	30.16

* SARIMA	                    35.11

* SARIMA with Best Parameters   30.85
```
## 🚩 Challenges Faced
	
  * Data Quality: Dealing with missing and duplicate records.
	
  * Model Tuning: Identifying the best p, d, q values using Auto ARIMA.
	
  * Stationarity Issues: Ensuring time series data is stationary before applying models.

## 🔚 Conclusion
	
  * The SARIMA model using auto-tuned parameters provided the most accurate forecasting results. Further 	optimization may improve the model.
