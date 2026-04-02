# Smart-Mobility-Demand-Prediction
End-to-end machine learning project for bike demand prediction using EDA, feature engineering, regression modeling, and validation. Includes business insights and data-driven strategies for optimizing fleet allocation, pricing, and operations based on weather, seasonality, and user behavior

# 🚴‍♂️ Bike Sharing Demand Prediction & Business Insights

## 📌 Overview
This project analyzes a bike-sharing dataset to understand demand patterns and build a predictive model using Linear Regression. The goal is to identify key factors influencing bike rentals and derive actionable business insights.

---

## 🎯 Objectives
- Perform Exploratory Data Analysis (EDA)
- Identify key factors affecting bike demand
- Build a regression model to predict bike rentals (`cnt`)
- Validate model assumptions
- Generate business insights & strategies

---

## 📊 Dataset Description
The dataset contains daily bike rental data with features such as:
- 🌡️ Temperature (`temp`, `atemp`)
- 💧 Humidity (`hum`)
- 💨 Windspeed (`windspeed`)
- 🌦️ Weather situation (`weathersit`)
- 📅 Date, month, weekday
- 👥 Casual & registered users
- 🎯 Target: Total rentals (`cnt`)

---

## 🔍 Exploratory Data Analysis (EDA)
- Distribution plots for numerical features
- Boxplots for categorical variables vs demand
- Correlation heatmap
- Pairplot for feature relationships

### Key Findings:
- Temperature strongly influences demand
- Bad weather reduces usage significantly
- Demand varies across seasons and months

---

## ⚙️ Data Preprocessing
- Converted categorical variables (month, weekday, weather)
- Created dummy variables
- Removed multicollinearity (`temp`, `casual`, `registered`)
- Feature scaling using MinMaxScaler
- Train-test split (70:30)

---

## 🧠 Feature Selection
- Recursive Feature Elimination (RFE)
- Statistical significance (p-values)
- Variance Inflation Factor (VIF)

### Final Features:
- yr, atemp, windspeed, season_spring, mnth_Jul, weathersit_C


---

## 📈 Model Building
- Linear Regression (Statsmodels & Sklearn)
- Multiple models compared:
  - 15 features
  - 7 features
  - 6 features (final optimized)

---

## 📊 Model Performance

| Model | R² Score | Remarks |
|------|--------|--------|
| Full Model | ~0.85 | High complexity |
| Reduced Model | ~0.81 | Best balance |
| Final Model | ~0.79 | Simple & stable |

---

## 🔍 Model Diagnostics
- Residual analysis → approximately normal
- Residual vs predicted → slight heteroscedasticity
- VIF → low multicollinearity
- Strong generalization on test data

---

## 📊 Visualizations
- Distribution plots
- Correlation heatmap
- Residual plots
- Actual vs Predicted scatter plot

---

## 💡 Key Insights

### 🔥 Positive Drivers
- Perceived temperature (atemp)
- Year-over-year growth

### ❌ Negative Drivers
- Humidity
- Windspeed
- Bad weather conditions

### 📅 Seasonal Trends
- High demand: Fall, moderate weather
- Low demand: Spring, extreme summer

---

## 🚀 Business Strategy

### 1. Demand Forecasting
- Use weather-based prediction models

### 2. Dynamic Pricing
- Increase prices in high demand
- Discounts in bad weather

### 3. Fleet Optimization
- Allocate bikes based on demand patterns

### 4. Seasonal Campaigns
- Boost demand in low seasons

### 5. Smart Operations
- Schedule maintenance in low-demand periods

---

## 🛠️ Tech Stack
- Python 
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Statsmodels

---

## 📂 Project Structure
├── data.csv

├── Smart_Mobility_Prediction.ipynb

├── Data dictinonary.txt

├── README.md

---

## ▶️ How to Run
```bash
git clone https://github.com/your-username/bike-demand-analysis.git
cd bike-demand-analysis
pip install -r requirements.txt
jupyter notebook
