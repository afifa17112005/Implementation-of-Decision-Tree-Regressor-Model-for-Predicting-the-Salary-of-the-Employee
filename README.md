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
Developed by: Lathika Sree R
RegisterNumber: 212224040169 
*/
```

```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
```
```
R2 score:  0.48611111111111116
```
```
dt.predict([[5,6]])
```

## Output:

<img width="1763" height="428" alt="image" src="https://github.com/user-attachments/assets/69e3c13d-6845-4d4a-a072-b672bd57a310" />

<img width="331" height="249" alt="image" src="https://github.com/user-attachments/assets/512e518b-3c8b-46d9-8a49-9154136bee38" />

<img width="1751" height="293" alt="image" src="https://github.com/user-attachments/assets/dd303306-d885-4c4e-b2f1-3c7f7a1a7584" />

<img width="1066" height="66" alt="image" src="https://github.com/user-attachments/assets/d65a41e8-dcb1-4133-b7c2-816e879b8eaa" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
