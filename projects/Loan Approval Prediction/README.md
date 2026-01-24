# 🏦 Loan Approval Prediction using Deep Learning

## 📌 Overview
This project focuses on automating the loan eligibility process using **Deep Learning (Neural Networks)**. By analyzing applicant details such as income, education, marital status, and credit history, the system predicts whether a loan application should be approved or rejected.

The motivation behind this project is to assist financial institutions in **mitigating credit risk**, speeding up the manual validation process, and ensuring fair decision-making based on historical data trends.

---

## ❓ Problem Statement
Manual loan processing is time-consuming and prone to human error. For banks, approving risky applicants leads to financial defaults, while rejecting creditworthy applicants results in business loss. 

This project formulates the problem as a **binary classification task**:
- **1 (Approved)** ✅
- **0 (Rejected)** ❌

---

## 📊 Dataset & Workflow
The project is divided into three main stages, each handled in a dedicated Jupyter Notebook:

### 1️⃣ Data Loading & Cleaning (`data_loading_cleaning.ipynb`)
* **Cleaning:** Handled missing values using Median for numerical features and Mode for categorical ones.
* **Feature Engineering:** Processed the `Dependents` column and dropped irrelevant identifiers like `Loan_ID`.
* **Encoding:** Applied **One-Hot Encoding** to transform categorical variables into a machine-readable format.
* **Storage:** Exported processed data as `loan_encoded.csv`.

### 2️⃣ Exploratory Data Analysis (`loan_viz.ipynb`)
* **Visualizations:** Used Seaborn and Matplotlib to identify patterns.
* **Key Findings:** Analyzed the impact of `Credit_History`, `Education`, and `Property_Area` on loan status.
* **Correlation:** Generated a heatmap to understand the relationships between financial features.

### 3️⃣ Modeling & Evaluation (`modeling.ipynb`)
* **Preprocessing:** Scaled features using `StandardScaler` for optimal Neural Network performance.
* **Model Architecture:** Built a **Multi-Layer Perceptron (MLP)** using TensorFlow/Keras with:
    * **Hidden Layers:** Dense layers with ReLU activation.
    * **Regularization:** Dropout layers and L2 regularization to prevent overfitting.
    * **Early Stopping:** Implemented to halt training at the best validation loss.

---

## 🧠 Model Architecture
| Layer | Type | Neurons/Rate | Activation |
| :--- | :--- | :--- | :--- |
| Input | Dense | Input Dim | ReLU |
| Hidden 1 | Dense | 64 | ReLU (+ Dropout 0.3) |
| Hidden 2 | Dense | 32 | ReLU (+ Dropout 0.2) |
| Output | Dense | 1 | Sigmoid |

---

## 📈 Results
- **Accuracy:** ~86% on the test set.
- **ROC-AUC Score:** 0.77
- **Deployment Ready:** The model is saved as `loan_approval_model.keras` and the scaler as `scaler.pkl` for real-time predictions.

---

## 🛠️ Tools & Technologies
* **Language:** Python 3.x
* **DL Framework:** TensorFlow / Keras
* **Data Science:** Pandas, NumPy, Scikit-learn
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook

---

## 🚀 How to Use
1. Clone this repository.
2. Install dependencies: `pip install tensorflow pandas scikit-learn matplotlib seaborn`.
3. Run `modeling.ipynb` to train the model or use the saved `.keras` file for inference.
