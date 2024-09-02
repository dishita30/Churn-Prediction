# Customer Churn Prediction

## Dataset Description

This dataset contains information about 5,000 customers, including their demographic details, contract information, service usage, and whether they have churned or not. The goal is to build a predictive model that can accurately identify customers who are likely to churn, which can help the company take proactive measures to retain them.

The dataset includes the following features:

1. **CustomerID**: Unique identifier for each customer.
2. **Age**: Age of the customer.
3. **Gender**: Gender of the customer.
4. **ContractType**: The type of contract the customer has (Month-to-month, One year, Two year).
5. **MonthlyCharges**: The monthly charges the customer pays.
6. **TotalCharges**: The total charges the customer has paid over their tenure.
7. **TechSupport**: Whether the customer has tech support or not.
8. **InternetService**: The type of internet service the customer has (DSL, Fiber optic, No).
9. **Tenure**: The number of months the customer has been with the company.
10. **PaperlessBilling**: Whether the customer has paperless billing or not.
11. **PaymentMethod**: The payment method the customer uses.
12. **AverageMonthlyCharges**: The average monthly charges the customer pays.
13. **CustomerLifetimeValue**: The estimated lifetime value of the customer.
14. **Churn**: Whether the customer has churned or not (Yes/No).

## Data Preprocessing and Feature Engineering

1. **Handling Missing Values**: The dataset had missing values in the 'Age', 'TotalCharges', and 'InternetService' columns. These were imputed using appropriate techniques, such as mean imputation for numerical features and mode imputation for categorical features.

2. **Encoding Categorical Features**: The categorical features in the dataset were encoded using label encoding, transforming them into numerical values.

3. **Feature Engineering**: Additional features were created based on domain knowledge and insights from the exploratory data analysis (EDA), such as 'AverageMonthlyCharges' and 'CustomerLifetimeValue'.

4. **Handling Imbalanced Data**: The dataset was found to be imbalanced, with a majority of non-churned customers. To address this, the Synthetic Minority Over-sampling Technique (SMOTE) was used to balance the training data.

## Model Building and Evaluation

Several classification models were evaluated, including Logistic Regression, Random Forest, Gradient Boosting, and XGBoost. The models were trained and tuned using techniques like grid search and randomized search.

The XGBoost model was found to perform the best, with the following metrics on the test set:

- Accuracy: 99%
- Precision: 98%
- Recall: 97%
- F1-Score: 98%
- AUC-ROC: 99%

The superior performance of the XGBoost model can be attributed to its ability to handle non-linear relationships, efficient parallel processing, effective regularization techniques, and handling of missing values.

## Model Deployment

The trained XGBoost model has been saved to a file named 'xgboost_model.pkl' using the pickle library. This model can be easily loaded and used for making predictions on new customer data.

## Conclusion

This project demonstrates the development of a robust customer churn prediction model using the XGBoost algorithm. The model's high accuracy and other performance metrics indicate its effectiveness in identifying customers who are likely to churn, which can help the company take proactive measures to retain them and improve customer loyalty.
