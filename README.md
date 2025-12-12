📊 Time Series Forecasting & Stationarity Analysis — Multi-City Automation

This project is a complete automated time-series analysis pipeline for climate/location-based daily statistics stored in an Excel file.
It performs data cleaning, visualization, stationarity testing, model selection, forecasting, and produces a unified summary report for all cities.

The pipeline uses AR, MA, and ARIMA models, selected using AIC-based criteria.

✨ Key Features
✅ 1. Automated Multi-City Processing
The script processes every location in the dataset automatically:
Loads and sorts data
Extracts time-series for each city
Handles missing values
✅ 2. Exploratory Data Analysis
For each city:
Basic statistics (mean, std, skewness, kurtosis)
Time-series visualization
KDE distribution plot (probability density)
Plots include:
Mean
Median
Mode
✅ 3. Stationarity Tests
Three robust tests are applied:
ADF Test (Dickey-Fuller)
KPSS Test
Kolmogorov–Smirnov (KS) Test split-half distribution test
This helps determine if differencing is needed.
✅ 4. Model Selection & Fitting
Automatically selects optimal lags using AIC:
Best AR(p)
Best MA(q)
Builds ARIMA(p,0,q) model
Each model generates:
Summary statistics
Predictions
10-day ahead forecast plot
MAE (Mean Absolute Error)
✅ 5. Output Summary Report
Exports a consolidated CSV file:
| City | Data Points | ADF | KPSS | KS | Best AR(p) | Best MA(q) | MAE (AR) | MAE (MA) | MAE (ARIMA) |
Saved as:
project_summary.csv
✅ 6. All plots are automatically saved
📁 Project Structure
📦 TimeSeries-Forecasting
│
├── daily_stats_by_location.xlsx   # Input data
├── project_summary.csv            # Output summary
├── city_feature_plots/            # Saved charts (optional)
│
└── time_series_analysis.py        # Main script

🛠️ Technologies Used
Python 3.x
pandas
numpy
seaborn
matplotlib
scipy
statsmodels
