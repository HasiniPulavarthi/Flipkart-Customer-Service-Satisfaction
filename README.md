#  Flipkart CSAT Score Prediction

##  Objective
The objective of this project is to build a machine learning classification model to predict customer satisfaction (CSAT) scores for Flipkart. The model helps identify key factors influencing customer experience and enables improvements in service quality, operations, and customer retention.

---

##  Dataset Overview
The dataset consists of 20 features capturing customer interactions and service-related information.

###  Key Customer Features
- Order_ID  
- Order_Date_Time  
- Customer_City  
- Item_Price  
- Channel_Name  
- Customer_Remarks  

###  Operational Features
- Issue_Reported_at  
- Issue_Responded  
- Survey_Response_Date  
- Product_Category  
- Agent_Name  
- Supervisor  
- Manager  
- Agent_Shift  
- Sub_Category  

###  Target Variable
- **CSAT Score (1–5)**  
  Higher values indicate better customer satisfaction.

---

##  Data Preprocessing & Cleaning
- Converted date columns to datetime format  
- Dropped `Connected_Handling_Time` due to ~99% missing values  
- Removed rows with missing `Order_ID`  
- Handled missing values using appropriate imputation techniques  

---

##  Feature Engineering
- Extracted year, month, day, hour, and minute from `Order_Date_Time`  
- Removed outliers in `Item_Price` using IQR method (~23.85% removed)  
- Applied One-Hot Encoding to categorical features (Channel, Product Category, etc.)  

---

##  Exploratory Data Analysis (EDA)
- Analyzed distribution of CSAT scores and item prices  
- Studied relationships between CSAT and features like:
  - Channel  
  - Category  
  - Response time  
- Evaluated agent performance and shift-based trends  

---

##  Model Building

###  Data Splitting
- Train-Test Split: 80-20  

###  Models Used
- Logistic Regression  
- Decision Tree  
- Random Forest  
- K-Nearest Neighbors  
- Extra Trees Classifier  

###  Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  

---

##  Model Performance
- Extra Trees Classifier performed best  
- Achieved high precision and accuracy  
- Evaluated using Confusion Matrix and ROC-AUC Curve  

---

##  Feature Importance
Key factors influencing customer satisfaction:
- Customer Remarks  
- Issue Responded Time  
- Channel Name  
- Category  

---

##  Key Insights
- Faster issue resolution improves customer satisfaction  
- Certain categories and channels show lower CSAT  
- Customer remarks strongly impact satisfaction  
- Agent performance varies across shifts  

---

##  Conclusion
The model successfully predicts customer satisfaction and provides actionable insights to improve customer experience, optimize service strategies, and enhance retention.

---

##  Future Improvements
- Apply advanced NLP on customer remarks  
- Deploy model as a web application  
- Use real-time data for prediction  

---

##  Tech Stack
- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- Google Colab  
