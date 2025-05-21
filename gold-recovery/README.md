# 🛢️ Gold Recovery Optimization: Region Selection for Oil Well Development

## 📍 Project Description

This project was developed for **OilyGiant**, a mining company evaluating where to drill its next oil well. The objective was to identify the most profitable region out of three candidates by building a predictive model for oil reserves and simulating expected profits and risk using historical data.

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
- pandas  
- NumPy  
- scikit-learn  
- Plotly Express  
- Linear Regression  
- Bootstrap Sampling  

---

## 🧭 Project Structure

- **Step 1: Data Loading & Preprocessing**  
  - Loaded oil reserve datasets from three regions  
  - Verified data integrity and confirmed no missing values  
  - Investigated duplicate well IDs but retained them, as reserve values varied  

- **Step 2: Modeling Reserve Volume per Region**  
  - Built separate Linear Regression models for each region  
  - Splitted each dataset into 75% training and 25% validation sets  
  - Computed RMSE and mean predicted reserves for each region  
  - Results:  
    - Region 0: RMSE = 37.58, Avg = 92.59  
    - Region 1: RMSE = 0.89, Avg = 68.73  
    - Region 2: RMSE = 40.03, Avg = 94.97  

- **Step 3: Break-even Analysis**  
  - Estimated development cost per well = $500,000  
  - Revenue per 1,000 barrels = $4,500  
  - Break-even threshold = 111.11 thousand barrels per well  
  - None of the regions meet this threshold  

- **Step 4: Profit Simulation**  
  - Defined a custom function to simulate profit from model predictions  
  - Region 0: $332,082.60  
  - Region 1: $241,508.67  
  - Region 2: $271,035.00  
  - Region 0 had the highest projected profit

- **Step 5: Risk Assessment with Bootstrapping**  
  - Conducted 1,000 bootstrap samples per region  
  - Computed mean profit, 95% confidence intervals, and loss risk  
    - Region 0: 6.6% risk  
    - Region 1: **0.4% risk**  
    - Region 2: 7.2% risk  

---

## ⚙️ Setup Instructions
- Clone the repository, then install all dependencies using pipinstall.

---

## 🚀 Usage

Run the notebook `Gold_Recovery.ipynb` to:

- Load and clean region-specific oil well data  
- Train Linear Regression models to predict reserves  
- Simulate profit for each region  
- Analyze risk using bootstrap sampling  
- Identify the most profitable and stable region for development  

---

## 🧾 Conclusion

Based on the analysis of oil reserves and profit projections across the three regions:

- **Region 0** emerges as the most profitable with an estimated profit of **$332,082.60**  
- **None of the regions** meet the break-even threshold of **111.11 thousand barrels**  
- **Region 1** has the **lowest risk (0.4%)** but the **least reserves**  
- **Region 2** offers **high reserves** but comes with a **higher risk (7.2%)**  
- **Region 0** is a viable candidate if profit maximization is prioritized, though risk still exists  

---

## 💡 Suggestions for Business Improvement

- **Conduct an in-depth economic feasibility study** before investing in Region 0  
- **Explore partnerships or subsidies** to reduce per-well development costs  
- **Recalibrate model inputs** with more recent or enriched data (e.g., geological, environmental)  
- **Integrate dynamic pricing models** into simulations to test sensitivity to oil price fluctuations  
