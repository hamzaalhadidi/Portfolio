# ☕ Coffee Leaf Disease Classification using Deep Learning

## 📌 Overview
This project focuses on the automated detection and classification of diseases affecting **Coffee plants** using **Deep Learning (CNN)**. By analyzing digital images of coffee leaves, the system can identify whether a plant is healthy or infected by specific conditions such as **Miner, Phoma, or Rust**.

This tool aims to support coffee farmers by providing a data-driven approach to crop health monitoring, helping to prevent the spread of diseases and improve yield quality.

---

## ❓ Problem Statement
Identifying coffee leaf diseases manually is a labor-intensive task and requires expert agricultural knowledge. Delayed diagnosis can lead to significant financial losses.  
This project builds a **Convolutional Neural Network (CNN)** to classify leaf images into **4 categories**:
1. **Healthy** ✅ - Disease-free coffee leaves.
2. **Miner** 🐛 - Leaves showing tracks from leaf miner larvae.
3. **Phoma** 🍂 - Leaves affected by Phoma fungal spots.
4. **Rust** 🍄 - Leaves infected with Coffee Leaf Rust (orange powdery spots).

---

## 📊 Dataset & Workflow
The pipeline is structured into three specialized Jupyter Notebooks:

### 1️⃣ Data Exploration (`data_exploration.ipynb`)
* **Data Processing:** Loaded images from directories and organized them into batches using `tf.keras.utils`.
* **Standardization:** Images were resized to **256x256** pixels to ensure consistency.
* **Metadata:** Saved class names and configuration to `dataset_info.pkl` for use during inference.

### 2️⃣ Model Training (`model_training.ipynb`)
* **Preprocessing:** Applied pixel rescaling (normalization) to improve training speed.
* **Architecture:** Designed a **Deep CNN** with multiple convolutional and pooling layers to extract spatial features from the leaves.
* **Regularization:** Included **Dropout** layers to ensure the model generalizes well to new, unseen images.
* **Output:** Saved the trained model as `coffee_disease_model.keras`.

### 3️⃣ Model Inference (`model_inference.ipynb`)
* **Validation:** A dedicated script to test the model's accuracy on real-world samples.
* **Visualization:** For any input image, the script displays:
    - **Actual Class:** The true label of the leaf.
    - **Predicted Class:** The model's classification result.
    - **Confidence Score (%):** How certain the model is about its decision.

---

## 🧠 Model Architecture
The model utilizes a **Sequential CNN** structure:
- **Rescaling Layer:** Converts pixel values to the [0, 1] range.
- **Convolutional Layers:** Detects patterns like spots, edges, and leaf textures.
- **Max Pooling:** Reduces computational complexity by downsampling feature maps.
- **Dense Layers:** Fully connected layers that output probabilities for each disease class via **Softmax**.

---

## 📈 Results
- **Efficient Classification:** The model shows high performance in distinguishing between healthy leaves and those with fungal or pest damage.
- **Real-time Potential:** The inference script is optimized to provide predictions with high confidence scores (e.g., >90%).

---

## 🛠️ Tools & Technologies
* **Language:** Python
* **Deep Learning Framework:** **TensorFlow / Keras**
* **Image Processing:** **Pillow (PIL)** (Integrated via Keras preprocessing)
* **Data Science & Viz:** NumPy, Matplotlib
* **Environment:** Jupyter Notebook

---

## 🚀 How to Run
1. **Clone this repository.**
2. **Install requirements:**
   ```bash
   pip install tensorflow numpy matplotlib pillow
