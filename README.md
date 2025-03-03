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

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: KEERTHANA V
RegisterNumber: 212223220045
```
```
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
x_mean=np.mean(x)
y_mean=np.mean(y)
num=0
denom=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    denom+=(x[i]-x_mean)**2
m=num/denom
c=y_mean-m*(x_mean)
print("Slope",m)
print("y intercept",c)
y_pred=(m*x)+c
print("Predicted Value",y_pred)
plt.scatter(x,y)
plt.plot(x,y_pred,color='red')
plt.show()
```

## Output:
### Input Data:
<img width="368" alt="image" src="https://github.com/user-attachments/assets/5613e8d8-02b6-4d4d-8f69-48a688c2ac68" />

### Slope:
<img width="199" alt="image" src="https://github.com/user-attachments/assets/6a717963-ac76-43d5-a2b0-b7fea2b9c28e" />

### Y-intercept:
<img width="259" alt="image" src="https://github.com/user-attachments/assets/33a8c2c8-a85f-45b7-82b1-614b4c8d4884" />

### Predicted y values:
<img width="722" alt="image" src="https://github.com/user-attachments/assets/f89cdf89-c265-47ac-951f-2a86e2c87fbf" />

### Best-fit-line:
<img width="428" alt="image" src="https://github.com/user-attachments/assets/54bbffb1-d9c3-4775-bbb2-1e7925aa0125" />


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
