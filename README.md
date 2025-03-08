# **Stock Price Prediction: ARIMA vs. Gradient Boosting**  

## **Overview**  
This project analyzes stock price prediction using two models:  
- **ARIMA (AutoRegressive Integrated Moving Average)** – A traditional time series model.  
- **Gradient Boosting Regressor** – A machine learning model utilizing historical price trends and features.  

The performance of both models is evaluated using **Root Mean Squared Error (RMSE)**, with Gradient Boosting significantly outperforming ARIMA.  

## **Dataset**  
The dataset includes stock prices with features such as:  
- **Open, High, Low, Close prices**  
- **Trading Volume**  
- **Moving Averages (SMA_50, SMA_7, SMA_30)**  
- **Lagged Price Features (Close_Lag_1, Close_Lag_3, Close_Lag_7)**  
- **Daily Percentage Change**  

## **Project Workflow**  
1. **Data Preprocessing**  
   - Handled missing values and formatted date indices.  
   - Created lagged features and moving averages for Gradient Boosting.  

2. **Model Training & Evaluation**  
   - **ARIMA Model:** Used ADF test, differencing, and Auto ARIMA to determine optimal (p, d, q) parameters.  
   - **Gradient Boosting:** Tuned hyperparameters using Grid Search and Time Series Split cross-validation.  

3. **Results & Comparison**  
   - **ARIMA RMSE:** **437** (Struggles with non-linearity and external factors).  
   - **Gradient Boosting RMSE:** **78** (Captures complex patterns better).  

## **Key Findings**  
- **ARIMA** is suitable for simple stationary time series but fails to adapt to rapid market changes.  
- **Gradient Boosting** excels with feature engineering, handling market trends effectively.  
- **Stock markets are non-linear**, making Gradient Boosting a more practical choice.  

## **Technologies Used**  
- **Python (pandas, numpy, matplotlib, seaborn)**  
- **Statsmodels (ARIMA, ADF Test)**  
- **Scikit-learn (Gradient Boosting, Grid Search, Model Evaluation)**  
- **Pmdarima (Auto ARIMA)**  

## **Conclusion**  
Gradient Boosting proves to be the superior model for stock price prediction, effectively leveraging historical data and market trends. ARIMA, while interpretable, lacks adaptability to market volatility. 
