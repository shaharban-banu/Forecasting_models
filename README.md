# 🛒 Retail Demand Forecasting System

## 📌 Project Overview
This project focuses on building a **Retail Demand Forecasting System** using historical weekly sales data.  
The objective is to predict future demand accurately to support **inventory planning, supply chain optimization, and business decision-making**.

Multiple time series forecasting models were implemented and compared to identify the most effective approach for retail demand prediction.

---

## 📂 Dataset Information
- **Source File**: `train.csv`
- **Time Index**: `Date`
- **Target Variable**: `Weekly_Sales`
- **Categorical Dimensions**:
  - `Store`
  - `Dept`
- **External Factor**:
  - `IsHoliday` (captures holiday effects on sales)

Sales were aggregated at the **weekly level** to create a univariate time series for forecasting.

---

## 🔍 Exploratory Data Analysis (EDA)
- Visualized overall **weekly sales trends**
- Identified **seasonality patterns**
- Analyzed the **impact of holidays** on sales

---

## 📈 Time Series Analysis
- Performed **Augmented Dickey–Fuller (ADF) test**
- Confirmed that the time series is **stationary**
- Used **ACF and PACF plots** to determine ARIMA and SARIMA parameters
- Identified strong **yearly seasonality (52 weeks)**

---

## 🤖 Models Implemented

### 1️⃣ ARIMA
- Captures short-term dependencies
- Suitable for stationary time series
- Does not explicitly handle seasonality

### 2️⃣ SARIMA
- Extends ARIMA by modeling **seasonality**
- Well-suited for retail data with yearly patterns

### 3️⃣ Prophet
- Business-friendly forecasting model
- Automatically models trend and seasonality
- Useful for explainability but less precise for this dataset

---

## 📊 Model Evaluation

### 🔢 Evaluation Metrics
- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**

### 📋 Model Performance Comparison

| Model   | MAE | RMSE |
|--------|------|-------|
| ARIMA  | 1,588,545 | 1,892,971 |
| SARIMA | **778,600** | **934,630** |
| Prophet | 8,234,404 | 10,538,570 |

---

## 🏆 Key Results & Insights
- **SARIMA achieved the lowest MAE and RMSE**, making it the most accurate model.
- ARIMA performed reasonably well but struggled with seasonal patterns.
- Prophet significantly underperformed due to the complex seasonal structure of retail sales.
- Yearly seasonality played a **critical role** in forecasting accuracy.

---

## 📌 Business Insights
- Accurate demand forecasting can reduce **overstocking and stockouts**
- Seasonal awareness improves **holiday inventory planning**
- SARIMA is best suited for **operational forecasting**
- Prophet can still be used for **high-level business trend visualization**

---

## ✅ Final Recommendation
- **Primary Model**: SARIMA (for accuracy and seasonality handling)
- **Supporting Model**: Prophet (for explainability and stakeholder reporting)

---

## 🛠️ Technologies Used
- Python
- Pandas, NumPy
- Matplotlib
- Statsmodels (ARIMA, SARIMA)
- Prophet
- Scikit-learn

---

## 🚀 Future Enhancements
- Store-wise and department-wise forecasting
- Incorporating external features (promotions, CPI, fuel prices)
- Deep learning models (LSTM)
- Automated forecasting pipeline

---

## 👤 Author
**Banu**  
_Data Science Student_

---

## 📎 Note
This project demonstrates an end-to-end **time series forecasting workflow**, combining statistical rigor with business relevance.

