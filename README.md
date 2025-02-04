# Water Potability Classification Project

##  Project Overview
This project aims to **predict water potability** based on various physicochemical properties using machine learning models. The dataset consists of water quality parameters, and the goal is to develop models that effectively classify whether a given water sample is **potable (safe to drink) or not**.

## Models Implemented
We trained and evaluated **two different models**, each utilizing different **regularization techniques** and **optimizers** to compare performance:

1️⃣ **L1 Regularization with Adam Optimizer (Peter Johnson's Model)**  
2️⃣ **L2 Regularization with SGD Optimizer (Inès IKIREZI's Model)**  

Both models are assessed based on **accuracy, precision, recall, F1-score, and loss curves**.

---

## Table of Model Comparisons

| Train Instance | Engineer Name | Regularizer | Optimizer | Early Stopping | Dropout Rate | Training Accuracy | Validation Accuracy | Test Accuracy | F1 Score | Recall | Precision |
|---------------|--------------|-------------|-----------|----------------|--------------|------------------|------------------|-------------|---------|--------|-----------|
| 1 | **Peter Johnson** | **L1 (0.002)** | **Adam (lr=0.0001)** | Patience=15, monitor='val_loss' | 0.3 | **0.4068** | **0.9267** | **0.8800** | **0.8767** | **0.8205** | **0.9412** |
| 2 | **Inès IKIREZI** | **L2 (0.003)** | **SGD (lr=0.001, momentum=0.9)** | Patience=10, monitor='val_loss' | 0.25 | **0.8924** | **0.8642** | **0.8415** | **0.8321** | **0.7893** | **0.8910** |


---

## Performance Analysis
The traditional machine learning model implemented by Inès IKIREZI utilizes a structured approach with L2 regularization and an SGD optimizer. It achieves a high training accuracy of 89.24% and generalizes well with a validation accuracy of 86.42% and a test accuracy of 84.15%. This efficient and interpretable model makes it suitable for real-world applications where model explainability is important.

On the other hand, Peter Johnson's deep learning model uses L1 regularization, dropout layers, and the Adam optimizer to improve generalization. Despite its lower training accuracy (40.68%), the model significantly outperforms in validation (92.67%) and test accuracy (88.00%), demonstrating superior generalization capability. The deep learning approach provides higher predictive power at the cost of increased computational complexity.

---

## Project Structure

📁 Water-Potability-Classification 
│── 📄 README.md 
│── 📄 requirements.txt # Dependencies required for the project

│── 📂 data/
│── 📄 water_potability.csv #Dataset

│── 📂 notebooks/ # Notebooks for training and evaluation 
│── 📄 Peter_Johnson_Water_Quality_Model.ipynb
│── 📄 Inès_IKIREZI_Water_Quality_Colab 




---

## How to Run the Project
To set up and run this project locally:

### **1️⃣ Install Dependencies**
Ensure you have **Python 3.9+** installed, then run:
```bash
pip install tensorflow
```
### **2️⃣ Run the Training Notebooks**
Navigate to the notebooks folder and open:
Peter_Johnson_Water_Quality_Model.ipynb (for L1 + Adam)
Inès_IKIREZI_Water_Quality_Colab (for L2 + SGD)

### **3️⃣ Evaluate the Models**
Run all cells in the notebooks.
View loss curves, accuracy metrics, and confusion matrices.


## Contributors
- Peter Johnson (Max Prodigy): Trained L1 + Adam model.
- Inès IKIREZI (IkireziI): Training L2 + SGD model.
- Instructor: Providing feedback and project guidelines.



