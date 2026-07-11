# Customer Churn Prediction

A machine learning project that predicts whether a bank customer is likely to leave the bank (churn) based on customer demographics, account details, and banking behavior.

The project compares multiple machine learning algorithms and evaluates their performance using various classification metrics to identify the best-performing model.

---

## Project Overview

Customer churn is one of the biggest challenges for subscription-based and banking businesses. Predicting churn allows organizations to identify customers who are likely to leave and take proactive measures to retain them.

This project uses supervised machine learning algorithms to classify customers into two categories:

- **0** → Customer stays with the bank
- **1** → Customer leaves the bank (Churn)

---

## Dataset

The dataset contains customer information such as:

- Credit Score
- Geography
- Gender
- Age
- Tenure
- Balance
- Number of Products
- Has Credit Card
- Is Active Member
- Estimated Salary
- Exited (Target Variable)

Columns such as **RowNumber**, **CustomerId**, and **Surname** were removed since they do not contribute to predicting customer churn.

---

## Project Workflow

1. Import required libraries
2. Load the dataset
3. Perform exploratory data analysis (EDA)
4. Handle missing values and duplicates
5. Remove unnecessary features
6. Encode categorical variables
7. Split the dataset into training and testing sets
8. Scale numerical features (for Logistic Regression)
9. Train multiple machine learning models
10. Evaluate model performance
11. Compare models using ROC curves and evaluation metrics
12. Analyze feature importance
13. Draw conclusions

---

## Machine Learning Models

The following classification algorithms were implemented:

- Logistic Regression
- Random Forest Classifier
- Gradient Boosting Classifier

---

## Model Evaluation

Each model was evaluated using:

- Accuracy Score
- Confusion Matrix
- Classification Report
- ROC-AUC Score
- ROC Curve

A comparison table was also created to determine the best-performing model.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Project Structure

```
Customer-Churn-Prediction/
│
├── Customer_Churn_Prediction.ipynb
├── Churn_Modelling.csv
├── README.md
├── requirements.txt
└── images/
    ├── churn_distribution.png
    ├── correlation_heatmap.png
    ├── feature_importance.png
    └── roc_curve.png
```

---

## Installation

Clone the repository

```bash
git clone https://github.com/yourusername/Customer-Churn-Prediction.git
```

Move into the project directory

```bash
cd Customer-Churn-Prediction
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Project

Launch Jupyter Notebook

```bash
jupyter notebook
```

Open

```
Customer_Churn_Prediction.ipynb
```

Run all cells sequentially.

---

## Results

The trained models were compared using multiple evaluation metrics.

The project includes:

- Exploratory Data Analysis
- ROC Curve Comparison
- Classification Reports
- Confusion Matrices
- Feature Importance Visualization

The comparison helps identify the model that performs best for predicting customer churn.

---


## Author

**Amol Kainthola**

---

## License

This project is intended for educational and learning purposes.
