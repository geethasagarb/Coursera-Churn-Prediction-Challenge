# **Coursera - Data Science Challenge - Customer Churn Prediction**

![Churn-prediction](https://github.com/user-attachments/assets/68ff8c28-209c-4471-ad87-0ad01c87c1df)

```mermaid
flowchart TB
    %% Data Sources
    subgraph "Data Sources"
        train["train.csv"]:::dataFile
        test["test.csv"]:::dataFile
        desc["data_descriptions.csv"]:::dataFile
    end

    %% Jupyter Notebook Environment
    jnb["Jupyter Notebook Environment (ChurnPrediction.ipynb)"]:::notebook

    %% Processing Modules inside the Notebook Pipeline
    preproc["Data Cleaning & Preprocessing\n(Handles missing values, categorical conversion, One-Hot Encoding via ColumnTransformer)"]:::process
    feat["Feature Engineering\n(Generates features from subscription details and usage patterns)"]:::process
    model["Model Training & Evaluation\n(Logistic Regression with hyperparameters, ROC AUC evaluation)"]:::model

    %% Output and Business Outcome Components
    output["Prediction Output\n(prediction_submission.csv)"]:::dataFile
    business["Business Insights\n(Churn Intervention Strategies)"]:::business
    doc["Documentation\n(README.md)"]:::doc

    %% Data Flow
    train --> jnb
    test  --> jnb
    desc  --> jnb
    jnb --> preproc
    preproc --> feat
    feat --> model
    model --> output
    output --> business
    output --> doc

    %% Click Events
    click train "https://github.com/geethasagarb/coursera-churn-prediction-challenge/blob/main/train.csv"
    click test "https://github.com/geethasagarb/coursera-churn-prediction-challenge/blob/main/test.csv"
    click desc "https://github.com/geethasagarb/coursera-churn-prediction-challenge/blob/main/data_descriptions.csv"
    click jnb "https://github.com/geethasagarb/coursera-churn-prediction-challenge/blob/main/ChurnPrediction.ipynb"
    click output "https://github.com/geethasagarb/coursera-churn-prediction-challenge/blob/main/prediction_submission.csv"
    click doc "https://github.com/geethasagarb/coursera-churn-prediction-challenge/blob/main/README.md"

    %% Styles
    classDef dataFile fill:#ffefba,stroke:#d35400,stroke-width:2px;
    classDef notebook fill:#d6eaf8,stroke:#2e86c1,stroke-width:2px;
    classDef process fill:#d5f5e3,stroke:#27ae60,stroke-width:2px;
    classDef model fill:#fdebd0,stroke:#e67e22,stroke-width:2px;
    classDef business fill:#e8f8f5,stroke:#16a085,stroke-width:2px;
    classDef doc fill:#fadbd8,stroke:#c0392b,stroke-width:2px;
```




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

---

### **How the Business Problem is Solved with Logistic Regression**  

The core business problem was to **identify customers at high risk of churning** from the video streaming service. By using a **Logistic Regression model with feature engineering and preprocessing**, we achieved the following key outcomes:

 **Early Churn Prediction**:  
- The model predicts **churn likelihood for each customer**, allowing proactive retention strategies.  
- With a **75.1% ROC AUC score**, it effectively differentiates between customers likely to churn vs. stay.  

 **Data-Driven Decision Making**:  
- The model provides insights into **which customer segments** (e.g., payment methods, subscription types, content preferences) are more likely to churn.  
- This helps in **tailoring marketing efforts** and **offering personalized retention incentives**.  

 **Cost Reduction & Revenue Growth**:  
- **Preemptive retention strategies** (e.g., discounts, content recommendations) can be targeted at high-risk users.  
- Preventing churn directly translates to **higher customer lifetime value (CLV)** and **reduced acquisition costs**.  

 **Scalability & Automation**:  
- The pipeline-based model can **easily be updated** with new data, making it scalable for future use.  
- It can be deployed as an **API or integrated into a CRM system** for **real-time churn prediction**.  

### **Conclusion**  
This solution aligns with the business objective by **enabling strategic interventions** before customers churn, leading to **higher retention, improved profitability, and sustained user engagement**. 

---

## **Tools & Technologies Used**
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn  
- **Machine Learning:** Logistic Regression, OneHotEncoder, ColumnTransformer  
- **Development Environment:** Jupyter Notebook  

---

## **Link to Coursera Data Science Challenge**
For more details and to view the challenge notebook, visit the following link:  
[Coursera Data Science Challenge - Churn Prediction](https://hub.labs.coursera.org:443/connect/sharedzfcxmnxr?forceRefresh=false&path=%2Fnotebooks%2FChurnPrediction.ipynb&isLabVersioning=file-prep)

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
