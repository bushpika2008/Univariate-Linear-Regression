# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.

2.	Calculate the mean of the X -values and the mean of the Y -values.
   <img width="473" height="184" alt="Screenshot 2026-03-18 142731" src="https://github.com/user-attachments/assets/7d448fb0-6952-47df-ac52-d32db3b2ae65" />


4.	Find the slope m of the line of best fit using the formula.
  
5.	Compute the y -intercept of the line by using the formula:
   <img width="306" height="74" alt="Screenshot 2026-03-18 142736" src="https://github.com/user-attachments/assets/259485cd-c6dc-4c4e-8c4b-23c719c4a882" />

  

7.	Use the slope m and the y -intercept to form the equation of the line.

8.	Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()
```

## Output
<img width="960" height="623" alt="image" src="https://github.com/user-attachments/assets/a510b93d-f738-43f4-9419-17ed417311e9" />
<img width="912" height="562" alt="image" src="https://github.com/user-attachments/assets/9f008f37-8be0-4338-93b1-1f8e8b277032" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
