# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load the dataset into a DataFrame and explore its contents to understand the data structure. 
2.Separate the dataset into independent (X) and dependent (Y) variables, and split them into training and testing sets. 
3.Create a linear regression model and fit it using the training data. 
4.Predict the results for the testing set and plot the training and testing sets with fitted lines. 
5.Calculate error metrics (MSE, MAE, RMSE) to evaluate the model’s performance. 


## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: S.VISANIYA
RegisterNumber:  212225040492

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score


df = pd.read_csv(r"C:\Users\acer\Downloads\student_scores.csv")


print(df.head())


plt.scatter(df['Hours'], df['Scores'])
plt.xlabel("Hours")
plt.ylabel("Scores")


x = df[['Hours']]
y = df['Scores']

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2, random_state=0)


lr = LinearRegression()
lr.fit(x_train, y_train)


y_pred = lr.predict(x_test)


plt.scatter(df['Hours'], df['Scores'])
plt.plot(x_train, lr.predict(x_train))
plt.xlabel("Hours")
plt.ylabel("Scores")


print("Slope (Coefficient):", lr.coef_)
print("Intercept:", lr.intercept_)


mse = mean_squared_error(y_test, y_pred)
rmse = np.sqrt(mse)
mae = mean_absolute_error(y_test, y_pred)
r2 = r2_score(y_test, y_pred)

print("MSE:", mse)
print("RMSE:", rmse)
print("MAE:", mae)
print("R2 Score:", r2)
*/
```

## Output:
<img width="1100" height="768" alt="Screenshot 2026-04-29 102824" src="https://github.com/user-attachments/assets/9225065e-9ab7-434c-81ee-5a707a972d86" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
