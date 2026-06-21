# Customer Churn Prediction

This project predicts customer churn for a telecom company using machine learning.

## Project Goal

The goal is to identify customers who are likely to leave the company, so the business can take action before losing them.

## Dataset

The dataset contains customer information such as:

- Tenure
- Monthly charges
- Total charges
- Contract type
- Internet service
- Payment method
- Churn status

## Main Steps

1. Loaded and inspected the dataset
2. Cleaned the `TotalCharges` column
3. Performed exploratory data analysis
4. Encoded categorical variables using one-hot encoding
5. Split the data into training and test sets
6. Trained Logistic Regression and Random Forest models
7. Evaluated models using accuracy, precision, recall, and F1-score
8. Experimented with decision thresholds

## Key Findings

- Customers with short tenure have much higher churn rates.
- Month-to-month contract customers churn much more than one-year or two-year contract customers.
- Fiber optic customers have higher churn rates than DSL or no-internet customers.
- Lowering the classification threshold improved churn recall from 57% to 76%.

## Model Results

### Logistic Regression with Scaling, Threshold 0.5

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Stay | 0.85 | 0.89 | 0.87 |
| Churn | 0.65 | 0.57 | 0.61 |

Accuracy: 0.80

### Logistic Regression with Scaling, Threshold 0.3

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| Stay | 0.89 | 0.74 | 0.81 |
| Churn | 0.51 | 0.76 | 0.61 |

Accuracy: 0.74

## Conclusion

The default Logistic Regression model achieved good overall accuracy, but lowering the decision threshold improved the ability to detect churners. This shows that model evaluation should depend on the business goal, not accuracy alone.

## Tools Used

- Python
- pandas
- matplotlib
- scikit-learn
- Git and GitHub
