# Water Potability Classification Project

##  Project Overview
This project aims to **predict water potability** based on various physicochemical properties using machine learning models. The dataset consists of water quality parameters, and the goal is to develop models that effectively classify whether a given water sample is **potable (safe to drink) or not**.

## Models Implemented
We trained and evaluated **two different models**, each utilizing different **regularization techniques** and **optimizers** to compare performance:

1️⃣ **L1 Regularization with Adam Optimizer (Your Model)**  
2️⃣ **L2 Regularization with SGD Optimizer (Colleague's Model)**  

Both models are assessed based on **accuracy, precision, recall, F1-score, and loss curves**.

---

## Table of Model Comparisons

| Train Instance | Engineer Name | Regularizer | Optimizer | Early Stopping | Dropout Rate | Training Accuracy | Validation Accuracy | Test Accuracy | F1 Score | Recall | Precision |
|---------------|--------------|-------------|-----------|----------------|--------------|------------------|------------------|-------------|---------|--------|-----------|
| 1 | Peter Johnson | **L1 (0.003)** | **Adam (lr=0.0001)** | Patience=15, monitor='val_loss' | 0.3 | **0.4068** | **0.9267** | **0.8800** | **0.8767** | **0.8205** | **0.9412** |
| 2 | Ines Irikezi | **L2 (0.003)** | **SGD (lr=0.001, momentum=0.9)** | Patience=10, monitor='val_loss' | 0.25 | TBD | TBD | TBD | TBD | TBD | TBD |

🔹 **Note:**  
- The **second row (colleague’s model) will be updated** once training is complete.  

---

## Performance Analysis
**L1 Regularization + Adam** performed well with a **high validation accuracy (92.67%) and test accuracy (88%)**, suggesting **good generalization**.  
**Precision (94.12%) is high**, meaning **low false positives**—the model rarely classifies unsafe water as safe.  
**Recall (82.05%) is slightly lower**, meaning it **misses some potable water samples** (false negatives).  
**Next Steps:** Comparing against the **L2 + SGD model** to determine which generalizes better.

---

## Project Structure

📁 Water-Potability-Classification 
│── 📄 README.md 
│── 📄 requirements.txt # Dependencies required for the project 
│── 📂 data/ 
│── 📂 notebooks/ # Jupyter Notebooks for training and evaluation 
│── 📄 Peter_Johnson_Water_Quality_Model.ipynb
│── 📄 colleague_model.ipynb # Colleague's trained model (to be completed) 
│── 📂 reports/ # Analysis reports and performance metrics 
│── 📂 plots/ # Loss & accuracy curves, confusion matrices 
│── 📂 src/ # Python scripts for preprocessing & modeling 
│── 📄 LICENSE # Open-source license information


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
colleague_model.ipynb (for L2 + SGD)

### **3️⃣ Evaluate the Models**
Run all cells in the notebooks.
View loss curves, accuracy metrics, and confusion matrices.

## Visualizations
We have included performance plots to track model training progress:

Training Loss Curve	Accuracy Curve
🔹 The confusion matrices and classification reports provide deeper insights into model performance.

## Contributors
Peter Johnson (Max Prodigy): Trained L1 + Adam model.
Colleague: Training L1 + SGD model.
Instructor: Providing feedback and project guidelines.



