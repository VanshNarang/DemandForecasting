# Demand Forecasting
Predict quantity to be ordered per SKU by forecasting Sales for next month based on this month's data.

## About the Data
The Data can be found in the Excel workbook. There are 2 sheets of importance that were present pre-analysis.
1) 'June Sale' : Sale data for the month of June
2) 'Inventory' : Inventory available as of July 1st.

 Using the Data we are to predict the future inventory requirements so that we can place orders in time and avoid any 'out-of-stock' days.
 
 ## How we Do it?
 
 ### Exponential Smoothing
 
 Exponential smoothing is a rule of thumb technique for smoothing time series data using the exponential window function. Whereas in the simple moving average the past observations are weighted equally, exponential functions are used to assign exponentially decreasing weights over time. It is an easily learned and easily applied procedure for making some determination based on prior assumptions by the user, such as seasonality. Exponential smoothing is often used for analysis of time-series data.
 
 <img src = 'https://wikimedia.org/api/rest_v1/media/math/render/svg/3e907f6034bf9fdf4224ac372adc1e8900d96ff1' align = center>

