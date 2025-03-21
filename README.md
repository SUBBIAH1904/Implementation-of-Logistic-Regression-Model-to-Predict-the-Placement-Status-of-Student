# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

Step 1. Start

Step 2. Load the California Housing dataset and select the first 3 features as input (X) and target variables (Y) (including the target price and another feature).

Step 3. Split the data into training and testing sets, then scale (standardize) both the input features and target variables.

Step 4. Train a multi-output regression model using Stochastic Gradient Descent (SGD) on the training data.

Step 5. Make predictions on the test data, inverse transform the predictions, calculate the Mean Squared Error, and print the results.

Step 6. Stop

## Program & Output:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
Developed by: Subbiah S
RegisterNumber: 212223220111
*/
```
~~~
import pandas as pd
data=pd.read_csv('/content/Placement_Data.csv')
data.head(5)
~~~
![image](https://github.com/user-attachments/assets/cd89d34d-6c2a-420e-a0db-8be612c81842)

~~~
data1=data.copy()
data1=data1.drop(["sl_no","salary"],axis=1)
data1.head()
~~~
![image](https://github.com/user-attachments/assets/08bab0f2-9ed6-4ba9-bdf5-2ce81b451040)

~~~
data1.isnull().sum()
~~~
![image](https://github.com/user-attachments/assets/c4ab9a49-2dfb-47bc-bfe1-2621f7989735)

~~~
data1.duplicated().sum()
~~~
![image](https://github.com/user-attachments/assets/e45217f7-9d5a-46c1-acd9-a32af7cad022)

~~~
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data1["gender"]=le.fit_transform(data1["gender"])
data1["ssc_b"]=le.fit_transform(data1["ssc_b"])
data1["hsc_b"]=le.fit_transform(data1["hsc_b"])
data1["hsc_s"]=le.fit_transform(data1["hsc_s"])
data1["degree_t"]=le.fit_transform(data1["degree_t"])
data1["workex"]=le.fit_transform(data1["workex"])
data1["specialisation"]=le.fit_transform(data1["specialisation"])
data1["status"]=le.fit_transform(data1["status"])
data1
~~~
![image](https://github.com/user-attachments/assets/410538ce-2548-4121-945b-c7676e121438)

## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
