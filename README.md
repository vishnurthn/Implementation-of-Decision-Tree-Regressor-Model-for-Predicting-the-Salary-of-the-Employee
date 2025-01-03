# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import pandas
2.Import Decision tree classifier
3.Fit the data in the model
4.Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Vishnu Rathan B
RegisterNumber:  24001855
*/
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
print(data.head())
x=data[["Position","Level"]]
print(x.head())
y=data["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print(y_pred)
from sklearn import metrics
r2=metrics.r2_score(y_test,y_pred)
print(r2)
dt.predict([[5,6]])
*/
```

## Output:
![Decision Tree Regressor Model for Predicting the Salary of the Employee](sam.png)

![expt 9 1](https://github.com/user-attachments/assets/967ea062-297e-482c-b770-e753cfc3dfeb)

![expt 9 2](https://github.com/user-attachments/assets/00f1c56c-dbf0-4e2a-b7b3-613d7257abb0)

![expt 9 3](https://github.com/user-attachments/assets/f8031190-77b2-48c4-ab5d-bf4f6ac61e51)

![Screenshot 2025-01-03 083106](https://github.com/user-attachments/assets/3dbdb64e-5e83-48bb-8afb-da7a8f27298a)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
