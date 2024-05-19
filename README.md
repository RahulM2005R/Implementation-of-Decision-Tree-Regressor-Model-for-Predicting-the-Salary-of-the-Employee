# EX-6:Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee
### DATE:
## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
1.Import the required libraries. 
2.Read the data frame using pandas.
3.Get the information regarding the null values present in the dataframe.
4.Apply label encoder to the non-numerical column inoreder to convert into numerical values.
5.Determine training and test data set.
6.Apply decision tree regression on to the dataframe.
7.Get the values of Mean square error, r2 and data prediction.
## Program:
```
data=pd.read_csv("Salary Data.csv")
data.head()
data.tail()
data.info()
data["Gender"]=data["Gender"].astype('category')
data["Education Level"]=data["Education Level"].astype('category')
data["Job Title"]=data["Job Title"].astype('category')
data.info()
data["Gender"]=data["Gender"].cat.codes
data["Education Level"]=data["Education Level"].cat.codes
data["Job Title"]=data["Job Title"].cat.codes
data.info()
data.head()
x=data[['Age','Gender','Education Level','Job Title','Years of Experience']]
x
x.shape
y=data[['Salary']]
y.shape
from sklearn.model_selection import train_test_split
x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=2)
from sklearn.tree import DecisionTreeRegressor
dtr=DecisionTreeRegressor()
dtr.fit(x_train,y_train)
y_pred=dtr.predict(x_test)
print(y_pred)
x_train.shape
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse
r2=metrics.r2_score(y_test,y_pred)
r2
dtr.predict([[44,0,2,130,20]])
```

## Output:
### HEAD:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/c5f70415-f9fb-40f2-a198-9959de779f6e)
### TAIL:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/dac83dfd-a702-4005-b8a0-c590808358fa)
### DATASET INFO
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/5ddf23e9-aff2-42a7-97e8-725ecaf3fc62)
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/9f13560b-f051-492c-ae8b-82700e0be192)
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/b38214f6-ee0e-48a4-92d6-c41028352bc0)
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/fc0ad04c-8b59-420c-8b05-73c3487fbaeb)
### X DATA:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/d1a4ebe6-c1eb-4403-9989-596ed42d477c)
### DATASHAPE:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/80d0bebc-bde0-4d99-b34a-96011c525d88)
### Y_PRED:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/424b1372-9f1a-4f81-9206-a5ab08b678d1)
### MEAN_SQUARED_VALUE:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/aeca42dc-e68e-4c83-a41d-366f073273f2)
### R2 VALUE:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/a81c66d6-2d91-422d-873b-405fae7d0270)
### DTR PRODUCT:
![image](https://github.com/RahulM2005R/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/166299886/fcc485fa-f50f-4815-a584-8eccf389c8b6)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
