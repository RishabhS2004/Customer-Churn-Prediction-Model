# INSTALLATION GUIDE:

## 1. Clone the repository-

git clone https://github.com/your-username/customer-churn-prediction.git
cd customer-churn-prediction

## 2. Create virtual environment-

Windows:
python -m venv venv
venv\Scripts\activate

Mac\Linux:
python3 -m venv venv
source venv/bin/activate

## 3. Install dependencies-

pip install -r requirements.txt

# RUNNING THE PIPELINE:

## Train the Model-
python src/train.py

## Start MLflow UI-
mlflow ui

## Open your browser and go to:
http://127.0.0.1:5000

## Run the Flask API-
python app/app.py

## The Flask server will start at:
http://127.0.0.1:8000

## Prediction Endpoint-
POST /predict

## Sample JSON Input-
{
    "gender": "Female",
    "SeniorCitizen": 0,
    "Partner": "Yes",
    "Dependents": "No",
    "tenure": 12,
    "MonthlyCharges": 75.5,
    "TotalCharges": 900.2
}

## Sample Response-
{
    "prediction": "Customer is likely to churn"
}

# PROJECT THEORY:
# Customer Churn Prediction System

## Overview

Customer churn is one of the biggest challenges faced by businesses today, especially in industries like banking, telecom, SaaS, and subscription-based services. Losing customers directly affects revenue and business growth, which makes customer retention extremely important.

This project focuses on building a Machine Learning-based Customer Churn Prediction System that can identify customers who are likely to leave a service in the future. By analyzing customer-related data such as demographics, subscription details, payment information, and service usage patterns, the model predicts whether a customer is likely to churn or stay.

The project covers the complete Machine Learning workflow, including:
- Data preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Model training and evaluation
- Experiment tracking using MLflow
- API deployment using Flask

The main objective of this project is to help businesses take proactive actions to retain customers before they leave.

---

# Features

- Predict customer churn using Machine Learning
- Clean and preprocess customer data
- Train and compare multiple ML models
- Track experiments and model metrics using MLflow
- Manage model versions and registry
- Deploy the model using Flask REST API
- Send real-time prediction requests using JSON
- Modular and scalable project structure

---

# Technologies Used

## Programming Language
- Python

## Libraries and Frameworks
- Pandas
- NumPy
- Scikit-learn
- MLflow
- Flask
- Joblib
- Matplotlib
- Seaborn

## Tools
- VS Code
- Git & GitHub
- Postman
- MLflow UI

---

# Project Workflow

## 1. Data Collection

The dataset contains customer-related information such as:
- Customer demographics
- Subscription details
- Service usage information
- Payment details
- Customer tenure
- Contract type

### Target Variable
`Churn` → Indicates whether the customer left the service or continued using it.

---

## 2. Data Preprocessing

Before training the models, the dataset was cleaned and transformed using several preprocessing techniques.

The preprocessing pipeline includes:
- Handling missing values
- Encoding categorical variables
- Feature scaling
- Feature selection
- Splitting the dataset into training and testing sets

---

## 3. Exploratory Data Analysis (EDA)

EDA was performed to better understand customer behavior and identify patterns related to churn.

The analysis focused on:
- Customer behavior trends
- Churn distribution
- Correlation between features
- Important churn-driving factors

### Visualization Techniques Used
- Heatmaps
- Histograms
- Count plots
- Correlation matrices
- Bar charts

---

# Machine Learning Models Used

Multiple Machine Learning algorithms were trained and evaluated to compare their performance.

| Model | Description |
|---|---|
| Logistic Regression | Baseline classification model |
| Decision Tree | Rule-based predictive model |
| Random Forest | Ensemble learning model with improved accuracy |
| K-Nearest Neighbors (KNN) | Distance-based classification model |
| Support Vector Machine (SVM) | Margin-based classification model |
| Multi-Layer Perceptron (MLP) | Neural network-based classifier |

---

# Evaluation Metrics

The models were evaluated using the following classification metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC-AUC Score

These metrics help measure how effectively the model identifies customers who are likely to churn.

---

# MLflow Integration

MLflow was integrated into the project to manage experiments and track model performance efficiently.

### MLflow Features Used
- Experiment tracking
- Parameter logging
- Metric logging
- Model versioning
- Model comparison
- Model registry management

This makes the workflow more organized, reproducible, and scalable.

---

# Project Structure

```bash
customer-churn-prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── EDA_and_Model_Training.ipynb
│
├── models/
│   └── trained_models/
│
├── mlruns/
│
├── app/
│   └── app.py
│
├── src/
│   ├── preprocessing.py
│   ├── train.py
│   ├── evaluate.py
│   └── predict.py
│
├── requirements.txt
├── README.md
└── .gitignore
