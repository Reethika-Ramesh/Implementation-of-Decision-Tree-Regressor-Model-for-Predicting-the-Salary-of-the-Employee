# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the standard libraries.
2.Upload the dataset and check for any null values using .isnull() function.
3.Import LabelEncoder and encode the dataset.
4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.
5.Predict the values of arrays.
6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.
7.Predict the values of array.
8.Apply to new unknown values.

## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: REETHIKA.R
RegisterNumber:  212219220042

import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
y=data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])

```

## Output:

## Data Head:
![image](https://user-images.githubusercontent.com/98681990/174663114-734df308-87c8-44a5-aa43-ed936f9442f6.png)

## Data Info:
![image](https://user-images.githubusercontent.com/98681990/174663132-4543786f-b006-4354-8b04-b657045888b8.png)


## Data Isnull:
![image](https://user-images.githubusercontent.com/98681990/174663153-2569625a-10a4-4c0b-949a-4395bc72eba1.png)

## Data Head:
![image](https://user-images.githubusercontent.com/98681990/174663168-001b2432-b396-4e90-b9e3-aa0c72ee0205.png)

## MSE:
![image](https://user-images.githubusercontent.com/98681990/174663182-422dda07-fa7f-4068-8ec0-ef387d8bc74b.png)

## R2:
![image](https://user-images.githubusercontent.com/98681990/174663203-f9805a16-e9b8-414d-9ab1-05037bd1bf39.png)

## Predicted Value:
![image](https://user-images.githubusercontent.com/98681990/174663215-ec22b02c-f3f1-46e4-a20b-4cb3e6d10422.png)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
