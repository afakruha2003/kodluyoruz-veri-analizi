# 🌱 Renewable Energy Consumption Analysis (1990–2022)

## 📌 Project Overview

This project analyzes **renewable energy consumption across countries and regions between 1990 and 2022**, focusing on long-term trends, country-level comparisons, and future projections using machine learning techniques.

The study applies **data preprocessing, exploratory data analysis (EDA), visualization, and linear regression-based forecasting** to derive meaningful insights from raw energy data and to highlight the global transition toward sustainable energy sources.

---

## 🎯 Objectives

The main objectives of this project are:

- Analyze **temporal trends** in renewable energy consumption  
- Compare **consumption levels and growth rates** across countries  
- Apply **data cleaning and exploratory data analysis (EDA)** techniques  
- Visualize energy transition patterns using statistical and graphical methods  
- Demonstrate the importance of renewable energy for **sustainability** through data-driven insights  
- Predict **future renewable energy consumption** based on historical data  

---

## 📊 Dataset Description

- **Time Period:** 1990 – 2022  
- **Scope:** Countries and regions worldwide  
- **Energy Type:** Renewables  
- **Initial Format:** Wide format (years as columns)  
- **Final Format:** Long format (Year–Energy structure)  

---

## 🧹 Data Preprocessing

Before analysis and modeling, the following preprocessing steps were applied:

- Removal of completely empty rows and columns  
- Re-indexing the dataset for consistency  
- Data type validation and conversion for numerical analysis  
- Selection of year-based numerical columns as model features  
- Transformation from **wide format to long format**:
  - `Year`: Year of observation  
  - `Energy`: Renewable energy consumption value  
- Conversion of `Year` to numeric format  
- Handling non-numeric energy values as `NaN`  
- Removal of rows containing missing (`NaN`) values  
- Filtering the dataset to include only **Renewables**  

These steps ensured **data reliability, consistency, and model compatibility**.

---

## 🔍 Exploratory Data Analysis (EDA)

During EDA, the following analyses were conducted:

- Yearly trends in renewable energy consumption  
- Country-level comparisons of consumption levels  
- Identification of global growth patterns and acceleration periods  

### Key Observations

- Renewable energy consumption shows a **clear upward global trend**  
- Growth has accelerated in recent years, reflecting the impact of  
  **climate policies and environmental awareness**  
- Renewable energy is no longer an alternative source but a **core component of global energy systems**

---

## 🤖 Machine Learning & Forecasting

### Country-Level Forecasting: China Example

A **Linear Regression** model was built using China’s historical renewable energy data to forecast consumption for the next 10 years.

- **Model:** Linear Regression  
- **Input (X):** Year  
- **Target (y):** Renewable energy consumption  

```python
from sklearn.linear_model import LinearRegression
import pandas as pd

country = "China"
df_country = df_renew[df_renew["countries"] == country]

X = df_country[["Year"]]
y = df_country["Energy"]

model = LinearRegression()
model.fit(X, y)

# Forecast for next 10 years
future_years = pd.DataFrame({"Year": range(2023, 2033)})
future_pred = model.predict(future_years)

future_df = future_years.copy()
future_df["Predicted_Energy"] = future_pred
```

## 📈 Comparative Forecasting Across Countries

Using data from **1990–2022**, renewable energy consumption growth was projected for the **next 10 years**.

The analysis focuses on:

- Identifying the **top 10 countries** expected to show the highest increase in renewable energy consumption  
- Comparing **energy transition speeds** across countries  
- Evaluating long-term adoption patterns based on historical trends  

This approach enables a **comparative assessment of national energy transition dynamics**.

---

## 🧠 Key Findings & Insights

Key insights derived from the analysis include:

- Renewable energy consumption is **steadily increasing worldwide**  
- Some countries adopted renewable energy **early**, resulting in strong long-term growth  
- Other countries show **slower but stable** adoption patterns  
- Developed countries generally demonstrate higher consumption levels due to:
  - Advanced technology  
  - Strong energy infrastructure  

Although **China** has been the largest renewable energy consumer between **1990–2022**,  
model projections suggest that **the United States is expected to experience the highest growth rate over the next decade**.

---

## 🛠 Technologies & Libraries Used

The following tools and libraries were used throughout the project:

- **Python**  
- **Pandas**  
- **NumPy**  
- **Matplotlib**  
- **Seaborn**  
- **Scikit-learn**  

---

## 🚀 Project Contribution

This project demonstrates the ability to:

- Clean and preprocess **real-world datasets**  
- Perform **exploratory and comparative data analysis**  
- Analyze **time-based trends** in large datasets  
- Build **interpretable machine learning models**  
- Generate **future forecasts** using historical data  
- Translate sustainability challenges into **data-driven insights**
