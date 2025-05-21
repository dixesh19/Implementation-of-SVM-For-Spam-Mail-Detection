# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import necessary libraries
2. Check the dataset for missing values and make necessary changes.
3. Split the dataset for Training and Testing purpose.
4. Implement SVM for the splitted datasets.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: DINESH R
RegisterNumber:  212224240037
import chardet 
file = "spam.csv"
with open(file,'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result
import pandas as pd

data = pd.read_csv("spam.csv",encoding = 'windows-1252')
data.head()
data.info()
data.isnull().sum()

x = data['v1'].values
y = data['v2'].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC
svc = SVC(kernel = 'linear')
svc.fit(x_train,y_train)
y_pred = svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy = metrics.accuracy_score(y_pred,y_test)
accuracy
*/
```

## Output:
![image](https://github.com/user-attachments/assets/5c80df7f-a00c-44b9-96a1-d243e174f925)
![image](https://github.com/user-attachments/assets/4000e530-316a-42d8-95bc-8b6df90ba276)
![image](https://github.com/user-attachments/assets/234af8a3-9cc5-4fa8-9c18-766360c04629)
![image](https://github.com/user-attachments/assets/24e8b703-03d0-4f6e-a569-8a75f144f447)
![image](https://github.com/user-attachments/assets/4fd019d5-e2fb-4b53-ba0b-313e6af82252)
## Accuracy
![image](https://github.com/user-attachments/assets/acb5201e-a2c6-4dd7-b4f1-03ded53a1f41)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
