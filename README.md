# 🚀 Spaceship Titanic - From Overfitting to Reliable Machine Learning Pipeline

## 📌 Project Overview

This project was built using the Kaggle **Spaceship Titanic** dataset. The main objective was to predict whether a passenger was **transported to another dimension**.

Beyond model performance, this project became a practical lesson in one of the most important machine learning concepts:

> **A high notebook score does not always mean a good real-world model.**

The project was developed in two stages:

1. **Initial notebook:** higher validation score, weaker real-world performance
2. **Improved notebook:** cleaner pipeline, reduced data leakage, stronger generalization

---

# 🎯 Objective

Predict the target variable:

* **Transported = True**
* **Transported = False**

---

# 📊 Dataset

Source: Kaggle - Spaceship Titanic Competition

The dataset contains passenger information such as:

* HomePlanet
* CryoSleep
* Cabin
* Destination
* Age
* VIP status
* Spending categories
* Passenger name

---

# 🔍 Phase 1 - Initial Model (Unstructured Approach)

The first version of the project used a more direct workflow:

* Basic preprocessing
* Manual transformations
* Simpler validation structure
* No fully structured preprocessing pipeline

### Results

* **Notebook Accuracy:** ~0.82
* **Kaggle Public Score:** ~0.75

### Key Lesson

Although the local score looked strong, the model did not generalize well to unseen data.

This exposed issues such as:

* Data leakage
* Inconsistent preprocessing
* Over-optimistic validation

---

# 🧠 Phase 2 - Improved Machine Learning Pipeline

A second version of the project was rebuilt with a more professional workflow.

### Improvements Implemented

## ✅ Proper Data Splitting Before Preprocessing

Train/test split was applied before transformations to prevent leakage.

## ✅ Missing Value Handling

Used:

* `SimpleImputer(strategy="median")` for numerical variables
* `SimpleImputer(strategy="most_frequent")` for categorical variables

## ✅ Encoding

Used:

* `OneHotEncoder(handle_unknown="ignore")`

## ✅ Cross Validation

Used:

* `StratifiedKFold`
* `GridSearchCV`

## ✅ Feature Engineering

Created predictive variables such as:

* `TotalGastos`
* `HasGasto`
* `Cryo_NoGasto`
* `Deck / Num / Side`

## ✅ Model Comparison

Compared:

* Random Forest
* XGBoost

---

# 🏆 Final Results

### Best Model: XGBoost

* **Notebook Accuracy:** ~0.81
* **Kaggle Public Score:** **0.80313**

---

# 📈 Why This Version Was Better

Even though notebook accuracy was slightly lower than the first attempt:

* Real-world Kaggle performance improved significantly
* Gap between validation and unseen data became much smaller
* Model became more reliable and realistic

This demonstrates the importance of:

> **Generalization over inflated local scores**

---

# 🧠 Key Learnings

This project helped reinforce practical skills in:

* Data leakage prevention
* Proper preprocessing workflow
* Feature engineering
* Cross validation
* Hyperparameter tuning
* Model comparison
* Real-world model evaluation
* Kaggle competition workflow

---

# 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Jupyter Notebook

---

# 📁 Repository Files

```text
SpaceshipTitanic_v1.ipynb
SpaceshipTitanic_v2.ipynb
README.md
```

---

# 💡 Final Insight

The most valuable outcome of this project was not only the final score, but understanding that:

> Building a trustworthy machine learning pipeline matters more than chasing misleading local accuracy.

---

# Author

Bruno Parodi

Industrial Engineer transitioning into Data Science, focused on practical machine learning projects and continuous improvement.

---:::
