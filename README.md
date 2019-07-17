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
<p align='center'>
 <img src = 'https://wikimedia.org/api/rest_v1/media/math/render/svg/3e907f6034bf9fdf4224ac372adc1e8900d96ff1' align = center>
 </p>
 
 where α is the smoothing factor, and 0 < α < 1. In other words, the smoothed statistic st' is a simple weighted average of the current observation xt and the previous smoothed statistic st−1. The term smoothing factor applied to α here is something of a misnomer, as larger values of α actually reduce the level of smoothing, and in the limiting case with α = 1 the output series is just the current observation. Simple exponential smoothing is easily applied, and it produces a smoothed statistic as soon as two observations are available.
 
 We consider a smoothing factor(α) of 0.7.  The smoothing factor is choosen on the higher side because we want the actual sales from previous month to have a higher impact on the predictions than the previously predicted value. 
 
 ### Why shall we weigh old sales data higher than recent prediction?
 
 The nature of the data is such that a substantial amount of SKUs have sale of 1-2 a day and spreaded at unequal intervals with a total sale amounting to <10 for the month. In such a scenario, had we taken a lower α, the predictions would have gone substantially down for those cases (maybe even 0 for a few) which would've been inaccurate and would've led to 'out of stock' days as we wouldn't reorder enough stock for the small demand. 
 
 

 

