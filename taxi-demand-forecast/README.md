# Taxi Demand Forecasting Project

## Project Description

Sweet Lift Taxi company has collected historical data on taxi orders at airports. To attract more drivers during peak hours, the company needs to forecast the number of taxi orders for the upcoming hour. The goal of this project is to develop a predictive model that achieves an RMSE of no more than **48** on the test set.

---

## Table of Contents

- [Technologies and Tools Used](#technologies-and-tools-used)  
- [Project Structure](#project-structure)  
- [Setup Instructions](#setup-instructions)  
- [Usage](#usage)  
- [Conclusion](#conclusion)  
- [Suggestions for Business Improvement](#suggestions-for-business-improvement)

---

## Technologies and Tools Used

- Python  
- Pandas  
- NumPy  
- Matplotlib  
- scikit-learn  
- statsmodels  
- pmdarima  
- CatBoost  

---

## Project Structure

- **Data Preparation**:  
  Resampled raw taxi order data by hour, identified and handled duplicates, filled missing values with backfill.

- **Exploratory Data Analysis (EDA)**:  
  Visualized rolling means, seasonal decomposition, and residuals to identify patterns and outliers.

- **Stationarity Check**:  
  Performed ADF test and differencing; confirmed the data is stationary.

- **Feature Engineering**:  
  Created lag features, time-based features, and rolling averages to support machine learning models.

- **Model Training**:  
  - **Linear Regression**: Achieved an RMSE of **45.49** on the test set  
  - **AutoReg**: RMSE = **55.55**  
  - **MA (ARIMA)**: RMSE = **58.95**  
  - **AutoARIMA**: RMSE = **58.90**

---

## Setup Instructions

Clone the repository to your local machine and then install the required libraries and dependcies via pipinstall.

---
## 🚀 Usage

Run the notebook `taxi-demand-forecast.ipynb` to:

- Load and resample taxi order data by hour
- Analyze trends, seasonality, and stationarity
- Engineer lag and rolling window features
- Train and evaluate multiple models (Linear Regression, AutoReg, ARIMA, AutoARIMA)
- Select the model with the lowest RMSE for deployment

---

## 🧾 Conclusion

Among all models tested:

- **Linear Regression** achieved the best performance with an RMSE of **45.49**.
- Time series models like **AutoReg**, **ARIMA**, and **AutoARIMA** were explored, but none met the RMSE threshold.
- The dataset displayed strong seasonality and a rising trend over time, which informed the modeling approach.
- Despite the presence of duplicate `num_orders` values, data quality was preserved by preserving all entries post-resampling.

---

## 💡 Suggestions for Business Improvement

- **Deploy the Linear Regression model** to begin predicting hourly demand at airports and inform driver availability.
- **Consider hybrid models** or advanced time series techniques to capture long-term patterns with improved accuracy.
- **Integrate real-time weather or event data** to enhance prediction sensitivity during high-variance days.
- **Schedule driver incentives** during predicted peak hours to prevent service gaps and maximize coverage.
- **Re-evaluate model performance monthly** to retrain on new trends and maintain prediction accuracy.
