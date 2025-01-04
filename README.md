# Churn Prediction using Artificial Neural Network (ANN) - Accuracy : 85.95%

## Dataset
  This dataset contains information about customers of a bank. Each row represents an individual customer, with multiple columns providing details about their demographics, financial metrics, and engagement with the institution. Here’s a breakdown of the columns and their descriptions:
  	•	RowNumber: A sequential identifier for each row in the dataset.
  	•	CustomerId: A unique identifier assigned to each customer.
  	•	Surname: The last name of the customer.
  	•	CreditScore: A numerical value representing the customer’s creditworthiness.
  	•	Geography: The customer’s country of residence.
  	•	Gender: The gender of the customer (e.g., Male or Female).
  	•	Age: The age of the customer in years.
  	•	Tenure: The number of years the customer has been with the institution.
  	•	Balance: The amount of money in the customer’s account (e.g., bank balance).
  	•	NumOfProducts: The number of financial products the customer is using with the institution (e.g., credit cards, loans).
  	•	HasCrCard: A binary indicator (1 = Yes, 0 = No) showing whether the customer owns a credit card.
  	•	IsActiveMember: A binary indicator (1 = Active, 0 = Inactive) of the customer’s account activity status.
  	•	EstimatedSalary: The estimated annual salary of the customer.
  	•	Exited: A binary target variable (1 = Yes, 0 = No) indicating whether the customer has exited (churned) from the institution.
  
  Dataset Characteristics:
  
  	•	Demographics: Provides customer-specific details like age, gender, and geography.
  	•	Financial Data: Includes key financial indicators such as credit score, balance, and estimated salary.
  	•	Engagement: Captures customer interaction levels via metrics like tenure, number of products, and active membership status.
  	•	Target Variable: The “Exited” column identifies customers who have churned, making the dataset suitable for churn prediction models.

## Objective
	•	Predict customer churn based on their demographics, financial data, and engagement levels.
	•	Analyze factors contributing to customer loyalty and retention.
	•	Understand the demographic and financial profiles of customers who are likely to exit.

## Feature Engineering
  Encoding Categorical Variables:
  	•	Geography: The Geography column is transformed using one-hot encoding via pd.get_dummies(), with drop_first=True to avoid multicollinearity. This results in binary columns for each country (excluding one as the reference category).
  	•	Gender: Similarly, the Gender column is encoded into binary values, with one gender (e.g., Male or Female) dropped for reference.

## Feature Scaling
Feature scaling ensures all features contribute equally to the model by standardizing them to a uniform scale, improving performance and convergence. Here, we used StandardScaler from sklearn to transform the data to have a mean of 0 and standard deviation of 1

## Artificial Neural Network (ANN)

1. Input Layer : Activation function used is Relu, no of neurons = 10
2. Hidden Layer 1 : Activation function used is Relu, no of neurons = 7
3. Hidden Layer 2 : Activation function used is Relu, no of neurons = 6
4. Output Layer : Activation function used is Sigmoid, no of neurons = 1  #Since it is a binary classification Sigmoid id used
5. optimizer= adam
6. loss= binary_crossentropy
7. metrics= accuracy
8. Early Stopping is used to automatically stop the model training when the accuracy is stagnent

## Confusion Matrix 
array([[1568,   27],
       [ 254,  151]])

## Accuracy 
85.95%

## Accuracy of the model train vs test

<img width="610" alt="Screenshot 2025-01-04 at 00 21 39" src="https://github.com/user-attachments/assets/b9bdb349-8e36-460e-8b59-7dc9ac7c1e0d" />

## Loss of the model train vs test

![image](https://github.com/user-attachments/assets/477be4ec-ad24-446a-bb39-a80ca0bd16f2)



 
