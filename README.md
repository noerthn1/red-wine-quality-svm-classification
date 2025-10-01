# 🍷 Red Wine Quality Classifications with SVM

## 📌 Project Overview
This project applies Support Vector Machines (SVM) to classify wines as good or not good based on their physicochemical properties.

The dataset comes from the UCI Machine Learning Repository Wine Quality (https://archive.ics.uci.edu/dataset/186/wine+quality)

## 🎯 Goal
- Predict whether a wine is high quality (≥7) or low quality (<7).
- Explore the performance of different SVM kernels.
- Handle class imbalance and evaluate beyond accuracy.

## 📊 Dataset
- Features: 11 physicochemical attributes (e.g., acidity, sugar, pH, alcohol).
- Target: Wine quality score (converted to binary: good vs. not good).
- Size: ~6,500 samples.

## ⚙️Method
1. **Exploratory Data Analysis (EDA)**
    - Checked distributions, correlations, and class imbalance.
    
2. **Baseline Model: Linear SVM**
   - High accuracy but failed to detect minority class (recall = 0).

3. **RBF Kernel SVM**
    - Better performance, but minority recall was still low.

4. **Hyperparameter Tuning (GridSearchCV)**
    - Tuned C and gamma for RBF kernel.
    - Improved minority recall to 68% while keeping high accuracy.

## 📈 Results
| Model                 | Accuracy | Recall (Minority) | F1 (Minority) |
| --------------------- | -------- | ----------------- | ------------- |
| Linear SVM (baseline) | 0.85     | 0.00              | 0.00          |
| RBF SVM (default)     | 0.88     | 0.26              | 0.38          |
| RBF SVM (tuned)       | **0.90** | **0.68**          | **0.67**      |

## ⚙️Tools
- Python 3.12
- Scikit-learn
- Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook

## 🧠 What I learned :
- Why accuracy isn’t enough for imbalanced datasets.
- How kernel choice impacts SVM performance.
- The importance of hyperparameter tuning (C and gamma).
- How to present machine learning results in a clear way.
