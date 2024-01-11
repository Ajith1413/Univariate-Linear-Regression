# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: AJITH KUMAR A
#register number: 23002150

import numpy as np
import matplotlib.pyplot as py
x=np.array(eval(input()))
y=np.array(eval(input()))
x_mean=np.mean(x)
y_mean=np.mean(y)
num,denom=0,0
for i in range (len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
m=num/denom
b=y_mean-(m*x_mean)
print(m,b)
y_pred=(m*x)+b
print(y_pred)
py.scatter(x,y,color='pink')
py.plot(x,y_pred,color='blue')
py.show()
```
## Output
![image](https://github.com/Ajith1413/Univariate-Linear-Regression/assets/139842524/572414a9-8010-4e12-bd71-b6736951a4f2)

![image](https://github.com/Ajith1413/Univariate-Linear-Regression/assets/139842524/93a9d0b3-e461-4d8f-aea3-720be77c8d78)

![image](https://github.com/Ajith1413/Univariate-Linear-Regression/assets/139842524/a83fb8cc-f43f-4abc-9d6e-4cfaef81cd0e)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
