# EnergySense AI: Electricity Consumption Analysis and Forecasting

## Project Overview

EnergySense AI is a data analysis and machine learning project focused on household electricity consumption.

The project uses a real-world electricity consumption dataset to analyze usage patterns, identify peak hours, compare weekday and weekend consumption, forecast hourly electricity usage, and detect unusual consumption behavior.

## Dataset

The project uses the Individual Household Electric Power Consumption dataset from the UCI Machine Learning Repository.

The dataset contains electricity measurements such as:

- Date and time
- Global active power
- Global reactive power
- Voltage
- Global intensity
- Sub-metering 1
- Sub-metering 2
- Sub-metering 3

## Project Objectives

The main goals of this project are:

- Clean and prepare electricity consumption data
- Analyze daily electricity usage trends
- Identify peak consumption hours
- Compare weekday and weekend usage
- Analyze sub-metering areas
- Estimate other household energy consumption
- Build a forecasting model for hourly electricity consumption
- Detect unusual energy consumption patterns

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Project Workflow

### 1. Data Cleaning

The dataset was cleaned by handling missing values, converting columns to the correct data types, and creating a datetime column from the original date and time columns.

### 2. Feature Engineering

New time-based features were created, including:

- Hour
- Day of week
- Month
- Year
- Weekend status

For forecasting, historical features were also created:

- Previous hour energy consumption
- Previous day same hour energy consumption
- Rolling 24-hour average

### 3. Daily Consumption Analysis

Daily electricity consumption was analyzed to understand how energy usage changes over time.

The highest daily energy consumption was around 79.56 kWh, while the lowest daily energy consumption was around 0.24 kWh.

### 4. Peak Hours Analysis

The analysis showed that the highest average electricity consumption occurs around 8:00 PM, while the lowest average consumption occurs around 4:00 AM.

This can help in understanding peak demand periods.

### 5. Weekday vs Weekend Analysis

The average electricity consumption was higher during weekends compared to weekdays.

- Weekday average consumption: 1.035 kW
- Weekend average consumption: 1.234 kW

This suggests that household activity increases during weekends.

### 6. Sub-Metering Analysis

The analysis showed that Sub_metering_3 had the highest measured energy usage compared to the other sub-metering areas.

Sub_metering_3 represents the water heater and air conditioner, which are usually high-consumption appliances.

### 7. Forecasting Model

A Linear Regression model was built to forecast hourly electricity consumption using time-based and historical features.

Model results:

- Mean Absolute Error: 0.3672 kWh
- R2 Score: 0.5159

The model shows that previous consumption patterns can help predict future energy usage.

### 8. Anomaly Detection

Isolation Forest was used to detect unusual hourly electricity consumption patterns.

The model detected 692 anomalous records out of 34,565 hourly records.

These anomalies may represent unusual energy usage, equipment issues, or abnormal household behavior.

## Conclusion

In this project, I worked on a real household electricity consumption dataset and tried to understand how energy usage changes over time.

I cleaned the data, created new time-based features, and analyzed daily consumption, peak hours, weekday vs weekend usage, and sub-metering areas.

I also built a simple forecasting model to predict hourly electricity consumption and used anomaly detection to identify unusual consumption records.

This project helped me practice data cleaning, data analysis, visualization, machine learning, and applying these skills to an energy-related problem.

## Future Improvements

This project can be improved by:

- Using advanced forecasting models such as Random Forest, XGBoost, ARIMA, Prophet, or LSTM
- Adding weather data such as temperature and humidity
- Building an interactive dashboard using Streamlit or Power BI
- Comparing multiple machine learning models
- Adding electricity cost estimation
- Deploying the model as a web application

## Files in This Repository

- `EnergySense_AI_Analysis.ipynb`  
  Main Jupyter Notebook containing the full analysis and machine learning work.

- `clean_energy_sample.csv`  
  A cleaned sample of the processed dataset.

- `hourly_energy_forecasting_data.csv`  
  Hourly dataset used for forecasting.

## Author

Mohamed Sameh
