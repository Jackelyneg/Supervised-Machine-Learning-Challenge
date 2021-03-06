# Supervised-Machine-Learning-Challenge

## Predicting Credit Risk
## Task
- To build a machine learning model, using Logistic Regression and Random Forest Classifier that attempts to predict whether a loan from LendingClub will become high risk or not.

## Background
LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.


### Instructions
- Retrieve the data
- CSV: 2019loans.csv
       2020Q1loans.csv
- The CSV's will be used for an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

Note: these two CSVs have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.

### Preprocessing: Convert categorical data to numeric
- Create a training set from the 2019 loans using pd.get_dummies() to convert the categorical data to numeric columns. 
- Similarly, create a testing set from the 2020 loans, also using pd.get_dummies(). 
- There are categories in the 2019 loans that do not exist in the testing set.


- Two models are compared on this data: a logistic regression, and a random forests classifier.
- Fit a LogisticRegression model and RandomForestClassifier model
- Create a LogisticRegression model, fit it to the data, and print the model's score. Do the same for a RandomForestClassifier. 

### Revisit the Preprocessing: Scale the data
- The data going into these models was never scaled, an important step in preprocessing. Use StandardScaler to scale the training and testing sets. Before re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data, make another prediction about how you think scaling will affect the accuracy of the models. Write your predictions down and provide justification.

- Fit and score the LogisticRegression and RandomForestClassifier models on the scaled data.

### Results:
- Logistic Regression is a better model fit for the data and is also sensitive when the data is scaled and when important features are selected. For Random Forest there is no visible change once the data is scaled and improtant features are selected.
