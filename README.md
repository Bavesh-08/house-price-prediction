# 🏠 House Price Prediction Model

A machine learning model that predicts house prices based on property characteristics using Linear Regression.

---

## 📊 Project Overview

This project implements a **Linear Regression model** to predict residential property prices. The model analyzes various housing features such as area, bedrooms, bathrooms, condition, location, and more to provide accurate price estimates.

### Key Metrics
- **Training R² Score**: 0.0068
- **Test R² Score**: -0.0156
- **Training MAE**: $237,632
- **Test MAE**: $243,259
- **Dataset Size**: 2,000 properties

---

## 🎯 Features

The model uses the following property attributes for prediction:

| Feature | Description | Type |
|---------|-------------|------|
| **Area** | Square footage of the property | Numerical |
| **Bedrooms** | Number of bedrooms | Numerical |
| **Bathrooms** | Number of bathrooms | Numerical |
| **Floors** | Number of floors | Numerical |
| **YearBuilt** | Year the property was constructed | Numerical |
| **Location** | Geographic location (Downtown, Suburban, Rural, Urban) | Categorical |
| **Condition** | Property condition (Excellent, Good, Fair, Poor) | Categorical |
| **Garage** | Presence of garage (Yes/No) | Binary |

---

## 📈 Dataset Information

- **Total Records**: 2,000 properties
- **Features**: 9 (excluding target)
- **Target Variable**: Price
- **Missing Values**: None
- **Train-Test Split**: 80-20 ratio

### Data Statistics
- **Price Range**: $5,005 - $999,656
- **Mean Price**: $537,676.86
- **Standard Deviation**: $276,428.85

---

## 🛠️ Technology Stack

```
Language: Python 3.x
Libraries:
  - NumPy         (Numerical computing)
  - Pandas        (Data manipulation)
  - Scikit-learn  (Machine learning)
  - Matplotlib    (Visualization)
  - Seaborn       (Statistical visualization)
```

---

## 📝 Model Pipeline

### 1. **Data Loading**
   - Load housing dataset (CSV format)
   - Inspect dataset structure and integrity

### 2. **Data Preprocessing**
   - Encode categorical variables (Location, Condition, Garage)
   - Standardize features using StandardScaler
   - Remove target variable from features

### 3. **Data Splitting**
   - Split data: 80% training, 20% testing
   - Random state: 2 (for reproducibility)

### 4. **Model Training**
   - Algorithm: Linear Regression
   - Fit model on standardized training data

### 5. **Evaluation**
   - R² Score (coefficient of determination)
   - Mean Absolute Error (MAE)
   - Visualization: Actual vs. Predicted scatter plots

---

## 📊 Model Performance

### Training Results
```
R² Score:          0.0068
Mean Absolute Error: $237,632
```

### Testing Results
```
R² Score:          -0.0156
Mean Absolute Error: $243,259
```

### 📌 Performance Analysis

The model shows **poor predictive performance** with near-zero R² scores. This indicates that:
- Linear relationships don't capture price variations effectively
- Feature engineering or additional features may be needed
- More complex models (Random Forest, XGBoost, Neural Networks) might perform better

---

## 🔍 Visualizations

The model generates comparison plots showing:
- **Training Data**: Actual vs. Predicted prices scatter plot
- **Test Data**: Actual vs. Predicted prices scatter plot

These visualizations help identify prediction patterns and model limitations.

---

## 💡 Recommendations for Improvement

1. **Feature Engineering**
   - Create interaction terms (Area × YearBuilt)
   - Add polynomial features for non-linear relationships
   - Normalize or scale categorical variables differently

2. **Model Enhancement**
   - Try advanced algorithms: Random Forest, Gradient Boosting, Neural Networks
   - Implement hyperparameter tuning
   - Use ensemble methods for better accuracy

3. **Data Exploration**
   - Perform EDA to identify outliers
   - Analyze feature correlations
   - Check for multicollinearity

4. **Regularization**
   - Implement Ridge or Lasso regression
   - Apply cross-validation techniques
   - Experiment with different test-train splits

---

## 📂 Project Structure

```
├── dataset/
│   └── House Price Prediction Dataset.csv
├── model.py                 # Main model code
├── requirements.txt         # Dependencies
└── README.md               # Documentation
```

---

## 🔧 Usage

```python
# Load the model script
python model.py

# Predictions
predictions = model.predict(X_new)

# Evaluation
r2_score = metrics.r2_score(y_actual, predictions)
mae = metrics.mean_absolute_error(y_actual, predictions)
```

---

## 📋 Code Snippet

```python
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import StandardScaler

# Initialize and train
model = LinearRegression()
model.fit(x_train, y_train)

# Predict
predictions = model.predict(x_test)

# Evaluate
from sklearn import metrics
r2 = metrics.r2_score(y_test, predictions)
```

---

## 🎓 Learning Outcomes

This project demonstrates:
- ✅ Data preprocessing and standardization
- ✅ Train-test split methodology
- ✅ Linear regression implementation
- ✅ Model evaluation metrics (R², MAE)
- ✅ Data visualization techniques
- ✅ Categorical variable encoding

---


**Last Updated**: March 2026  
**Status**: ⚠️ Model needs optimization for production use
