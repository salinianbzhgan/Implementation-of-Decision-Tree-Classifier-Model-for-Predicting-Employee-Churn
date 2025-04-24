### Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

### AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

### Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Jupyter notebook
### Algorithm
1.Import Libraries and Load Dataset. 2. Preprocess the Data. 3. Split the Dataset. 4. Train the Decision Tree Classifier. 5. Make Predictions and Evaluate the Model

### Program:
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: SALINI A 
RegisterNumber: 212223220091
```
import pandas as pd
data=pd.read_csv("Employee.csv")
data
```
```
data["left"].value_counts()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
```
```
data.head()
```
```
data["salary"]=le.fit_transform(data["salary"])
data
```
```
x=data[["satisfaction_level","last_evaluation","number_project","time_spend_company"]]
x.head()
```
```
y=data["left"]
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
```
```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
```
```
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
```
dt.predict([[0.5,0.8,2,9]])
```
### Output:
![image](https://github.com/user-attachments/assets/873e7700-0f50-47dc-b18d-6661ae56aa94)
![image](https://github.com/user-attachments/assets/b5b2154a-7647-4737-8f63-1d0fe6844e51)
![image](https://github.com/user-attachments/assets/857e7968-7050-4c40-a17e-50ca447c2d5e)
![image](https://github.com/user-attachments/assets/41f14f45-9d3d-4974-80ce-974baff1bf01)
![image](https://github.com/user-attachments/assets/63a8eb1d-f7d6-4e72-906e-3b1af5b3eb59)
![image](https://github.com/user-attachments/assets/364d4c00-b2c7-4846-9d41-fbdd411468e9)
![image](https://github.com/user-attachments/assets/ef76e780-6f97-426f-a864-e2028faac439)

### Result:
Thus the program to implement the Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
