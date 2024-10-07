# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
```
Step 1:Start.
Step 2:Import the required libraries.
Step 3:Upload the csv file and read the dataset.
Step 4:Check for any null values using the isnull() function.
Step 5:From sklearn.tree inport DecisionTreeRegressor.
Step 6:Import metrics and calculate the Mean squared error.
Step 7:Apply metrics to the dataset, and predict the output.
Step 8:End.
```
## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Iswarya P
RegisterNumber: 212223230082 
```

```
import pandas as pd
data=pd.read_csv("C:/Users/Manju Mageswari/Downloads/Salary.csv")
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
x_train, x_test, y_train, y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
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
### MSE:
![image](https://github.com/user-attachments/assets/dd7abf19-8855-4199-a1f3-7b0eac39efbc)


### r2 value:
![image](https://github.com/user-attachments/assets/f0460230-4f3e-435e-830b-a240e6c334ec)


### Predicted value:
![image](https://github.com/user-attachments/assets/1c67a416-564f-4067-a6c6-7b24442aedbd)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
