# 🦠 COVID-19 Forecasting Project | Time Series & Regression Modeling

![image](https://github.com/user-attachments/assets/450aa5d4-a596-4bdb-94dd-afe508f69310)

## 📝 Overview

This project leverages **machine learning and time series forecasting** techniques to model and predict COVID-19 case trends. It explores the performance of various models including:

- **Linear Regression**
- **Decision Tree Regression**
- **Random Forest Regression**
- **ARIMA (AutoRegressive Integrated Moving Average)**

The primary goal is to identify the most accurate forecasting method to predict short-term case numbers and inform better **public health decision-making** and **resource allocation**.

## 📦 Dataset Source

- **📊 Johns Hopkins University COVID-19 Repository**
- **🌍 World Health Organization (WHO)**
- **🔗 Country Mapping Data:**  
[Kaggle Country Mapping](https://www.kaggle.com/andradaolteanu/country-mapping-iso-continent-region)  
[Kaggle COVID-19 Dataset](https://www.kaggle.com/antgoldbloom/covid19-data-from-john-hopkins-university)

## 🛠 Technologies Used

![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge)
![Pmdarima](https://img.shields.io/badge/pmdarima-00599C?style=for-the-badge)

## 🎯 Objectives

- Clean and preprocess time series COVID-19 case data
- Apply regression models to forecast case numbers
- Evaluate model performance using R² score
- Visualize trends and predictions to interpret results
- Identify the best-performing model for forecasting

## 🔬 Methodology

1. **Data Cleaning & Aggregation**
   - Summed daily case data by country
   - Mapped country alpha codes for choropleth visualization
2. **Exploratory Data Analysis**
   - Used `.describe()`, `.info()`, and `.head()` for summary insights
   - Created choropleth maps for global case density
3. **Trend Visualization**
   - Time-series plots for daily cases and deaths
   - Applied moving average smoothing for clarity
4. **Model Building**
   - Fitted ARIMA using `auto_arima` from `pmdarima`
   - Trained linear, decision tree, and random forest regressors
   - Applied `train_test_split` and evaluated with `r2_score`.

## 📈 Results

| Model                    | R² Score  | Description                                        |
|-------------------------|-----------|----------------------------------------------------|
| Linear Regression        | -0.0111   | Poor fit; underperformed baseline                  |
| Decision Tree Regression | 0.3759    | Moderate performance                               |
| Random Forest Regression | **0.4177** | Best performing model on test set                 |
| ARIMA                    | 0.0030    | Poor prediction accuracy for daily case series     |

📌 **Random Forest Regression** proved most effective for modeling the non-linear COVID-19 trends.

## 🔍 Model Comparison

- **Linear Regression:** Failed to capture data complexity
- **Decision Tree:** Somewhat captured daily spikes
- **Random Forest:** Generalized well and captured daily fluctuations
- **ARIMA:** Underfit due to high noise and seasonality

## 📊 Forecasting Visualization

- Forecasted next 30 days using the trained **Random Forest Regressor**
- Visualized predictions alongside historical data

🖼️ Output:
- Blue Line: Actual cases from last 30 days
- Red Dashed Line: Predicted case trend for next 30 days

> This enables **short-term forecasting** and preparation for resource planning.

## 🔮 Future Scope

- Include vaccination rates and mobility metrics
- Expand time horizon and retrain on newer data
- Use deep learning models (LSTM, Prophet)
- Publish real-time dashboard for visualization

🚀 **Accurate forecasting can save lives — data driven models help prepare for tomorrow.**
