# Breast Cancer Detection using PCA and Predictive Modeling

This repository contains an end-to-end analysis of the Wisconsin Breast Cancer Diagnostic dataset. It focuses on early detection of malignant tumors using shape-based features extracted from cell nuclei, with PCA used for dimensionality reduction and multiple classification models evaluated for performance.

📬 _This project supports the insights shared in the Substack post: [Breast Cancer in 2025](https://aixme.substack.com/p/breast-cancer-in-2025)_

![image](https://github.com/user-attachments/assets/54331042-2d36-47cb-adc0-14ca7fa4d791)
<sub>Image courtesy of [The Harvard Gazette](https://news.harvard.edu/gazette/story/2022/09/researchers-report-dramatic-rise-in-early-onset-cancers/)</sub>

## Project Structure

- `eda.ipynb`: Exploratory Data Analysis — feature understanding, class imbalance, visualizations
- `datamodels.ipynb`: PCA transformation, handling class imbalance, model building and evaluation
- `pca_data.csv`: PCA-transformed dataset used for modeling
- `requirements.txt`: List of dependencies

---

## Dataset

- Source: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)
- 569 samples, 30 numeric features + 1 target
- Target: `Diagnosis` (0 = Benign, 1 = Malignant)

---

## Modeling Approach

To address the class imbalance and maximize detection of malignant tumors, we applied two strategies:

**Data-Level (Resampling):**
- SMOTE + Logistic Regression
- SMOTE + Support Vector Classifier
- SMOTE + Random Forest

**Algorithm-Level (Built-in Balancing):**
- Balanced Random Forest
- Easy Ensemble

Models were evaluated using accuracy, precision, recall (sensitivity), specificity, and F1 score.

---

## Results

Key results are summarized in the blog post [here](https://aixme.substack.com/p/breast-cancer-in-2025#:~:text=are%20the%20results..-,Results,-Before%20we%20jump).

Simpler models (Logistic Regression, SVC with SMOTE) showed strong balanced performance with easier deployment potential in clinical settings.

---

## Installation

```bash
pip install -r requirements.txt
```

---

## Acknowledgments

- UCI Machine Learning Repository
- [imbalanced-learn](https://imbalanced-learn.org/)
---
