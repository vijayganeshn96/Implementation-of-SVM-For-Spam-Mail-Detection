# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Vijay Ganesh N
RegisterNumber: 212221040177
*/
import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='latin-1')
data.head()
data.info()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
# count vectorizer it is a method to convert text to numerical data
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy

```

## Output:
#### Data head
![SVM For Spam Mail Detection](https://github.com/vijayganeshn96/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/Screenshot%202022-06-19%20180349.png)
#### Final output for spam detection
![SVM For Spam Mail Detection](https://github.com/vijayganeshn96/Implementation-of-SVM-For-Spam-Mail-Detection/blob/main/svc.png)
## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
