# time-series-forecasting
#Project Overview

This project is a solution for the Store Sales – Time Series Forecasting competition hosted by Kaggle.
The objective is to accurately forecast daily sales for thousands of product families across different grocery stores in Ecuador, owned by Corporación Favorita.

Through this project, I explored real-world time series forecasting challenges using machine learning techniques such as feature engineering,
lag/rolling statistics, and LightGBM modeling. The final predictions are evaluated using Root Mean Squared Logarithmic Error (RMSLE).

Goal of the Project

To build a predictive model that:
Forecasts sales per store per product family per day
Leverages historical data, promotions, oil prices, holidays, and store metadata
Minimizes RMSLE for more reliable and stable predictions
Can generalize well on unseen test data

# What the Model Does

 Loads and merges all datasets
 Converts dates into rich time-based features (year, month, week, etc.)
 Creates lag features (1, 7, 14, 30 days) to capture past sales trends
 Computes rolling means and standard deviations to capture seasonal behavior
 Adds features for oil prices, holidays, promotion effects, and store clustering
 Encodes categorical features with Label Encoding
 Trains a LightGBM Regressor on log-transformed sales (log1p(sales))
 Produces final predictions and exports a submission.csv file



Forecasting sales helps retailers:

Reduce food waste (especially for perishable items)

Optimize inventory and supply chain management

Increase revenue and customer satisfaction

Move from intuition-based planning to data-driven decisions
