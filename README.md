# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2. Import Decision tree classifier
3. Fit the data in the model
4. Find the accuracy score

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Yamunaasri T S
RegisterNumber:  212222240117

import pandas as pd
data=pd.read_csv("/content/Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()    #no departments and no left
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
#### data.head()
![Screenshot 2023-06-03 125050](https://github.com/Yamunaasri/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/115707860/2f5b859a-4027-48a7-b014-b19a9b8b5d58)

#### data.info()
![Screenshot 2023-06-03 125121](https://github.com/Yamunaasri/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/115707860/828d738a-2c5d-40fc-bb34-6f1fd1f15d2a)

#### isnull() and sum()
![Screenshot 2023-06-03 125143](https://github.com/Yamunaasri/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/115707860/55e89a77-5d19-464a-b1f3-017c247ef570)

#### data.head() for salary 
![Screenshot 2023-06-03 125624](https://github.com/Yamunaasri/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/115707860/cbc58a1d-4fea-4f0a-a6dc-dfa47e055ac7)

#### MSE value
![Screenshot 2023-06-03 125705](https://github.com/Yamunaasri/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/115707860/588d3b32-9ce3-4e6b-80fc-b1bc369ead8d)


#### r2 value
![Screenshot 2023-06-03 125753](https://github.com/Yamunaasri/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/115707860/c12b1343-5f08-40f5-8a7f-cac51a07462d)

#### data prediction
![Screenshot 2023-06-03 130011](https://github.com/Yamunaasri/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/115707860/95377109-ecb3-4041-abc9-55fb270029a0)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
