# customer-churn-prediction
## Business problem: why should a firm worry about churn?

What is "churn"? When a customer opts out/abandons the services.

Why does churn constitute an issue? Because gaining a new client is expensive: advertisement, welcome bonus etc.

Meanwhile, retaining a client can be less costly: minimal discount or a free update. Simple as that.

That's exaclty why firms prefer keeping an already existing client rather than getting a new one.

## THE PROJECT OBJECTIVE: 

We want to estimate the probability for each client to end the contract. Therefore, we don't want the output to be dummy, but a probability estimate in range [0,100] percent, and then determine wheter it would be ideal to take preventive actions or not with respect to a benchmark.

## WHY IS IT NEEDED?

Because the Marketing division of the firm can tackle down these clients and take further actions: a phone call, an email, etc.

## HOW DO WE MEASURE SUCCESS? 

Not only in relation to the confidence level of the model, but also by weighting the gravity of the error: a false negative costs more than a false positive.

## THE DATASET

Dataset used: Telco Customer Churn, Kaggle

Dataset contains contains 7043 rows (customers) and 21 columns (features). Target variable is 1 ("Churn") and it is binary: 1 if client abandoned, 0 otherwise.

## HOW THE REPO IS STRUCTURED

Customer-Churn/
│
├── data/
│
├── notebooks/
│
├── src/
│
└── README.md