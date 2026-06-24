# League of Legends Match Outcome and Player Tier Classification

## Overview

This project explores machine learning approaches for analyzing League of Legends gameplay data. The goal was to investigate which gameplay statistics are most predictive of match outcomes and player skill levels.

Two classification problems were studied:

1. Binary Classification – Predict whether a player's team wins or loses a match.
2. Multi-Class Classification – Predict a player's ranked tier based on in-game performance metrics.

The project was completed as part of CSE 5104: Data Mining.

---

## Dataset

The dataset contains League of Legends match statistics, including gameplay-related features such as:

* Kills
* Deaths
* Assists
* Gold earned
* Damage dealt
* Damage taken
* Vision-related statistics
* Ranked tier information

After preprocessing, irrelevant identifiers were removed and meaningful gameplay features were selected for model training.

---

## Methods

### Data Preprocessing

* Removed invalid or corrupted records
* Converted target variables into classification labels
* Removed irrelevant identifiers
* Selected gameplay-related numerical features
* Split data into training and validation sets

### Classification Models

#### K-Nearest Neighbors (KNN)

Hyperparameter tuned:

* Number of neighbors (k)

Tested values:

* 3, 5, 7, 9, 11

#### Random Forest

Hyperparameter tuned:

* Number of trees (n_estimators)

Tested values:

* 50, 100, 150, 200, 300

### Model Selection

Five-fold cross-validation was used to select optimal hyperparameters.

### Dimension Reduction

Principal Component Analysis (PCA) was applied to reduce the feature space by approximately 50%.

Models were retrained and evaluated on both the original and reduced datasets.

---

## Results

### Binary Classification (Match Outcome Prediction)

Best Model:

* Random Forest

Validation Accuracy:

* 79.26%

### Multi-Class Classification (Player Tier Prediction)

Best Model:

* Random Forest

Validation Accuracy:

* 25.7%

### Impact of PCA

PCA reduced model performance in both classification tasks, suggesting that important predictive information was lost during dimensionality reduction.

---

## Key Findings

* Match outcomes can be predicted with relatively high accuracy using gameplay statistics.
* Predicting player rank tiers is significantly more challenging than predicting match outcomes.
* Random Forest consistently outperformed KNN across both classification tasks.
* PCA did not improve performance for this dataset.

---

## Repository Structure

```text
report/
    Project report

presentation/
    Business insights presentation

notebooks/
    Data preprocessing
    Binary classification
    Multi-class classification
    PCA experiments
```

---

## Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Jupyter Notebook

---

## Course Information

Course: CSE 5104 – Data Mining

Project Type: Course Project

Focus Areas:

* Classification
* Hyperparameter Tuning
* Cross Validation
* Dimension Reduction
* Data Mining
* Predictive Analytics
