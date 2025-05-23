# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

Import the standard libraries.

Upload the dataset and check for any null values using .isnull() function.

Import LabelEncoder and encode the dataset.

Import DecisionTreeRegressor from sklearn and apply the model on the dataset.

Predict the values of arrays.

Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

Predict the values of array.

Apply to new unknown values.


## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: SWETHA A
RegisterNumber:  212223220114
*/
```
```
import pandas as pd


data = pd.read_csv("Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"] = le.fit_transform(data["Position"])
data.head()

x = data[["Position", "Level"]]
y = data["Salary"]

from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)

from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train, y_train)
y_pred = df.predict(x_test)

from sklearn import metrics
mse = metrics.mean_squared_error(y_test, y_pred)
mse

r2 = metrics.r2_score(y_test, y_pred)
r2

dt.predict([[5,6]])
```
## Output:

![Screenshot 2025-05-23 084354](https://github.com/user-attachments/assets/3e840371-effb-42ef-99cc-beec9e23e384)

![Screenshot 2025-05-23 084354](https://github.com/user-attachments/assets/90a40f32-4347-4a11-91a3-9389b9161ef0)

![Screenshot 2025-05-23 084354](https://github.com/user-attachments/assets/195942cd-0bef-4a7b-9b97-d38c1d8dc2e8)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
