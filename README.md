# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries
2. Read the data frame using pandas
3. Get the information regarding the null values present in the dataframe.
4. Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5. Determine training and test data set.
6. Apply decision tree Classifier on to the dataframe.
7. Get the values of accuracy and data prediction.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: KAVYA K
RegisterNumber: 212222230065 
import pandas as pd
data=pd.read_csv("Employee.csv")

data.head()

data.info()

data.isnull().sum()

data["left"].value_counts()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()

x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()

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
*/
```

## Output:
Output:
Initial data set:

![238370361-a91fde4f-a912-4b54-941d-b2ba2e9d7178](https://github.com/kavyasenthamarai/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118668727/3ff58612-8579-4954-9fb8-0f2959de278a)

Data info:

![238371021-3e876e7e-eadc-4125-b21b-6734a505096c](https://github.com/kavyasenthamarai/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118668727/915c50b6-c185-4d68-9d8d-f87101db2d18)

Optimization of null values:

![image](https://github.com/kavyasenthamarai/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118668727/818671a5-e9af-4b24-a709-e60478c9822b)

Assignment of x and y values:

![image](https://github.com/kavyasenthamarai/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118668727/478ac405-262a-4087-a0d0-aaac3a792f09)

Converting string literals to numerical values using label encoder:

![image](https://github.com/kavyasenthamarai/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118668727/6b31c971-6b11-45e7-88dc-318429b92637)

Accuracy:

![image](https://github.com/kavyasenthamarai/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118668727/f6c05b8a-b823-4570-b917-d46624e98f03)

Prediction:

![image](https://github.com/kavyasenthamarai/Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn/assets/118668727/9c953f5e-7d74-4913-b968-b0aed5acda5e)

## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
