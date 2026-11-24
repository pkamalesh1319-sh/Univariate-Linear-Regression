
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
#Name : Kamalesh P
#Reg num: 26014307
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
</br><img width="1127" height="657" alt="Screenshot 2026-11-24 091859" src="https://github.com/user-attachments/assets/b5d60cea-e32b-44e6-9c42-a862e73473b9" />

</br><img width="990" height="606" alt="Screenshot 2026-11-24 091910" src="https://github.com/user-attachments/assets/28e2dd93-f4d5-452d-9a29-e7ca4b2a1213" />

</br><img width="1082" height="556" alt="Screenshot 2026-11-24 091916" src="https://github.com/user-attachments/assets/5aebf0e4-22c8-433e-b03b-9e01052c9164" />




## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
