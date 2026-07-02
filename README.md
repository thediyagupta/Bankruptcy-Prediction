# 💰 Bankruptcy Prediction using Decision Tree & Random Forest (From Scratch)

An end-to-end machine learning project for predicting corporate bankruptcy on a highly imbalanced financial dataset. This project implements **Decision Tree** and **Random Forest** algorithms entirely from scratch using **Python** and **NumPy**, and evaluates multiple techniques for handling class imbalance, including **SMOTE**.

---

## 📌 Overview

Bankruptcy prediction is a binary classification problem where the objective is to identify financially distressed companies before they fail. Since bankrupt companies are rare, the dataset is highly imbalanced, making traditional classification models biased toward the majority class.

This project builds a complete machine learning pipeline covering:

- Data preprocessing
- Feature scaling
- Handling class imbalance
- Decision Tree implementation from scratch
- Random Forest implementation from scratch
- Threshold optimization
- Model evaluation
- Model serialization

---

## ✨ Features

- 🌳 Decision Tree implemented from scratch using NumPy
- 🌲 Random Forest implemented from scratch
- 🎯 Gini Impurity based node splitting
- 🔁 Bootstrap sampling for bagging
- 🎲 Random feature selection at each split
- ⚖️ SMOTE-based oversampling for minority class
- 📊 Standard feature scaling
- 📈 Probability prediction and threshold tuning
- 💾 Save and load trained models using Pickle

---

## 📂 Project Structure

```
.
├── SMOT_Random_Forest_Final_Code.ipynb
├── random_forest_model.pt
├── scaler.pth
└── README.md
```

---

## 🛠 Tech Stack

### Language

- Python

### Libraries

- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Imbalanced-learn
- Pickle

---

## 📊 Dataset

The project uses a bankruptcy prediction dataset containing financial indicators of companies.

**Problem Type**

- Binary Classification

**Class Distribution**

- Bankrupt : Non-Bankrupt ≈ **3 : 97**

Due to the severe class imbalance, oversampling techniques are required to improve minority-class detection.

---

## ⚙️ Machine Learning Pipeline

### 1. Data Preprocessing

- Load dataset
- Train-test split
- Standardize numerical features using `StandardScaler`

---

### 2. Handling Class Imbalance

SMOTE (Synthetic Minority Oversampling Technique) is applied only to the training set to generate synthetic minority-class samples.

---

### 3. Decision Tree (From Scratch)

Implemented using:

- Gini Impurity
- Recursive tree construction
- Maximum depth
- Minimum samples per leaf
- Best feature-threshold search

---

### 4. Random Forest (From Scratch)

Random Forest is built using:

- Bootstrap sampling
- Multiple Decision Trees
- Random feature selection
- Majority voting
- Probability prediction

Configurable parameters include:

- Number of trees
- Maximum depth
- Minimum leaf size
- Maximum features
- Feature bootstrapping

---

### 5. Threshold Optimization

Instead of using the default probability threshold of **0.50**, different thresholds are evaluated to improve minority-class recall.

The optimal threshold is selected based on the trade-off between:

- Recall
- Precision
- G-Mean

---

## 📈 Model Evaluation

The project evaluates model performance using:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix
- Classification Report
- G-Mean

---

## 📌 Results

After applying SMOTE and threshold optimization, the Random Forest model achieved:

| Metric | Score |
|---------|-------|
| Recall | **69.7%** |
| ROC-AUC | **0.94** |
| G-Mean | **0.82** |

The optimized model significantly improves bankruptcy detection while maintaining strong overall classification performance.

---

## 💾 Model Persistence

The trained model and preprocessing objects are saved using Pickle.

```
random_forest_model.pt
scaler.pth
```

These can later be loaded for inference without retraining.

---

## 🚀 Future Improvements

- Hyperparameter tuning
- Cross-validation
- Feature importance visualization
- Precision-Recall curve
- ROC curve visualization
- FastAPI deployment
- Interactive prediction dashboard
- Explainability using SHAP/LIME

---

## 📚 Concepts Used

### Machine Learning

- Binary Classification
- Ensemble Learning
- Decision Trees
- Random Forest
- Bagging
- Bootstrap Sampling

### Imbalanced Learning

- SMOTE
- Class Imbalance
- Threshold Optimization

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Confusion Matrix
- G-Mean

### Python

- Object-Oriented Programming
- NumPy
- Pandas
- Pickle

---

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience in:

- Implementing tree-based algorithms from scratch
- Understanding ensemble learning techniques
- Handling highly imbalanced datasets
- Optimizing classification thresholds
- Building reproducible machine learning pipelines
- Evaluating models using multiple performance metrics

---

## 📄 License

This project is licensed under the MIT License. Feel free to use, modify, and distribute this project for educational and non-commercial purposes.

See the `LICENSE` file for more details.