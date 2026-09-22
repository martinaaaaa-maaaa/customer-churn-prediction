# Customer Churn Prediction

## Business Problem

Customer churn occurs when a customer stops using a company's services or terminates their contract.

For a telecommunications company, customer churn represents an important business problem. Acquiring new customers typically involves costs such as advertising, promotional offers, and welcome bonuses, while retaining existing customers may require less expensive interventions, such as targeted discounts or personalized offers.

Being able to identify customers who are at risk of leaving can therefore help the company focus its retention efforts more effectively.

## Project Objective

The objective of this project is to develop a machine learning model that estimates the probability that a customer will churn.

Rather than producing only a binary prediction, the model will generate a churn probability for each customer. This probability can then be compared with a decision threshold to identify customers who may benefit from targeted retention actions.

Potential interventions could include personalized offers, discounts, emails, or direct contact from the company.

## Measuring Success

Model performance should not be evaluated using accuracy alone.

In a churn prediction setting, different prediction errors can have different business costs:

- **False Negative:** the model predicts that a customer will stay, but the customer actually leaves.
- **False Positive:** the model predicts that a customer will leave, but the customer would have stayed anyway.

A false negative may result in a lost customer and missed retention opportunity, while a false positive may result in the cost of an unnecessary retention action.

For this reason, metrics such as **recall, precision, F1-score, and the confusion matrix** will be considered alongside accuracy. The final decision threshold should also reflect the business trade-off between missed churners and unnecessary retention interventions.

## Dataset

The project uses the **Telco Customer Churn** dataset.

The dataset contains:

- **7,043 customers**
- **21 variables**
- Customer demographics
- Account information
- Services subscribed to
- Contract information
- Monthly and total charges
- Churn status

The target variable is `Churn`, which indicates whether a customer left the company (`Yes`) or remained (`No`).

During the initial data exploration, 11 non-numeric values were identified in `TotalCharges`. These observations corresponded to customers with `tenure = 0` and were handled during data cleaning.

## Exploratory Data Analysis

Initial exploratory analysis showed that:

- Approximately **26.5%** of customers churned, compared with **73.5%** who remained.
- Churn rates differ across contract types.
- Customer tenure shows different distributions between churned and retained customers.
- Monthly charges also show differences between the two groups.

These observations are exploratory and indicate associations rather than causal relationships.

The complete exploratory analysis is available in:

`notebooks/01_eda.ipynb`

## Repository Structure

```text
customer-churn-prediction/
│
├── data/
│   ├── raw/            # Original dataset
│   └── processed/      # Processed data
│
├── notebooks/
│   └── 01_eda.ipynb    # Exploratory Data Analysis
│
├── src/                # Source code for preprocessing and modeling
│
├── .gitignore
└── README.md