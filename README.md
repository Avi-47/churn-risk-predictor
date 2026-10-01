Customer Churn Risk Predictor

A machine learning classification project that predicts customer churn risk on a 1–5 scale using customer demographics, engagement behavior, transaction activity, and customer feedback.

The project demonstrates an end-to-end machine learning workflow, including exploratory data analysis, preprocessing, model comparison, hyperparameter tuning, model serialization, and deployment through an interactive Streamlit application.

🚀 Live Application
Try the model online

🌐 Open Customer Churn Risk Predictor

The deployed application allows users to enter customer information and receive a predicted churn-risk category through an interactive web interface.

📌 Project Overview

Customer churn can negatively affect revenue, customer lifetime value, and long-term business growth.

The objective of this project is to build a machine learning model capable of classifying customers into different levels of churn risk based on their demographic, behavioral, transactional, and feedback characteristics.

The project focuses on the complete workflow:

Customer Data
     ↓
Data Cleaning
     ↓
Exploratory Data Analysis
     ↓
Feature Engineering
     ↓
Model Comparison
     ↓
Hyperparameter Tuning
     ↓
Model Selection
     ↓
Model Serialization
     ↓
Streamlit Deployment

🎯 Problem Statement

The goal is to identify customers who may have a higher likelihood of churn so that businesses can potentially prioritize them for retention analysis and customer engagement strategies.

The model predicts one of five churn-risk categories:

Score	Risk Level
1	Very Low
2	Low
3	Moderate
4	High
5	Very High

Note: These categories represent machine-learning predictions and should not be interpreted as guaranteed churn probabilities.

📊 Dataset

The dataset contains customer demographic, transactional, engagement, and feedback information.

Customer Demographics

Age

Gender

Region Category

Membership Category

Referral Status

Customer Engagement

Login Frequency

Average Time Spent

Medium of Operation

Preferred Offer Types

Transaction & Loyalty Information

Transaction Value

Points in Wallet

Discount Usage

Customer Experience

Complaint History

Customer Feedback

Complaint Status

🔍 Data Preprocessing

The dataset was prepared for machine learning through several preprocessing steps:

Removal of irrelevant features

Missing-value handling

Categorical feature encoding

Numerical feature scaling

Outlier identification

Feature preparation for classification models

The preprocessing workflow is incorporated into the machine learning pipeline to ensure consistent transformations during prediction.

📈 Exploratory Data Analysis

The exploratory analysis examined relationships between customer characteristics and churn risk.

Key analysis included:

Churn-risk distribution

Churn risk across membership categories

Churn risk across customer feedback

Transaction value versus churn risk

Points in wallet versus churn risk

Average time spent versus churn risk

Feature correlation analysis

Outlier analysis using the Interquartile Range (IQR)

These analyses were used to understand the dataset and guide the subsequent modeling process.

🤖 Machine Learning Models

Multiple classification algorithms were evaluated:

Random Forest Classifier

Support Vector Machine

Logistic Regression

Decision Tree

Gaussian Naive Bayes

Hyperparameter tuning was performed using:

GridSearchCV

5-fold cross-validation

The final implementation uses a Random Forest Classifier with 20 estimators based on the model-selection process performed during development.

⚙️ Machine Learning Pipeline

The project uses a reusable preprocessing and prediction pipeline.

Raw Customer Input
        ↓
Preprocessing
        ↓
Feature Transformation
        ↓
Random Forest Model
        ↓
Churn Risk Classification
        ↓
Risk Level


The trained pipeline is serialized using joblib and loaded by the Streamlit application for inference.

This approach keeps the preprocessing and prediction workflow consistent between model development and application usage.

🌐 Streamlit Deployment

The trained model is integrated into a Streamlit application that provides an interactive interface for customer churn-risk prediction.

Application features

Customer information input

Automated preprocessing

Real-time prediction

Five-level churn-risk classification

Color-coded risk presentation

Human-readable risk descriptions

Live App

Launch Customer Churn Risk Predictor

🛠️ Technology Stack
Technology	Purpose
Python	Programming language
pandas	Data manipulation
NumPy	Numerical computation
scikit-learn	Machine learning
Matplotlib	Data visualization
Seaborn	Statistical visualization
joblib	Model serialization
Streamlit	Web application
📁 Project Structure
churn-risk-predictor/
│
├── app.py
├── requirements.txt
├── README.md
├── LICENSE
│
├── data/
│   └── ...
│
├── models/
│   └── ...
│
├── notebooks/
│   └── ...
│
└── ...


The exact directory structure may vary depending on the current development version.

💻 Run Locally
1. Clone the repository
git clone https://github.com/Avi-47/churn-risk-predictor.git
cd churn-risk-predictor

2. Create a virtual environment
Windows
python -m venv .venv
.venv\Scripts\activate

macOS / Linux
python3 -m venv .venv
source .venv/bin/activate

3. Install dependencies
pip install -r requirements.txt

4. Run the application
streamlit run app.py


The application will open in your browser at the local Streamlit address shown in the terminal.

📌 Key Highlights

End-to-end customer churn classification workflow

Exploratory analysis of customer behavior

Data preprocessing and feature engineering

Comparison of multiple classification algorithms

Hyperparameter tuning using GridSearchCV

5-fold cross-validation

Random Forest-based prediction pipeline

Model serialization using joblib

Interactive Streamlit application

Publicly deployed prediction interface

⚠️ Limitations

This project is intended as a machine learning and deployment demonstration rather than a production-ready customer retention system.

Important considerations include:

Model performance depends on the quality and representativeness of the dataset.

Churn-risk categories are classification outputs rather than calibrated churn probabilities.

Relationships identified in the dataset may not generalize to other customer populations.

Predictions should be validated before being used for operational customer-retention decisions.

A production deployment would require monitoring for data drift, model degradation, and changes in customer behavior.

🔮 Future Improvements

Potential extensions include:

Model explainability using SHAP

Probability calibration

Feature importance analysis

Class-imbalance analysis

Gradient boosting model comparison

Model monitoring and data-drift detection

Automated model retraining

Customer-level prediction explanations

REST API deployment

CRM integration

Experiment tracking

Production model monitoring

📚 What This Project Demonstrates

This project demonstrates the ability to take a structured business problem and develop an end-to-end machine learning solution:

Business Problem → Data Analysis → Preprocessing → Model Development → Evaluation → Serialization → Deployment

The emphasis is on building a complete and reusable workflow rather than only training an individual classification model.

🔗 Links

GitHub Repository: Avi-47/churn-risk-predictor

Live Streamlit Application: Customer Churn Risk Predictor

📄 License

See the LICENSE file for licensing information.