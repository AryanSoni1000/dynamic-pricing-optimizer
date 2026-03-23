<img width="1795" height="867" alt="image" src="https://github.com/user-attachments/assets/0d7ada94-f21f-4c64-8ec1-879e6836b2c9" /># Dynamic Pricing Optimizer

An AI-powered pricing analytics tool that helps e-commerce businesses determine the optimal selling price to maximize revenue.  
The project uses **Machine Learning**, **model comparison**, and **Streamlit** to provide real-time pricing insights through an interactive dashboard.

---

## Overview

Dynamic pricing is a pricing strategy where product prices are adjusted based on market conditions such as competitor pricing, demand, promotions, and seasonality.

This project simulates a real-world e-commerce pricing environment and helps answer a key business question:

> **What is the best price to charge in order to maximize revenue?**

The system evaluates multiple regression models, selects the best-performing one, and then uses it to estimate demand and revenue across different price points. A visual **Revenue vs. Price** curve is also generated to help identify the optimal price.

---

## Features

- Predicts demand-related behavior using machine learning
- Compares multiple regression models and selects the best one
- Estimates expected revenue for different pricing scenarios
- Finds the optimal price that maximizes revenue
- Interactive Streamlit dashboard
- Revenue vs. Price curve visualization
- Clean and modern dark-themed UI
- Easy to run locally and deploy online

---

## Problem Statement

In e-commerce, choosing the right product price is difficult:

- If the price is too high, demand may fall
- If the price is too low, profit margins shrink
- If the price ignores competition and promotions, business decisions become unreliable

This project addresses the problem of **price optimization** by using machine learning to:

1. Predict demand or units sold from market and business features  
2. Compare multiple regression models  
3. Estimate revenue for different prices  
4. Select the price that gives the maximum revenue  

---

## Dataset

The dataset contains structured e-commerce pricing records. Each row represents a pricing scenario with business and market factors.

### Columns Used

- `price` — current selling price
- `competitor_price` — competitor’s price
- `cost_price` — product cost
- `promo_flag` — whether a promotion is active
- `day_of_week` — day number in the week
- `is_weekend` — weekend indicator
- `month` — month of the year
- `units_sold` — demand-related target

The data is suitable for regression-based modeling because the output is continuous.

---

## Methodology

### 1. Data Preprocessing
The dataset is cleaned and prepared for model training. Missing values are handled, and numerical encoding is applied wherever needed.

### 2. Feature Selection
The following features are used for prediction:

- `competitor_price`
- `cost_price`
- `promo_flag`
- `day_of_week`
- `is_weekend`
- `month`
- `units_sold`

The target variable is:

- `price`

### 3. Model Training
Instead of relying on a single algorithm, the project trains and compares multiple regression models:

- Linear Regression
- Random Forest Regressor
- XGBoost Regressor

### 4. Model Selection
The best model is selected based on test performance, especially the lowest prediction error.

### 5. Price Optimization
After selecting the best model, the app evaluates multiple price points and computes expected revenue using:

\[
Revenue = Price \times Units\ Sold
\]

The price that produces the highest revenue is selected as the optimal price.

---

## Tech Stack

| Category | Technologies |
|---------|--------------|
| Language | Python |
| Machine Learning | Scikit-learn, XGBoost |
| Data Handling | Pandas, NumPy |
| Visualization | Plotly |
| UI Framework | Streamlit |
| Deployment | Streamlit Cloud / Localhost |

---

## Project Workflow

1. User enters product pricing details in the dashboard  
2. The selected ML model predicts the expected units sold  
3. Revenue is calculated for different candidate prices  
4. The best price is selected based on maximum revenue  
5. A Revenue vs. Price curve is displayed to visualize the result  

---

## Results

The project demonstrates that machine learning can be effectively used for dynamic pricing optimization.

### Key Observations
- Revenue increases with price only up to a certain point
- After that point, demand drops and revenue starts decreasing
- The optimal price lies near the peak of the Revenue vs. Price curve

This confirms the usefulness of dynamic pricing in business decision-making.

---

## Live App(Deployed on Streamlit Cloud)

https://dynamic-pricing-optimizer-nfkynxdmljwjryfxsojacq.streamlit.app/

