# Weather-Wizard

This is a project to forecast the temperature of Delhi using time series analysis. The dataset used is the Delhi Weather dataset, which contains weather information collected every hour from 1996 to 2017.


# Usage
Open delhi-weather-forecasting.ipynb in Jupyter Notebook.

Run the code cells in the notebook to perform data analysis, time series analysis, and forecasting.

# Approach
1.Load the necessary libraries such as pandas, numpy, seaborn, matplotlib, warnings, and other required libraries for time series analysis.

2.Load the Delhi weather dataset using pandas read_csv function.

3.Analyze the dataset by checking the first 5 and last 5 records, rename the required columns, check for duplicates, and convert the datetime column to the datetime format.

4.Set the datetime_utc column as the index column of the dataset.

5.Check for missing values using the heatmap from seaborn and the matrix from missingno libraries. Fill the missing values using forward fill method.

6.Perform exploratory data analysis by checking the frequency distribution of weather conditions and plotting the data.

7.Perform time series analysis by resampling the dataset with the frequency of one day and fill the missing values with the mean value of the temperature column.

8.Plot the data and check for stationarity by plotting the rolling mean and standard deviation and conducting the Dickey-Fuller test. If the p-value is less than the significance level, then the dataset is stationary, and no further differencing is required.

9.Plot the Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF) to identify the orders of the ARIMA model.

10.Fit the ARIMA model to the dataset and predict the temperature for the next n number of days.

11.Evaluate the model using the mean squared error (MSE) and root mean squared error (RMSE).

12.Visualize the predicted values along with the actual values using matplotlib.

# Results
The time series analysis showed that the temperature data is stationary, and therefore, an ARIMA model with d=0 can be used for forecasting. The ACF and PACF plots were used to determine the p and q values for the ARIMA model.

The forecasted temperatures for the next 30 days were then plotted using the ARIMA model. The forecast showed that the temperature is expected to fluctuate between 10°C to 30°C over the next 30 days.

