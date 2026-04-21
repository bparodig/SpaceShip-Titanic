# Spaceship Titanic - Improving Model Reliability Through Better Machine Learning Workflow

## Project Overview

This project was developed using the Kaggle **Spaceship Titanic** dataset. The objective was to predict whether a passenger was transported to another dimension.

More than a classification project, this became a practical exercise in understanding an important machine learning lesson:

**A strong local validation score does not always translate into strong real-world performance.**

The project was completed in two stages:

1. Initial notebook with a less structured workflow
2. Improved notebook with better preprocessing, reduced data leakage, and stronger generalization

---

## Objective

Predict the target variable:

* `Transported = True`
* `Transported = False`

---

## Dataset

Source: Kaggle - Spaceship Titanic Competition

The dataset includes passenger information such as:

* HomePlanet
* CryoSleep
* Cabin
* Destination
* Age
* VIP status
* Spending categories
* Passenger name

---

## Phase 1 - Initial Model

The first version of the project used a simpler workflow:

* Manual preprocessing
* Basic feature engineering
* Standard train/test validation
* No structured preprocessing pipeline

### Results

* Notebook Accuracy: ~0.82
* Kaggle Public Score: ~0.75

### Main Observation

Although the local score looked promising, the model did not generalize well to unseen data.

This highlighted common issues such as:

* Data leakage
* Inconsistent preprocessing between train and test data
* Overly optimistic local validation

---

## Phase 2 - Improved Workflow

The second version of the project was rebuilt using a more reliable machine learning process.

### Improvements Implemented

#### Proper Data Splitting Before Preprocessing

Train/test split was performed before transformations to prevent leakage.

#### Missing Value Handling

* Numerical variables: median imputation
* Categorical variables: most frequent value imputation

#### Encoding

* OneHotEncoder with unknown-category handling

#### Validation Strategy

* StratifiedKFold
* GridSearchCV

#### Feature Engineering

Created additional predictive features:

* `TotalGastos`
* `HasGasto`
* `Cryo_NoGasto`
* `Deck`, `Num`, `Side`

#### Model Comparison

Evaluated:

* Random Forest
* XGBoost

---

## Final Results

### Best Model: XGBoost

* Notebook Accuracy: ~0.81
* Kaggle Public Score: **0.80313**

---

## Why the Second Version Performed Better

Even though notebook accuracy was slightly lower than the first version, the Kaggle score improved significantly.

This indicates:

* Better generalization to unseen data
* More realistic validation process
* Smaller gap between local and real-world performance

---

## Key Learnings

This project helped strengthen practical skills in:

* Preventing data leakage
* Building preprocessing workflows
* Feature engineering
* Cross validation
* Hyperparameter tuning
* Model comparison
* Real-world model evaluation

---

## Final Insight

The most valuable outcome of this project was not only the final score, but learning that reliable machine learning workflows matter more than inflated local metrics.

---


## Author

Bruno Parodi

Industrial Engineer transitioning into Data Science with a focus on practical machine learning projects and continuous improvement.


Industrial Engineer transitioning into Data Science, focused on practical machine learning projects and continuous improvement.

---:::
