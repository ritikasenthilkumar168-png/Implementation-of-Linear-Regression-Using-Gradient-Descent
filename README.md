# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Load dataset and select input (R&D Spend) and output (Profit).
Normalize the input data.
2. Initialize parameters (m, b) and set learning rate and epochs.
3. Apply gradient descent to update m and b using prediction error.
4. Predict output and plot the regression line with data points.  

## Program:
```
/*
Program to implement the linear regression using gradient descent.
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

# Load dataset
data = pd.read_csv("Startup.csv")

# Select one feature (R&D Spend) and target (Profit)
X = data['R&D Spend'].values
y = data['Profit'].values

# Normalize (important for gradient descent)
X = (X - X.mean()) / X.std()

# Initialize parameters
m = 0
b = 0

learning_rate = 0.01
epochs = 1000
n = len(X)

# Gradient Descent
for i in range(epochs):
    y_pred = m * X + b
    
    # Gradients
    dm = (-2/n) * np.sum(X * (y - y_pred))
    db = (-2/n) * np.sum(y - y_pred)
    
    # Update
    m = m - learning_rate * dm
    b = b - learning_rate * db

print("Slope (m):", m)
print("Intercept (b):", b)

# Predictions for plotting
y_pred = m * X + b

# Plot
plt.scatter(X, y)
plt.plot(X, y_pred)

plt.xlabel("R&D Spend (Normalized)")
plt.ylabel("Profit")
plt.title("Gradient Descent on 50_Startups Dataset")

plt.show()
Developed by: Ritika S
RegisterNumber:  212225220086
*/
```
## Output:
![linear regression using gradient descent](sam.png)
<img width="699" height="854" alt="image" src="https://github.com/user-attachments/assets/9df21c17-4ff9-42fd-b80a-ffb5f53723d7" />

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
