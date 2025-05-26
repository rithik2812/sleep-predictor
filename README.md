# AI Sleep Quality Predictor + Lifestyle Recommender

An end-to-end **Machine Learning + Data Analytics** project that predicts sleep quality scores based on a user's lifestyle habits. Built with Python, scikit-learn, SHAP for explainability, and Gradio for an interactive UI — this app provides actionable insights to help users improve their sleep.

---

## Project Overview

This AI-powered app analyzes a person’s daily habits such as physical activity, stress levels, sleep duration, and more to **predict their sleep quality (0–10)**. It uses a trained ML model to make predictions and offers **personalized lifestyle recommendations** based on model explanations using **SHAP (SHapley Additive exPlanations)**.

The tool also includes a Gradio-powered interface where users can input their data and get:
- A predicted sleep quality score
- Custom tips to improve their sleep
- Top 3 factors affecting their sleep, with positive/negative direction

---

## Tech Stack

- **Python** 🐍
- **Pandas, NumPy** – data manipulation
- **Matplotlib, Seaborn** – visualizations
- **scikit-learn** – ML model (Random Forest Regressor)
- **SHAP** – model interpretability and feature importance
- **Gradio** – user interface for real-time predictions
- **Dataset** – [Sleep Health and Lifestyle Dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset)

---

##  Model & Explainability

### Random Forest Regressor
We used **Random Forest Regressor**, an ensemble machine learning algorithm that combines multiple decision trees and averages their predictions. It’s great for handling non-linear data, avoids overfitting better than individual trees, and works well with both numerical and categorical data.

### SHAP (SHapley Additive exPlanations)
To make the model's decisions transparent, we used **SHAP**, a game-theoretic approach to explain the output of any ML model. SHAP tells you **how much each feature contributed** to the final prediction — for example, whether high stress or low sleep duration pulled the score up or down. This makes the model **interpretable and trustworthy**.

---

## How It Works

### 1. **Data Preprocessing**
- Cleaned column names and encoded categorical variables like Gender, Occupation, and BMI Category using **Label Encoding**.
- Removed unused fields to simplify the model.

### 2. **Model Building**
- Features selected: `age`, `sleep_duration`, `physical_activity_level`, `stress_level`, and encoded categorical features.
- Trained a **Random Forest Regressor** to predict the target: `quality_of_sleep` (0–10 scale).
- Achieved performance:  
  - **RMSE**: ~0.17  
  - **Custom Accuracy (±0.5 tolerance)**: ~92%

### 3. **SHAP-Based Recommendations**
- Used SHAP to interpret model predictions for each user input.
- Highlighted the **top 3 most impactful lifestyle features** influencing the prediction.
- Added **human-readable, lifestyle-specific suggestions** based on user input.

### 4. **Gradio Interface**
- Built a clean UI with input sliders and dropdowns.
- Users can interactively get:
  - Predicted Sleep Score
  -  Custom Health Tips
  -  SHAP-based Feature Insights

---

## Key Features

 Sleep score prediction (0–10 scale)  
 Personalized health recommendations  
 SHAP-powered interpretability  
 Interactive Gradio interface  
 Realtime lifestyle-based feedback

---

##  Insights Captured

Here are some of the **insights** uncovered from this project:

- **Less than 7.5 hours of sleep** significantly lowers predicted sleep quality.
- **High stress levels (>6)** are strongly associated with lower sleep scores.
- Users with **low physical activity (<60 mins/day)** are at higher risk of poor sleep.
- **BMI and occupation** type play a major role in predicting sleep patterns.
- SHAP allows users to understand the **individual drivers** behind their scores — enabling personalized action plans.

---
