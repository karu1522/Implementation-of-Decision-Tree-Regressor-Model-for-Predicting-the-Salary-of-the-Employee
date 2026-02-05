# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas.
2. Import Decision tree classifier.
3. Fit the data in the model.
4. Find the accuracy score.

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Karthic U
RegisterNumber: 212224040151
```

## Dataframe:
```py
import pandas as pd
data=pd.read_csv("Salary.csv")
print(data.head())
print(data.info())
print(data.isnull().sum())
```

## Output:
<img width="439" height="464" alt="image" src="https://github.com/user-attachments/assets/f4ca10e6-dade-4c9c-a415-0cadcc61327c" />



## Head values:
```py
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```

## Output:
<img width="318" height="255" alt="image" src="https://github.com/user-attachments/assets/7015248c-1dca-4ead-b9d1-89db6288ba00" />


## Salary:
```py
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
```

## Output:
<img width="179" height="284" alt="image" src="https://github.com/user-attachments/assets/25c727b1-bfd9-4acf-9994-014d14a54ebd" />



## R2 values:
```py
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
r2
```

## Output:
<img width="251" height="38" alt="image" src="https://github.com/user-attachments/assets/867957a3-e730-4b33-be79-57cddcb4bcd2" />


## Prediction:
```py
dt.predict([[5,6]])
```

## Output:
<img width="179" height="26" alt="image" src="https://github.com/user-attachments/assets/570479d3-2ad7-4e2d-9e49-0b50f9e66f9e" />


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
