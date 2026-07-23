# Hotel Booking Cancellation Prediction Using Machine Learning

## Project Overview

This project develops a machine learning pipeline to predict whether a hotel reservation will be canceled before the guest's scheduled arrival. The analysis uses the **Hotel Booking Demand** dataset from Kaggle and follows the **CRISP-DM (Cross Industry Standard Process for Data Mining)** methodology, including data exploration, feature engineering, model development, evaluation, and business recommendations.

Booking cancellations can significantly impact hotel revenue, staffing, and occupancy planning. By accurately identifying reservations with a high likelihood of cancellation, hotels can implement proactive strategies that improve operational efficiency and reduce financial losses.

---

## Objectives

The primary objectives of this project are to:

* Explore the Hotel Booking Demand dataset through exploratory data analysis (EDA).
* Identify factors associated with booking cancellations.
* Clean and preprocess the data for machine learning.
* Engineer meaningful features to improve predictive performance.
* Develop and compare multiple machine learning models.
* Evaluate model performance using standard classification metrics.
* Provide business recommendations based on the model results.

---

## Dataset

**Dataset:** Hotel Booking Demand

**Source:** Kaggle

The dataset contains **119,390 hotel reservations** collected from both **City Hotels** and **Resort Hotels** between **2015 and 2017**. It includes booking details, customer information, pricing data, and historical reservation behavior.

**Target Variable**

* `is_canceled`

  * `0` = Booking was not canceled
  * `1` = Booking was canceled

---

## Project Workflow

This project follows the CRISP-DM framework:

1. Business Understanding
2. Data Understanding
3. Exploratory Data Analysis
4. Data Preparation
5. Feature Engineering
6. Model Development
7. Model Evaluation
8. Business Recommendations

---

## Machine Learning Models

The following models will be developed and compared:

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting (or XGBoost, if applicable)

Model performance will be evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC
* Confusion Matrix
* Cross-Validation

---

## Repository Structure

```text
Hotel-Booking-Cancellation-Prediction/
│
├── data/
│   └── hotel_bookings.csv
│
├── figures/
│   ├── figure1_class_distribution.png
│   ├── figure2_hotel_type.png
│   └── ...
│
├── src/
│   ├── eda.py
│   ├── feature_engineering.py
│   ├── modeling.py
│   └── evaluation.py
│
├── reports/
│   ├── Midpoint_Report.pdf
│   └── Final_Presentation.pptx
│
├── README.md
└── requirements.txt
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn

---

## Current Progress

* ✓ Dataset selected
* ✓ Exploratory Data Analysis
* ✓ Data cleaning and preprocessing
* ✓ Feature engineering

### Upcoming Work

* Build and compare machine learning models
* Hyperparameter tuning
* Model evaluation
* Business recommendations
* Final presentation

---

## Expected Business Impact

Accurate prediction of booking cancellations can help hotels:

* Improve occupancy forecasting
* Reduce revenue loss from cancellations
* Optimize overbooking strategies
* Improve staffing and resource planning
* Develop targeted customer retention strategies

---

## Author

**Aditi Shah**

Graduate Machine Learning Course Project
