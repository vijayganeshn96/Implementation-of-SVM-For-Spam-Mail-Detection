# Ex.No13_Learning_miniproject
# Implementation-of-SVM-For-Spam-Mail-Detection
### DATE:                                                                            
### REGISTER NUMBER : 212221040177

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Start the program.
2. Import the packages required.
3. Check data.head,info ana isnull operations.
4. Assign x and y values and v1,v2 values.
5. From sklearn import the required classes and functions.
6. Import Countvectorizer.
7. Transform data  and fit it in training data set.
8. Use svc.
9. Y_pred predict y.
10. End the program

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
