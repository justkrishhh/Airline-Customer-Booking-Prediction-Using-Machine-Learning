## Project Overview

This project focuses on predicting whether a customer will complete an airline booking using Machine Learning. The objective was to help airlines move from reactive to proactive decision-making by identifying customer booking behavior before travel occurs.

Using a dataset containing 50,000 customer booking records, a predictive model was developed to analyze customer behavior, booking characteristics, and travel preferences to determine the likelihood of a booking being completed.

The project follows a complete end-to-end Machine Learning workflow, including data preprocessing, feature engineering, model training, evaluation, and business insight generation.

---

## Business Problem

Airlines often face uncertainty in customer booking behavior, making it difficult to optimize marketing campaigns and forecast demand.

The goal of this project was to:

- Predict which customers are likely to complete a booking
- Understand the key factors influencing booking decisions
- Generate actionable business recommendations
- Improve customer targeting and conversion strategies

---

## Dataset Information

The dataset contains **50,000 customer booking records** and includes customer travel behavior, booking preferences, and journey-related information.

### Key Features Included

- Number of passengers
- Purchase lead time
- Length of stay
- Flight hour
- Flight day
- Route
- Booking origin
- Extra baggage preference
- Preferred seat selection
- In-flight meal preference
- Flight duration
- Booking completion status (Target Variable)

### Target Variable

`booking_complete`

- **1 → Booking completed**
- **0 → Booking not completed**

The dataset was imbalanced, with approximately **15% positive bookings**, requiring additional handling during model training.

---

## Project Workflow

### 1. Data Exploration & Understanding

Performed initial exploratory analysis to understand:

- Dataset structure
- Column data types
- Missing values
- Feature distributions
- Booking completion patterns

Basic statistics and feature inspection were conducted to understand customer behavior and identify preprocessing requirements.

---

### 2. Data Cleaning & Preparation

Prepared the dataset for Machine Learning by performing multiple preprocessing tasks.

#### Flight Day Mapping

The `flight_day` feature was converted from categorical weekday names into numerical values.

Example:

| Day | Encoded Value |
|------|---------------|
| Mon | 1 |
| Tue | 2 |
| Wed | 3 |
| Thu | 4 |
| Fri | 5 |
| Sat | 6 |
| Sun | 7 |

This transformation improved model compatibility.

---

### 3. Feature Engineering

Created additional features to improve predictive performance.

#### Weekend Indicator Feature

A new feature called `is_weekend` was created:

- `1 → Weekend Flight`
- `0 → Weekday Flight`

This feature was introduced to capture travel behavior differences between weekdays and weekends.

---

### 4. Feature Encoding

Since Machine Learning models require numerical inputs, categorical variables were encoded using appropriate techniques.

#### Label Encoding
Used for high-cardinality categorical features:

- `route`
- `booking_origin`

#### One-Hot Encoding
Applied to low-cardinality categorical features:

- `sales_channel`
- `trip_type`

This ensured that all variables were transformed into machine-readable numerical formats.

---

### 5. Data Validation

Validated the dataset to ensure:

- No missing values
- Correct data types
- Machine-learning-ready structure

This step ensured clean and reliable input data for model training.

---

## Machine Learning Model

### Algorithm Used

**Random Forest Classifier**

Random Forest was selected because:

- It performs well on structured datasets
- Handles non-linear relationships effectively
- Works well with mixed feature types
- Provides feature importance for interpretability

Feature importance was especially useful in identifying the strongest booking predictors.

---

## Model Training

### Train-Test Split

The dataset was split into:

- **80% Training Data**
- **20% Testing Data**

Using:

- `random_state = 42`
- stratified sampling for consistent target distribution

This ensured reproducibility and proper handling of class imbalance.

---

## Model Evaluation

The model performance was evaluated using:

### 5-Fold Cross Validation

Cross-validation was performed to assess model stability and reliability across multiple data splits.

Evaluation metric used:

- **Accuracy Score**

---

### Classification Report

The following evaluation metrics were analyzed:

- Precision
- Recall
- F1-Score
- Accuracy

These metrics helped assess model performance on both majority and minority classes.

---

## Feature Importance Analysis

A feature importance visualization was generated to identify the variables with the highest influence on booking prediction.

The model identified important booking indicators such as:

- Purchase lead time
- Route
- Flight hour
- Customer preferences
- Travel duration

This helped translate technical findings into actionable business insights.

---

## Business Insights

The analysis revealed that:

- Customers booking earlier were more likely to complete bookings
- Certain routes had significantly higher booking completion rates
- Travel timing influenced booking behavior
- Ancillary preferences such as meals, baggage, and seats contributed to prediction performance

---

## Business Recommendations

Based on the findings, airlines can:

- Target high-conversion routes with personalized marketing campaigns
- Encourage earlier bookings through discounts and promotional offers
- Improve conversion rates using predictive customer segmentation
- Optimize customer engagement strategies using behavioral insights

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook / VS Code

---

## Skills Demonstrated

- Data Cleaning
- Feature Engineering
- Data Preprocessing
- Machine Learning
- Predictive Modeling
- Random Forest Classification
- Model Evaluation
- Cross Validation
- Feature Importance Analysis
- Business Analytics
- Data Visualization
