Customer Churn Risk Predictor

Machine Learning • Classification • Random Forest • Streamlit

A machine learning project that predicts customer churn risk on a scale of 1–5 using customer demographics, engagement behavior, transaction activity, and customer feedback.

The project covers an end-to-end machine learning workflow — from exploratory data analysis and preprocessing to model comparison, hyperparameter tuning, model serialization, and deployment as an interactive Streamlit web application.

🚀 Live Demo
Try the application

🌐 Open Customer Churn Risk Predictor

Enter customer information into the application and receive a predicted churn-risk category in real time.

📌 Project Overview

Customer churn can have a significant impact on revenue, customer lifetime value, and long-term business growth.

The objective of this project is to develop a machine learning classification model that identifies customers across five levels of churn risk based on demographic, behavioral, transactional, and customer-experience features.

Machine Learning Workflow
┌──────────────────────┐
│    Customer Data     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Data Cleaning      │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Exploratory Analysis │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Feature Engineering  │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│  Model Comparison    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Hyperparameter Tuning│
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Model Selection    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Model Serialization  │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Streamlit Deployment │
└──────────────────────┘

🎯 Problem Statement

The goal is to identify customers who may have elevated churn risk so that businesses can potentially prioritize them for further analysis and customer-retention strategies.

The model classifies customers into five churn-risk categories:

Score	Risk Level
1	🟢 Very Low
2	🟢 Low
3	🟡 Moderate
4	🟠 High
5	🔴 Very High

Important: These categories are machine-learning classification outputs and should not be interpreted as calibrated probabilities or guaranteed predictions of customer behavior.

📊 Dataset

The dataset contains customer demographic, transactional, engagement, loyalty, and feedback information.

👤 Customer Demographics

Age

Gender

Region Category

Membership Category

Referral Status

📱 Customer Engagement

Login Frequency

Average Time Spent

Medium of Operation

Preferred Offer Types

💳 Transaction & Loyalty

Transaction Value

Points in Wallet

Discount Usage

💬 Customer Experience

Complaint History

Customer Feedback

Complaint Status

🔍 Data Preprocessing

The dataset was prepared for machine learning through multiple preprocessing steps:

Removal of irrelevant features

Missing-value handling

Categorical feature encoding

Numerical feature scaling

Outlier identification

Feature preparation for classification

Consistent preprocessing during model inference

The preprocessing workflow is integrated into the machine learning pipeline to ensure that training and prediction use consistent transformations.

📈 Exploratory Data Analysis

Exploratory analysis was performed to understand the relationship between customer characteristics and churn risk.

Analysis included

Churn-risk distribution

Churn risk by membership category

Churn risk by customer feedback

Transaction value versus churn risk

Points in wallet versus churn risk

Average time spent versus churn risk

Feature correlation analysis

Outlier analysis using the Interquartile Range (IQR) method

The EDA helped identify patterns in customer behavior and provided context for the subsequent modeling process.

🤖 Machine Learning

Several classification algorithms were evaluated:

Model	Purpose
Random Forest	Ensemble tree-based classification
Support Vector Machine	Margin-based classification
Logistic Regression	Linear classification baseline
Decision Tree	Interpretable tree-based model
Gaussian Naive Bayes	Probabilistic classification
Hyperparameter Optimization

Model tuning was performed using:

GridSearchCV

5-fold cross-validation

The final implementation uses a Random Forest Classifier with 20 estimators, based on the model-selection process performed during development.

⚙️ Prediction Pipeline

The application uses a reusable preprocessing and prediction pipeline.

Customer Input
      │
      ▼
┌─────────────────┐
│  Preprocessing  │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Feature         │
│ Transformation  │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Random Forest   │
│ Classifier      │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Churn Risk      │
│ Classification  │
└────────┬────────┘
         ↓
┌─────────────────┐
│ Risk Level 1–5  │
└─────────────────┘


The trained pipeline is serialized using Joblib and loaded by the Streamlit application during inference.

This ensures that the same preprocessing logic is applied when making predictions through the deployed application.

🌐 Streamlit Application

The trained model is integrated into an interactive Streamlit application.

Application Features

Customer information input

Automated preprocessing

Real-time prediction

Five-level churn-risk classification

Color-coded risk presentation

Human-readable risk descriptions

Interactive web interface

🔗 Live Application

Launch Customer Churn Risk Predictor →

🛠️ Technology Stack
Technology	Purpose
🐍 Python	Core programming language
🐼 pandas	Data manipulation
🔢 NumPy	Numerical computation
🤖 scikit-learn	Machine learning and preprocessing
📊 Matplotlib	Data visualization
📈 Seaborn	Statistical visualization
💾 Joblib	Model serialization
🌐 Streamlit	Interactive web application
📁 Project Structure
churn-risk-predictor/
│
├── app.py
├── requirements.txt
├── README.md
├── LICENSE
│
├── data/
│   ├── train.csv
│   └── test.csv
│
├── models/
│   └── ...
│
├── notebooks/
│   └── ...
│
└── ...


The exact structure may vary depending on the current development version of the project.

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


The application will be available at the local Streamlit address displayed in your terminal.

⭐ Key Highlights

End-to-end customer churn classification workflow

Exploratory analysis of customer behavior

Data preprocessing and feature engineering

Multiple classification algorithms evaluated

GridSearchCV hyperparameter optimization

5-fold cross-validation

Random Forest prediction pipeline

Model serialization with Joblib

Interactive Streamlit interface

Publicly deployed machine learning application

⚠️ Limitations

This project is intended as a machine learning and deployment demonstration rather than a production-ready customer-retention system.

Important considerations:

Model performance depends on the quality and representativeness of the dataset.

Churn-risk classes are classification outputs rather than calibrated churn probabilities.

Patterns identified in the dataset may not generalize to other customer populations.

Predictions should be validated before being used for operational customer-retention decisions.

A production system would require monitoring for data drift, model degradation, and changes in customer behavior.

🔮 Future Improvements

Potential improvements include:

 SHAP-based model explainability

 Probability calibration

 Feature importance visualization

 Class-imbalance analysis

 Gradient boosting model comparison

 Data-drift monitoring

 Automated model retraining

 Customer-level prediction explanations

 REST API deployment

 CRM integration

 Experiment tracking

 Production model monitoring

📚 What This Project Demonstrates

This project demonstrates an end-to-end approach to solving a structured business problem with machine learning:

Business Problem
       ↓
Data Analysis
       ↓
Data Preprocessing
       ↓
Feature Engineering
       ↓
Model Development
       ↓
Model Evaluation
       ↓
Hyperparameter Tuning
       ↓
Model Serialization
       ↓
Application Development
       ↓
Cloud Deployment


The project demonstrates both machine learning development and practical model deployment, connecting a trained classification model to an interactive application.

🔗 Project Links
Resource	Link
💻 GitHub Repository	Avi-47/churn-risk-predictor
🌐 Live Application	Customer Churn Risk Predictor
📄 License

This project is distributed under the license specified in the LICENSE file.

👨‍💻 Project

Customer Churn Risk Predictor

Built with Python • scikit-learn • pandas • NumPy • Joblib • Streamlit
