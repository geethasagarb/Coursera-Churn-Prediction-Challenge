# **Coursera - Data Science Challenge - Customer Churn Prediction**

![0*d58iZ6esNNcfntQ7](https://github.com/user-attachments/assets/124de62d-2f90-4343-aa0d-25ada771c155)


## **Project Overview**  
This project focuses on predicting customer churn for a video streaming service using machine learning. I built a **Logistic Regression model** with **feature engineering and pipeline-based preprocessing**, achieving a **ROC AUC score of 75.1%**. The goal is to identify high-risk churn customers early, enabling the business to take proactive retention measures and reduce revenue loss.


---

## **Dataset Details**  
- **Training Data:** 243,787 records  
- **Test Data:** 104,480 records  
- **Features:** Subscription details, payment methods, content preferences, usage behavior, and demographics  
- **Target Variable:** `Churn` (Binary: 1 = Churn, 0 = Retained)  

---

## **Approach & Methodology**  

### **1. Data Cleaning & Preprocessing**
- Handled missing values and ensured data consistency.
- Converted binary categorical variables (`Yes/No`) into numeric form.
- Applied **One-Hot Encoding** to categorical features using `ColumnTransformer`.

### **2. Feature Engineering**
- Engineered relevant features from subscription type, user activity, and preferences.
- Created new insights from existing attributes to improve model performance.

### **3. Model Development**
- Used **Logistic Regression** within a **pipeline** to streamline preprocessing and training.
- Optimized hyperparameters (`max_iter = 1000`, `C=1.0`, `solver=lbfgs`).
- Evaluated model performance using **ROC AUC score**.

### **4. Results & Business Impact**
- Achieved a **75.1% ROC AUC score**.
- Provided insights to help the business implement **targeted retention strategies** and reduce customer churn.
- ![Screenshot 2025-03-21 at 04 50 43](https://github.com/user-attachments/assets/1033837d-47f3-431b-80d2-422ae5ae7bd9)


---

## **Key Findings**
- **Higher watchlist sizes and longer viewing hours** correlate with lower churn rates.
- **Payment method and subscription type** significantly impact churn behavior.
- **Personalized retention efforts** for high-risk customers can enhance customer lifetime value.

---

## **Tools & Technologies Used**
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn  
- **Machine Learning:** Logistic Regression, OneHotEncoder, ColumnTransformer  
- **Development Environment:** Jupyter Notebook  

---

## **Next Steps**
- Experiment with **alternative models** (e.g., Random Forest, XGBoost) to improve accuracy.  
- Perform **feature selection** to optimize model efficiency.  
- **Deploy the model** as an API or integrate it into a business dashboard.  

---

## **How to Run the Project**
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-github-username/churn-prediction.git
   cd churn-prediction
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook to train the model and generate predictions.  

---
