# Providing Data-Driven Suggestions for HR
**Capstone Project of Google Advanced Data Analytics**

---

## 📌 Project Overview
This project analyzes HR data from a consulting firm (Salifort Motors) to understand the key factors that influence employee turnover.  
The primary goal is to build predictive models that help HR identify employees likely to leave the company and provide actionable recommendations to improve employee satisfaction.

---

## 🎯 Business Problem
The HR department collected employee data but was unsure how to use it effectively.  
Their main question:  
**What factors are most likely to cause employees to leave the company?**

By analyzing the data and building predictive models, this project provides HR with insights and strategies to improve retention.

---

## 📂 Dataset
- **Source:** [Kaggle HR Analytics Dataset](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv)  
- **Size:** 14,999 rows, 10 columns  
- **Data Type:** Mix of numerical and categorical features  

---

## 🔍 Project Workflow
The project was completed in the following phases:

### 1. **Exploratory Data Analysis (EDA)**
- Performed descriptive statistics  
- Renamed columns for clarity  
- Checked for duplicates  
- Identified outliers using boxplots and the IQR method  

### 2. **Data Visualization**
- **Univariate analysis** for numerical and categorical variables  
- **Bivariate analysis** (categorical vs. target, numerical vs. target)  
- **Correlation analysis** between numerical features  

**Key Insights from EDA**  
- Employees leaving are often **overworked**: longer hours, too many projects, and low satisfaction.  
- Lack of promotions or recognition contributes to attrition.  
- Employees with **6+ years tenure** are less likely to leave.  

### 3. **Model Assumptions (Logistic Regression)**
- Outcome variable is categorical  
- Independent observations  
- No severe multicollinearity  
- No extreme outliers  
- Linear relationship between predictors and logit outcome  
- Sufficient sample size  

### 4. **Model Implementation**
Built and compared three models:  
- Logistic Regression  
- Decision Tree  
- Random Forest  

**Evaluation Metrics Used**  
- Confusion Matrix  
- Classification Report (precision, recall, F1-score, accuracy)  
- AUC Curve  
- Hyperparameter tuning with **GridSearchCV**  

### 5. **Data Leakage Check**
- Identified and removed columns causing leakage  
- Re-trained tree-based models on the cleaned dataset  
- Re-evaluated using the same metrics  

### 6. **Feature Importance**
- **Top predictors:** last_evaluation, number_project, tenure, overworked  
- These features were most influential in predicting employee turnover  

---

## 📊 Model Results

### Logistic Regression
- Precision: **80%**  
- Recall: **83%**  
- F1-Score: **80%**  
- Accuracy: **83%**  

### Decision Tree (after feature engineering)
- AUC: **93.8%**  
- Precision: **87%**  
- Recall: **90.4%**  
- F1-Score: **88.7%**  
- Accuracy: **96.2%**  

### Random Forest
- Slightly outperformed Decision Tree across all metrics  

---

## ✅ Conclusion & Recommendations
The analysis confirms that **employee attrition is strongly linked to being overworked**.  
To improve retention, HR should:

1. Cap the number of projects assigned per employee  
2. Consider promotions for employees with 4+ years of tenure  
3. Reward or compensate employees for longer working hours  
4. Communicate overtime policies and workload expectations clearly  
5. Promote healthy work culture through discussions and feedback sessions  
6. Use fair performance evaluations that don’t solely favor excessive overtime  

---

## 🚀 Next Steps
- Deploy the best-performing model (Random Forest) as a predictive tool for HR  
- Conduct further qualitative research (e.g., employee surveys) to validate insights  
- Explore additional feature engineering and advanced ensemble models  
