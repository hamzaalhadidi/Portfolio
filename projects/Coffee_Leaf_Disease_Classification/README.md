# ☕ Coffee Leaf Disease Classification using CNN

## 📌 Overview
This project focuses on the automated detection and classification of diseases affecting **Coffee plants** using **Deep Learning** and **Computer Vision**. By analyzing digital images of coffee leaves, the system can accurately identify whether a plant is healthy or infected by specific pathogens like **Rust, Miner, or Phoma**.

Early detection of these diseases is crucial for coffee farmers to prevent crop loss, optimize pesticide use, and ensure high-quality coffee production.

---

## ❓ Problem Statement
Coffee crops are highly susceptible to environmental stressors and pests. Identifying these diseases manually requires expert knowledge and constant monitoring.  
This project builds a **Convolutional Neural Network (CNN)** to classify coffee leaf images into **4 distinct categories**:
1. **Healthy** ✅ - Green, vibrant leaves with no signs of infection.
2. **Miner** 🐛 - Leaves damaged by the Coffee Leaf Miner larvae.
3. **Phoma** 🍂 - Leaves affected by Phoma leaf spot (fungal infection).
4. **Rust** 🍄 - Leaves showing orange, powdery spots (Hemileia vastatrix).

---

## 📊 Dataset & Workflow
The project is organized into three specialized Jupyter Notebooks for clarity and modularity:

### 1️⃣ Data Exploration (`data_exploration.ipynb`)
* **Data Loading:** Organized images into training and validation sets with a target size of **256x256** pixels.
* **Visualization:** Displayed a grid of coffee leaf samples to observe the visual patterns of each disease.
* **Metadata:** Saved class names and image configurations into `dataset_info.pkl`.

### 2️⃣ Model Training (`model_training.ipynb`)
* **Preprocessing:** Implemented a rescaling layer to normalize pixel values.
* **Architecture:** Developed a **Deep CNN** featuring:
    * Multiple **Conv2D** layers for pattern recognition (spots, textures).
    * **MaxPooling** layers to reduce spatial dimensions.
    * **Dropout** layers to prevent overfitting on the training data.
* **Optimization:** Used the **Adam optimizer** and monitored accuracy/loss curves to ensure model convergence.

### 3️⃣ Model Inference (`model_inference.ipynb`)
* **Testing:** Loads the trained `.keras` model and the `dataset_info.pkl` to perform predictions.
* **Results:** The script randomly selects test images and outputs:
    * The **Actual Class** vs. **Predicted Class**.
    * The **Confidence Score (%)** of the prediction.

---

## 🧠 Model Architecture
| Layer Type | Purpose |
| :--- | :--- |
| **Rescaling** | Normalizes input images (0-255 to 0-1). |
| **Conv2D + ReLU** | Extracts spatial features and leaf textures. |
| **MaxPooling** | Downsamples the feature maps. |
| **Flatten** | Converts 2D data into a 1D vector. |
| **Dense (Softmax)** | Final layer providing probabilities for the 4 coffee leaf classes. |

---

## 📈 Results
- **High Precision:** The model effectively distinguishes between similar-looking fungal infections (like Rust vs. Phoma).
- **Deployment:** The finalized model is saved as `coffee_disease_model.keras`, making it ready for integration into agricultural mobile apps or drones.

---

## 🛠️ Tools & Technologies
* **Language:** Python
* **DL Framework:** **TensorFlow / Keras**
* **Image Processing:** OpenCV, Pillow
* **Analysis:** NumPy, Matplotlib
* **Environment:** Jupyter Notebook

---

## 🚀 How to Run
1. **Clone the repository.**
2. **Install dependencies:**
   ```bash
   pip install tensorflow numpy matplotlib pillow
