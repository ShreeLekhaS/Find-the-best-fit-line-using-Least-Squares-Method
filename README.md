# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program and Output:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Shree Lekha.S
RegisterNumber: 212223110052
*/
```
```
import numpy as np
import matplotlib.pyplot as plt

x = np.array(eval(input()))
y = np.array(eval(input()))

```
![image](https://github.com/user-attachments/assets/15c0d21b-deac-4b72-bf86-9ad670bbb545)
```
xmean = np.mean(x)
ymean = np.mean(y)

num=0
denom=0

for i in range(len(x)):
  num+=(x[i]-xmean)*(y[i]-ymean)
  denom+=(x[i]-xmean)**2

m=num/denom
b=ymean-m*xmean
print(m,b)

```
![image](https://github.com/user-attachments/assets/63354954-8da9-43c3-a18f-644dcb1adb00)

```
y_predicted = m*x+b
print(y_predicted)
```
![image](https://github.com/user-attachments/assets/92582c8a-21be-4a1c-afe3-73a1471c7f52)
```
plt.scatter(x,y)
plt.plot(x,y_predicted)
plt.show()
```
![image](https://github.com/user-attachments/assets/4c90a04c-c4b7-4a72-84f9-ccc6f988c99b)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
