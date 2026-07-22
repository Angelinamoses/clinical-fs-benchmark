# Clinical Feature Selection Benchmark

## Description
A comparative study of feature selection methods for clinical prediction using the Breast Cancer Wisconsin Diagnostic dataset.

## Objective

To evaluate feature selection methods based on:

* predictive performance
* reproducibility
* feature stability
* clinical relevance

## Dataset

Breast Cancer Wisconsin Diagnostic dataset from scikit-learn.

## Methods

* ANOVA
* LASSO
* RFE
* Random Forest importance

## Models

* Logistic Regression
* Random Forest
* SVM

## Evaluation

* Accuracy
* Precision
* Recall
* F1
* ROC-AUC
* Jaccard stability

## Clinical relevance layer

A proxy clinical relevance matrix based on literature-guided feature importance.

## Workflow

A simple numbered pipeline from loading data to final comparison.

## Limitations

* this is a sample on one dataset
* clinical relevance is proxy-based
* multi-dataset validation comes later
