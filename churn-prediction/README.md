# 📉 Customer Churn Prediction Project

## 📍 Project Description

This project focuses on predicting customer churn for a telecom company. The goal is to develop a machine learning model that identifies which customers are most likely to cancel their subscriptions, enabling proactive retention efforts and improving customer lifetime value.

---

## 📑 Table of Contents

- [Technologies and Tools Used](#technologies-and-tools-used)  
- [Project Structure](#project-structure)  
- [Setup Instructions](#setup-instructions)  
- [Usage](#usage)  
- [Conclusion](#conclusion)  
- [Suggestions for Business Improvement](#suggestions-for-business-improvement)
  
---

## 🛠️ Technologies and Tools Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- XGBoost
- LightGBM
- CatBoost
- Logistic Regression

---

## 🧭 Project Structure

- **Data Exploration:**  
  Analyzed churn distribution, service types, contract types, demographics, and payment methods to identify key patterns.

- **Data Cleaning & Feature Engineering:**  
  - Encoded categorical features using one-hot encoding.  
  - Scaled numerical features.  
  - Addressed class imbalance by upsampling the minority class.

- **Model Training & Evaluation:**  
  Trained and compared multiple models including:
  - Logistic Regression  
  - XGBoost Classifier
  - LightGBM Classifier
  - CatBoost Classifier  

- **Model Selection:**  
  - LightGBM was selected as the most optimal model. 
  - Achieved an AUC-ROC score of **0.90** on the test set.

- **Model Explainability:**  
- Analyzed and visualized feature importance to explain the most influential factors contributing to customer churn.

---

## ⚙️ Setup Instructions

Clone the repository to your local machine. Ensure you have Python installed along with the required libraries. You can install missing libraries using pip.

Load the datasets contract.csv, personal.csv, internet.csv, and phone.csv into your working directory.

---

## 🚀 Usage

Run the notebook `Finalproduct.ipynb` to:

- Explore and clean the data  
- Train and evaluate models  
- Visualize performance metrics and feature importance  
- Generate churn predictions  

---

## 🧾 Conclusion

LightGBM successfully identified customers likely to churn with AUC-ROC, accuracy, and F1 score. Key churn drivers included:

- Number of subscriptions
- Use of month-to-month contracts  
- Electronic check payment method  
- High monthly charges  

With an **AUC-ROC of 0.90**, this model provides a reliable foundation for churn mitigation strategies.

---

## 💡 Suggestions for Business Improvement

- Launch targeted campaigns for high-risk churn segments (e.g., offer discounts for long-term contracts. senior citizen discounts).    
- Promote use of auto-pay methods by incentivizing bank or credit card payments.
