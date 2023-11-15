# Forecasting-Pharma-Bounce-Rate

## Steps involved 

### Importing Libraries 
  - The code starts by importing necessary libraries like pandas, numpy, stats models, dtale, matplotlib, etc. These libraries are commonly used for data manipulation, visualization, and time series analysis.

### Reading Data
  - The code reads data from an Excel file named "Projectfinaldata.xlsx" using pandas and stores it in a DataFrame called "data."

### Data Exploration
  - The code then performs some data exploration steps like checking for duplicates in the data and removing them. It also checks for missing values and drops rows with missing values.

### Data Preprocessing
  - The code converts the "Dateofbill" column from an object (string) to a datetime format and sorts the data based on the date.

### Auto EDA using dtale 
  - The code uses the dtale library to create an interactive web-based exploratory data analysis (EDA) dashboard for the preprocessed data. This helps in understanding the data visually.

### Time Series Analysis
  - The code focuses on time series analysis for the top 5 drugs in the dataset.

### Top 5 drugs
  - "SODIUM CHLORIDE IVF 100ML", 
  - "SEVOFLURANE 99.97%",
  -  "SODIUM CHLORIDE 0.9%",
  -  "ONDANSETRON 2MG/ML" and
  -  "MULTIPLE ELECTROLYTES 500ML IVF"  

### Resample
  - Data is converted into monthly segments.

### Decomposition
  - It decomposes the time series data for each drug using the seasonal decompose function from stats models. The decomposition helps in understanding the trend, seasonality, and residual components of the time series.

### Autocorrelation and Partial Autocorrelation (ACF and PACF) Plots: 
  - The code plots the ACF and PACF plots to determine the order of the Autoregressive (AR) and Moving Average (MA) components for each drug's time series.

### Auto ARIMA Model: 
  - The code uses the pmdarima library to automatically find the best ARIMA model for each drug's time series based on the AIC (Akaike Information Criterion) values.

### Model Fitting and Forecasting: 
  - The code fits the ARIMA models to each drug's time series data and makes future predictions for the next 12 months.
### Model Evaluation: 
  -  The code calculates the Mean Absolute Percentage Error (MAPE) to evaluate the accuracy of the ARIMA models on the test data.
### Saving and Loading Models
  - The code saves the trained ARIMA models for each drug using the save method from stats models. Later, it loads these models for making future predictions.
### Final Forecasting
  - The code uses the saved models to make predictions for the next 12 months for each drug.
