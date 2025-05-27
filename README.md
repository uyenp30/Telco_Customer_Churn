# 🧑‍💼📉 Customer Churn Prediction
Why did customers churn? Who are going to churn next? Exploring data leads to strategic recommendations.

---

## 📌 Project Objectives

- Analyze customer data to uncover patterns associated with churn
- Build predictive models to classify churn vs. non-churn customers
- Interpret key drivers of churn for business decision-making
- Communicate insights through data visualizations and metrics

---

## 📁 Dataset

- **Source**: [Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data)
- **Rows**: ~7,043 customer records
- **Features**:  
  - Demographics (gender, senior citizen, partner, etc.)  
  - Services (internet, phone, streaming)  
  - Contract type, payment method, and tenure  
  - Churn status (target variable)

---

## 🛠️ Tools & Libraries

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-2D6EB5?style=flat&logo=seaborn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=matplotlib&logoColor=white)
![scikit-learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)

---

## 📈 Workflow Summary

### 1️⃣ Data Preparation
- Loaded the Telco churn dataset.
- Fixed data types: converted `SeniorCitizen` to categorical and `TotalCharges` to numeric.
- Handled missing values by dropping them due to low proportion and lack of churn signal.
- Dropped irrelevant column `customerID`.

### 2️⃣ Exploratory Data Analysis (EDA)
- Explored churn distribution (26.9% of customers churned).
- Visualized outliers and distributions for `tenure`, `MonthlyCharges`, and `TotalCharges`.
- Found no major outliers, but some skewness → applied standardization later.

### 3️⃣ Feature Engineering & Processing
- Identified and separated numerical and categorical features.
- Used **OneHotEncoding** for categorical variables and **StandardScaler** for numerical ones.
- Built a preprocessing pipeline using **ColumnTransformer** and **Pipeline**.
- Created a fully encoded feature set and calculated correlation of all features with churn.
  
### 4️⃣ Insights from Feature Correlation
- Top churn indicators: `Contract_Month-to-month`, `OnlineSecurity_No`, `TechSupport_No`, `ElectronicCheck`, `FiberOptic`, `MonthlyCharges`
- Strong retention signals: Long `tenure`, `Contract_Two year`, and higher `TotalCharges`

---

## 🧠 Results

| Model              | Accuracy | Precision | Recall | F1-score |
|-------------------|----------|-----------|--------|----------|
| Logistic Regression | 80%   | 0.65      | 0.57   | 0.61     |
| Random Forest       | 79%   | 0.62      | 0.51   | 0.56     |
| XGBoost             | 77%   | 0.57      | 0.52   | 0.54     |

✅ **Best Model:** Random Forest Classifier  
✅ **Top Features:** Contract Type, Tenure, Monthly Charges

---

## 💼 Business Impact and Suggestions

By deploying this model, businesses can:
- Proactively target customers likely to churn
- Offer personalized retention strategies
- Improve revenue by reducing customer loss
- Inform decisions for subscription models and pricing

Some suggestions for business
- Encourage customers to shift to longer-term contracts (e.g., one- or two-year).
- Incentivize adoption of support services like Tech Support, Device Protection, and Online Security.
- Monitor and improve satisfaction among Fiber Optic users.
- Investigate why electronic check users are churning—possibly a billing experience issue.

---

## ✨ Key Learnings

- **Feature engineering** has a major impact on model performance
- Balancing interpretability and accuracy is key in real-world use
- Visualization helps bridge the gap between technical and business audiences
- Evaluating models using **multiple metrics** reveals different strengths


---

## 🌱 About Me

I'm a self-taught data enthusiast and economics student passionate about using data to solve real-world problems.  
This project was part of my learning journey in Python and machine learning, and you can find more of my work [here](https://github.com/uyenp30/Data-Projects) 💻🌻

---

*Thank you for reading!* ✨  
*If you found this useful or have feedback, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/uyen-pham-sua/).*  
