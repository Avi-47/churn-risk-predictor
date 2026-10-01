# 🚀 Customer Churn Risk Predictor

<p align="center">
  <b>Machine Learning · Random Forest · Classification · Streamlit</b>
</p>

An end-to-end machine learning application that predicts customer churn risk across **5 categories (Very Low to Very High)** using demographic, behavioral, transactional, and customer feedback data.

The project covers data preprocessing, exploratory data analysis, model comparison, hyperparameter tuning, and deployment through an interactive Streamlit web app.

## 🌐 Live Demo

🔗 **[Launch Customer Churn Risk Predictor](YOUR_STREAMLIT_APP_URL)**

Enter customer details and get an instant churn-risk classification.

## ✨ Key Features

* 📊 **Exploratory Data Analysis:** Analyze customer behavior, transactions, feedback, and churn patterns.
* 🧹 **Data Preprocessing:** Handle missing values, encode categorical features, and prepare numerical features.
* 🤖 **Model Comparison:** Evaluate Random Forest, SVM, Logistic Regression, Decision Tree, and Gaussian Naive Bayes.
* ⚙️ **Hyperparameter Tuning:** Apply GridSearchCV with 5-fold cross-validation.
* 🌲 **Random Forest:** Use a tuned Random Forest classifier for five-level churn-risk prediction.
* 🌐 **Streamlit Deployment:** Interactive web interface for real-time predictions.
* 💾 **Model Serialization:** Save and load the trained pipeline using Joblib.

## 🎯 Churn Risk Categories

| Score | Risk Level   |
| :---: | ------------ |
|   1   | 🟢 Very Low  |
|   2   | 🟢 Low       |
|   3   | 🟡 Moderate  |
|   4   | 🟠 High      |
|   5   | 🔴 Very High |

> **Note:** The model outputs classification categories, not calibrated churn probabilities or guaranteed predictions of customer behavior.

## 🛠️ Tech Stack

| Technology           | Purpose                            |
| -------------------- | ---------------------------------- |
| Python               | Core development                   |
| Pandas & NumPy       | Data processing                    |
| Scikit-learn         | Machine learning and preprocessing |
| Matplotlib & Seaborn | Data visualization                 |
| Joblib               | Model serialization                |
| Streamlit            | Web application                    |

## 🔄 ML Workflow

```text
Customer Data
     ↓
Data Cleaning & Preprocessing
     ↓
Exploratory Data Analysis
     ↓
Feature Engineering
     ↓
Model Comparison
     ↓
Hyperparameter Tuning
     ↓
Random Forest Classifier
     ↓
Model Serialization (Joblib)
     ↓
Streamlit Deployment
     ↓
Real-Time Churn Risk Prediction
```

## 📂 Project Structure

```text
churn-risk-predictor/
├── app.py
├── requirements.txt
├── README.md
├── LICENSE
├── data/
├── models/
└── notebooks/
```

## 💻 Run Locally

**1. Clone the repository**

```bash
git clone https://github.com/Avi-47/churn-risk-predictor.git
cd churn-risk-predictor
```

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

**3. Launch the application**

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal to access the application.

## 🔮 Future Improvements

* SHAP-based model explainability
* Probability calibration
* Feature importance visualization
* Advanced ensemble model comparison
* Data drift and model performance monitoring
* REST API and CRM integration

## ⚠️ Disclaimer

This project is a machine learning and deployment demonstration. Predictions depend on the training dataset and should be validated before being used for real-world customer-retention decisions.

## 👨‍💻 Author

**Avimanyu Goswami**

[GitHub](https://github.com/Avi-47) · [Repository](https://github.com/Avi-47/churn-risk-predictor)

**Built with Python, Scikit-learn & Streamlit.**
