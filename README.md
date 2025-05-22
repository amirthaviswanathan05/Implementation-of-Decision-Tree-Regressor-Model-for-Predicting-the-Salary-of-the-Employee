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

4.Calculate Mean square error,data prediction and r2.

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: AMIRTHAVARSHINI V
RegisterNumber: 212223040014
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.info()

data.head()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data['Position'] = le.fit_transform(data['Position'])

x = data[['Position', 'Level']]
y = data['Salary']

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()

dt.fit(x_train, y_train)
y_pred = dt.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
print(mse)


dt.predict([[5,6]])
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)
![Screenshot 2025-05-22 215300](https://github.com/user-attachments/assets/dcc0c5b0-2df1-41c2-bd53-db0df2586fbd)
![Screenshot 2025-05-22 215319](https://github.com/user-attachments/assets/bc4375da-058b-4e13-a2fb-23b964de69db)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
