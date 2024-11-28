# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the libraries and read the data frame using pandas.
2.Calculate the null values present in the dataset and apply label encoder.
3.Determine test and training data set and apply decison tree regression in dataset.
4.calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: 
RegisterNumber:
import pandas as pd
from sklearn.preprocessing import LabelEncoder
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeRegressor
from sklearn import metrics


data = pd.read_csv(r"C:\Users\Suriya\Downloads\Salary.csv")


print(data.head())
print(data.info())
print(data.isnull().sum())


le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])


x = data[["Position", "Level"]]
y = data["Salary"]              


x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)


dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)


y_pred = dt.predict(x_test)


r2 = metrics.r2_score(y_test, y_pred)
print(f"R-squared: {r2}")


print("Predicted salaries:", y_pred)
*/
```

## Output:
![Screenshot 2024-11-28 210504](https://github.com/user-attachments/assets/bb10c4bc-062b-469a-8463-3680df9fd8da)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
