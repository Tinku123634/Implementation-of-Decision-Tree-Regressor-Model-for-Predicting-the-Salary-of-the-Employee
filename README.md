# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the required libraries for data processing and machine learning.

2.Load the dataset and convert categorical values into numerical format using label encoding.

3.Separate the features (X) and target variable (y) from the dataset.

4.Split the dataset into training and testing sets and train the Decision Tree Classifier using the training data.

5.Predict and evaluate the model using the test data and calculate accuracy and other performance metrics.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S.Tinku
RegisterNumber:25006607

import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder
from sklearn.tree import DecisionTreeClassifier
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

data = pd.read_csv("Employee.csv")

le = LabelEncoder()
for column in data.columns:
    if data[column].dtype == 'object':
        data[column] = le.fit_transform(data[column])

X = data.drop('left', axis=1)
y = data['left']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

model = DecisionTreeClassifier()
model.fit(X_train, y_train)

y_pred = model.predict(X_test)

print("Accuracy:", accuracy_score(y_test, y_pred))
print(confusion_matrix(y_test, y_pred))
print(classification_report(y_test, y_pred))
*/
```

## Output:

<img width="597" height="293" alt="Screenshot 2026-03-09 102554" src="https://github.com/user-attachments/assets/2dba0273-a6c5-45a7-8b24-91a705e3cedb" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
