# 🩺 Obesity Prediction Calculator Model

This project builds an **Obesity Prediction Calculator** using a trained machine learning model.  
It integrates **FastAPI** for the backend API and **Streamlit** for the web interface, allowing users to input health-related data and receive **real-time obesity level predictions**.

---

## Overview
The goal of this project is to develop a machine learning model that predicts obesity levels based on individual lifestyle and demographic data.  
It demonstrates the complete ML workflow from **data preprocessing** and **model training** to **deployment** as an interactive web application.

Obesity levels are classified into categories such as:
- **Insufficient Weight**
- **Normal Weight**
- **Overweight**
- **Obesity Type I**
- **Obesity Type II**
- **Obesity Type III**

---

## Dataset
- **File:** `ObesityDataSet2.csv`  
- **Total Entries:** 1056  
- **Target Column:** `NObeyesdad` (obesity level category)  
- **Features:** Age, Gender, Height, Weight, Family History, Eating Habits, Physical Activity, Transportation, and others.

---

## Data Preprocessing
- Removed rows with missing values.  
- Cleaned the `Age` column (removed text like “years” and converted to integer).  
- Applied **One-Hot Encoding** for categorical features.  
- Encoded target labels using **LabelEncoder**.  
- Split the dataset into **training (80%)** and **testing (20%)** sets.  
- Scaled numeric features for model compatibility.

---

## Model Pipeline
1. **Data Loading:** Imported and cleaned raw data from CSV.  
2. **Feature Engineering:** Encoded and standardized all input features.  
3. **Model Training:** Built and evaluated multiple supervised models (Logistic Regression, Random Forest, XGBoost).  
4. **Model Saving:** Exported the best-performing model for deployment.  
5. **Deployment:** Integrated trained model into FastAPI and Streamlit.

---

## Deployment
- **FastAPI** serves as the backend REST API that loads the trained model and processes prediction requests.  
- **Streamlit** provides a simple, user-friendly web interface where users can input health-related data and get instant predictions.

### Example Flow
1. User opens the web app.  
2. Inputs their health metrics (age, weight, physical activity, etc.).  
3. Streamlit sends data to the FastAPI endpoint `/predict`.  
4. FastAPI runs the ML model and returns the obesity category.  
5. Streamlit displays the predicted obesity level in real-time.

---

## Results
After preprocessing, the dataset was successfully prepared for model training and deployment.  
The trained model accurately predicts obesity categories based on user inputs, and the deployed app provides real-time results in an interactive dashboard.

---

## Tech Stack
- Python  
- Scikit-learn  
- Pandas, NumPy  
- FastAPI  
- Streamlit  
- Matplotlib, Seaborn  

---
