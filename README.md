# Customer Churn Prediction using Machine Learning

## Project Overview

This project focuses on predicting customer churn using Machine Learning techniques. Customer churn refers to whether a customer leaves a company or continues using its services. By analyzing customer demographics, financial information, and account activity, the model predicts the likelihood of customer exit.

The project includes:

* Data exploration and preprocessing
* Exploratory Data Analysis (EDA)
* Feature engineering
* Logistic Regression and Random Forest models
* Hyperparameter tuning
* Cross-validation and model evaluation
* Feature scaling comparison

---

## Objective

The primary objective of this project is to build a classification model capable of predicting customer churn accurately so businesses can identify at-risk customers and improve retention strategies.

---

## Dataset Information

The dataset contains customer banking information and churn labels.

### Features:

* **CreditScore** — Customer credit score
* **Geography** — Customer country/location
* **Gender** — Male/Female
* **Age** — Customer age
* **Tenure** — Number of years with the bank
* **Balance** — Account balance
* **NumOfProducts** — Number of bank products used
* **HasCrCard** — Credit card ownership
* **IsActiveMember** — Active membership status
* **EstimatedSalary** — Estimated salary
* **Exited** — Target variable (0 = Stayed, 1 = Churned)

---

## Technologies & Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## Workflow

### 1. Data Loading & Exploration

* Loaded dataset using Pandas
* Checked dataset shape, data types, and summary statistics
* Verified missing values

### 2. Exploratory Data Analysis (EDA)

Performed visual analysis including:

* Churn distribution visualization
* Correlation heatmap
* Credit Score vs Churn
* Balance vs Churn
* Age vs Churn
* Age vs Balance scatter plot by churn category

These visualizations helped identify customer behavior patterns associated with churn.

---

## Data Preprocessing

The preprocessing pipeline included:

* Label encoding for Gender
* One-hot encoding for Geography
* Removal of irrelevant columns:

  * RowNumber
  * CustomerId
  * Surname
* Feature scaling using `StandardScaler`

---

## Machine Learning Models Used

### 1. Logistic Regression

* Baseline classification model
* Initially trained without feature scaling

### Important Note

The Logistic Regression model generated a convergence warning before feature scaling:

* This warning is **not an error**
* It occurs because the optimizer reached the iteration limit
* Feature scaling was later applied using `StandardScaler`, which improved convergence and model performance

### 2. Random Forest Classifier

* Ensemble learning model
* Achieved higher accuracy compared to Logistic Regression

---

## Model Evaluation Metrics

The models were evaluated using:

* Accuracy Score
* Confusion Matrix
* Precision
* Recall
* F1-Score
* Cross-validation Accuracy

---

## Results

### Logistic Regression (Without Scaling)

* Accuracy: ~80%

### Logistic Regression (With Scaling)

* Accuracy: ~81%
* Improved convergence and prediction performance

### Random Forest Classifier

* Accuracy: ~86.6%
* Best performing model in this project

### Hyperparameter Tuning

`GridSearchCV` was used to optimize the Random Forest model parameters:

* Best Accuracy: ~86.5%

---

## Visualizations Included

* Churn distribution count plot
* Correlation heatmap
* Boxplots for CreditScore, Balance, and Age
* Scatter plot for Age vs Balance
* Confusion matrix heatmap

---

## Project Structure

```bash id="8jq3md"
├── customer_Leave_or_Stay.csv
├── Customer_Churn_Prediction.ipynb
├── README.md
```

---

## How to Run the Project

### 1. Clone the Repository

```bash id="ks82jd"
git clone <repository-link>
```

### 2. Install Required Libraries

```bash id="1h3x9w"
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 3. Run the Jupyter Notebook

```bash id="2nd8xm"
jupyter notebook
```

---

## Future Improvements

* Use advanced models such as:

  * XGBoost
  * LightGBM
  * CatBoost
* Handle class imbalance using SMOTE
* Perform feature selection
* Deploy the model using Flask or Streamlit
* Build a customer churn dashboard

---

## Conclusion

This project demonstrates how Machine Learning can be applied to customer retention analysis. Multiple models and preprocessing techniques were explored, with Random Forest achieving the best performance. Feature scaling also improved Logistic Regression performance and resolved convergence warnings.

---
