# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. import pandas module and import the required data set.
2.Find the null values and count them.
3.Count number of left values.
4.From sklearn import LabelEncoder to convert string values to numerical values.
5.From sklearn.model_selection import train_test_split.
6.Assign the train dataset and test dataset.
7.From sklearn.tree import DecisionTreeClassifier.
8.Use criteria as entropy.
9.From sklearn import metrics.
10.Find the accuracy of our model and predict the require values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: SWETHA D
RegisterNumber:  212223040222
*/
import pandas as pd
data = pd.read_csv("Employee.csv")
data.head()
data.info()

data.isnull().sum()

data["left"].value_counts

from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]

x.head()
y=data["left"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)

from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)

y_pred = dt.predict(x_test)
from sklearn import metrics

accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy

dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:
![decision tree classifier model](sam.png)
![238635663-fe7e2a52-b584-4686-8027-b1cb8ec0c136](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/76887df3-3601-4164-98bb-ea7fad1fd097)

![238635901-e91f5083-b124-4bde-a531-a3a8f8f469cb](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/7c8d8922-cbca-4382-a870-ded65c1aa1fa)

![238636120-13765c70-5817-4e4a-875b-191ff0b3a687](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/0902240c-1ae7-4fdc-ad60-a3b183749397)

![238637334-01560d37-b412-446d-8648-705b39e7a7ea](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/7e0512a1-c5e2-4b39-aac3-d212fad2286b)

![238637043-459eba34-9924-4f09-a9fe-c3db2cb4b230](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/c8b6d554-f120-4d70-abc2-5bfa10c7ee06)

![238637477-9c7e8ea2-4992-464f-9c3e-8ade02113569](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/8f48cd27-fb8a-43fb-85ca-3292a392ed62)

![238637597-7dd3fc29-5591-415e-b43c-bb3d9bcb392c](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/0a57bcc5-3d95-4e0f-83bf-a58cc3c1f072)


![238637742-9a5343bc-3a31-4ab6-9e9d-96bad64d5909](https://github.com/swetha23013979/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/153823422/e9147f0f-a7e4-4aed-b4ba-6dc759385667)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
