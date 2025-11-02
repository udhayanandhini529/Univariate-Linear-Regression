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

import numpy as np
import matplotlib.pyplot as plt
X= np.array([0,1,2,3,4,5,6,7,8,9])
Y= np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2

m=num/den
b=Y_Mean-(m*X_Mean)
print(f"Slope : {m}\nIntercept : {b}")
Y_Pred=(m*X)+b
print(f"Predicted values are : \n{Y_Pred}")
plt.scatter(X,Y,color='Red')
plt.plot(X,Y_Pred,color='Blue')
plt.show()






## Output
</br>
<img width="650" height="47" alt="image" src="https://github.com/user-attachments/assets/835d77dd-250e-4380-ab2b-52e9d56c0ed1" />
<img width="850" height="75" alt="image" src="https://github.com/user-attachments/assets/fd1397a4-3dcc-4bf8-b6fd-6fd24b77f690" />
<img width="532" height="397" alt="image" src="https://github.com/user-attachments/assets/e19598e6-a916-46c4-b547-133af4e47421" />
<img width="1052" height="470" alt="image" src="https://github.com/user-attachments/assets/d37125c4-770c-4757-bdef-85da99907258" />
<img width="666" height="499" alt="image" src="https://github.com/user-attachments/assets/a39e45d3-4c14-4b03-8049-5544ad65bd38" />


</br>
</br>
</br>

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
