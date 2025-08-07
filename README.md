# 🧪 Experiment 1: KNN Algorithm for Iris Flower Classification

This repository contains the implementation and evaluation of a **K-Nearest Neighbors (KNN)** classification model on the popular **Iris dataset**, as part of the Machine Learning coursework at **Harbin Institute of Technology, Shenzhen**.

> **Author**: Ilkin Masimov  
> **Student ID**: 24SF51099  
> **Experiment Date**: 2025-05-09

---

## 📁 Project Structure

- `KNN_for_Iris.ipynb` — Main Jupyter Notebook
- `Experiment1_24SF51099_Ilkin Masimov.pdf` — Full experiment report with plots and results
- `README.md` — Project documentation

---

## 🖥️ 1. Environment Setup

- Environment: Jupyter Notebook via Anaconda (pre-installed on macOS)
- Libraries used:
  - `numpy`, `pandas`
  - `scikit-learn`
  - `plotly` (for interactive visualization)

---

## 📊 2. Dataset

- **Dataset**: Iris dataset from `sklearn.datasets.load_iris()`
- **Features**:
  - Sepal Length, Sepal Width
  - Petal Length, Petal Width
- **Classes**:
  - Setosa, Versicolor, Virginica
- 150 samples in total

---

## 🔍 3. Data Exploration

- Conducted a correlation analysis using heatmaps.
- **Key insight**: Petal features (length and width) show high correlation (> 0.95), making them highly discriminative for classification.
- Visual comparisons between:
  - Sepal Length vs Width
  - Petal Length vs Width (stronger class separation)

---

## 🧠 4. Model Training

- Model: **K-Nearest Neighbors**
- Training/Test Split: 70/30
- Initial configuration:
  - `k=3`
  - Distance: Euclidean
- Accuracy: **95.56%**

---

## 📈 5. Model Evaluation

- Accuracy for different `k` values from 1 to 10.
- Feature importance comparison:
  - Sepal-only: ~73.33%
  - Petal-only: ~97.78%
- Best result on a single split:
  - Manhattan Distance, `k=3`, test_size=0.25, random_state=42 → **100% Accuracy**
- **Cross-Validation (5-fold)**:
  - Accuracy: **96% ± 0.0249**
  - Indicates better generalization and avoids split bias.

---

## ✅ 6. Conclusion

- **Initial model**: 95.56% accuracy (good)
- **Best model**: 100% (but possibly overfitting)
- **Cross-validated model**: 96% (reliable)
- **Takeaway**: Petal features dominate in predictive power. Cross-validation is crucial for reliable evaluation, especially with small datasets.

---

## 🚀 Getting Started

To run the notebook:

1. Install Anaconda: https://www.anaconda.com/download
2. Clone the repo:
   ```bash
   git clone https://github.com/your-username/knn-iris-classification.git
   cd knn-iris-classification
   ```
3. Launch Jupyter:
   ```bash
   jupyter notebook
   ```
4. Open and run `KNN_for_Iris.ipynb`

---

## 📌 Notes

- KNN is a **lazy learner**, making it simple yet powerful for small datasets.
- This project demonstrates not only classification, but also model tuning, validation, and feature importance analysis.