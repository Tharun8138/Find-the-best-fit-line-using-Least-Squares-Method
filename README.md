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
import numpy as np
import matplotlib.pyplot as plt

#Input array - X and Y
x=np.array(eval(input()))
y=np.array(eval(input()))

#Mean Extraction
x_mean=np.mean(x)
y_mean=np.mean(y)

#formula Implementation
num, denom = 0, 0

for i in range(len(x)):
  num += ((x[i] - x_mean)* (y[i] - y_mean))
  denom += (x[i] - x_mean)**2

m = num/denom
b = y_mean - m * x_mean

print(m, b)

y_predicted=m*x+b
y_predicted

plt.scatter(x,y,color='black')
plt.plot(x, y_predicted,color='red')
plt.show()

print(m*3+b)

```

## Output:
![Screenshot 2025-02-26 162950](https://github.com/user-attachments/assets/5c11819e-0d15-4bff-b830-d89e65572740)

![Screenshot 2025-02-26 162959](https://github.com/user-attachments/assets/5218e48c-8d1b-4aa3-b10c-e841846ce754)
![Screenshot 2025-02-26 162855](https://github.com/user-attachments/assets/59df8818-14ba-4366-977c-6575c2e7fc25)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
