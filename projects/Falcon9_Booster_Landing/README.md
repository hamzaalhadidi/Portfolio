# 🚀 Falcon 9 Booster Landing Prediction

## 📌 Overview
This project focuses on predicting the landing success of **SpaceX Falcon 9 first-stage boosters** using Machine Learning techniques.  
By analyzing historical launch data such as payload mass, launch site, orbit type, and flight history, the project aims to identify the key factors that influence successful booster landings.

The motivation behind this project is to support **cost-effective and sustainable space missions** by improving the reliability of reusable rocket technology.

---

## ❓ Problem Statement
Reusable rocket boosters significantly reduce launch costs, but their landing success depends on many dynamic factors.  
The challenge is to accurately predict whether a Falcon 9 booster will land successfully based on historical launch and mission data.

This project formulates the problem as a **binary classification task**:
- **1** → Successful Landing  
- **0** → Unsuccessful Landing  

---

## 📊 Dataset
The dataset was collected from **public and reliable sources**:
- **SpaceX API** – Historical Falcon 9 launch data
- **Wikipedia** – Supplementary booster and mission information

### Key Features:
- Payload Mass  
- Launch Site  
- Orbit Type  
- Flight Number  
- Booster Reuse Information  
- Landing Pad  
- Booster Block Version  

### Data Preprocessing:
- Handling missing values (mean & mode imputation)
- One-hot encoding for categorical variables
- Feature engineering to improve model performance
- Correlation analysis to reduce redundancy

---

## 🧠 Models Used
Multiple supervised Machine Learning models were trained and evaluated:

- **Logistic Regression**
- **Decision Tree Classifier**
- **Support Vector Machine (SVM)**
- **K-Nearest Neighbors (KNN)**

### Evaluation Metrics:
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Jaccard Score  

---

## 📈 Results
- **Decision Tree** achieved the best performance with an accuracy of **~89%**
- Payload Mass, Launch Site, and Orbit Type were identified as the most influential features
- Model performance improved with increased flight history, reflecting SpaceX’s learning curve

The results align with real-world observations where landing success rates increased significantly over time.

---

## 🛠️ Tools & Technologies
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook  
- **Visualization:** Statistical plots & correlation heatmaps  

---

## ▶️ How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/hamzaalhadidi/portfolio.git
