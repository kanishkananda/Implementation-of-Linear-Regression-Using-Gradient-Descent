# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load dataset and take X (R&D Spend) and y (Profit).
2. Normalize X and initialize m = 0, b = 0.
3. Predict: y_pred=mX+b
4. Update m and b using gradient descent for given epochs.
5. Print results and plot graph  

## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: N.KANISHKA
RegisterNumber: 212225230127
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Startup.csv")
X=data["R&D Spend"].values
y=data["Profit"].values
X=(X-X.mean())/X.std()
m=0
b=0

learning_rate=0.01
epochs=1000
n=len(X)

for i in range(epochs):
    y_pred=m*X+b
    dm=(-2/n)*np.sum(X*(y-y_pred))
    db=(-2/n)*np.sum(y-y_pred)
    
    m=m-learning_rate*dm
    b=b-learning_rate*db
print("Slope (m):",m)
print("Intercept (b):",b)
y_pred=m*X+b

plt.scatter(X,y)
plt.plot(X,y_pred)
plt.xlabel("R&D Spend (Normalized)")
plt.ylabel("Profit")
plt.title("Gradient Descent on 50_startups Dataset")
plt.show()
*/
```

## Output:
<img width="1036" height="727" alt="image" src="https://github.com/user-attachments/assets/66a164c9-17b3-4058-b9e0-c38b2917de0a" />


## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
