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
Developed by: your name:Mohanram Gunasekar
RegisterNumber: 212223240095

import numpy as np
import matplotlib.pyplot as plt

X = np.array(eval(input()))
Y = np.array(eval(input()))

Xmean = np.mean(X)
Ymean = np.mean(Y)
num,den = 0,0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
    
print (m, c)

Y_pred = m*X + c
print (Y_pred)

plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()
```
## Output:
![331241425-98cf4433-dcb9-4280-95d0-e8a4b7f16a89](https://github.com/MohanramGunasekar/Univariate-Linear-Regression/assets/139841812/ffa22a77-ce50-4992-b51c-8756cc0e3303)
![331241515-c8a34de5-4413-461b-b89c-71c9e3df9432](https://github.com/MohanramGunasekar/Univariate-Linear-Regression/assets/139841812/9941aa41-9d73-4271-a8bb-cc2b0b018c2a)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
