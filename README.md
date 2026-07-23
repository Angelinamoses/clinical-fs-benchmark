# Clinical Feature Selection Benchmark

A single-dataset research benchmark for comparing feature selection methods in clinical machine learning using the Breast Cancer Wisconsin Diagnostic dataset.

This project evaluates standard feature selection methods together with a simple clinically guided relevance layer to study the balance between predictive performance, reproducibility, feature stability, and clinical usefulness.

---

## Research Objective

The objective of this project is to compare feature selection methods for clinical prediction and assess:

- predictive performance
- reproducibility across resampling
- feature stability
- clinical relevance of selected features

This repository demonstrates the workflow on **one dataset only** as a controlled sample implementation before extending to multiple clinical datasets.

---

## Dataset

The sample study uses the **Breast Cancer Wisconsin Diagnostic Dataset** from `scikit-learn`.

This dataset is used because it is:
- binary classification
- clean and easy to reproduce
- suitable for a beginner-friendly but professional workflow
- appropriate for demonstrating the full pipeline on a single dataset

---

## Feature Selection Methods

The following feature selection methods are included:

- Feature Selection Methods

- **ANOVA**
- **mRMR**
- **Random Forest Feature Importance**
- **LASSO**
- **Boruta**


---

## Predictive Models

The following models are used after feature selection:

- **Logistic Regression**
- **Random Forest**
- **XGBoost**

---

## Clinical Relevance Layer

To make the workflow clinically meaningful, a simple **clinical relevance matrix** is added after statistical feature selection.

This layer assigns weights to features based on their relevance to breast cancer literature and clinical interpretation.

The purpose is to:
- keep clinically meaningful features
- downweight weakly interpretable features
- improve the clinical validity of the final selected subset

This is a simplified proxy for a clinical ontology layer and is intended for the sample implementation only.

---

## Evaluation Metrics

The following metrics are reported:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

In addition, the project evaluates:

- **Feature Stability** using Jaccard similarity
- **Reproducibility** using repeated stratified cross-validation

---

## Workflow

The notebook follows this pipeline:

1. Load the breast cancer dataset
2. Preprocess the data
3. Split the data into training and testing sets
4. Apply feature selection methods
5. Apply the clinical relevance layer
6. Train predictive models
7. Evaluate model performance
8. Measure feature stability
9. Compare methods in a final summary table

---

## Repository Structure

```text
clinical-fs-benchmark/
│
├── notebooks/
│   └── 01_breast_cancer_feature_selection_benchmark.ipynb
│
├── src/
│   ├── data_loader.py
│   ├── preprocessing.py
│   ├── feature_selection.py
│   ├── clinical_relevance.py
│   ├── models.py
│   ├── evaluation.py
│   └── stability.py
│
├── results/
│   ├── tables/
│   ├── figures/
│   └── metrics/
│
├── README.md
├── requirements.txt
├── .gitignore
└── main.py
