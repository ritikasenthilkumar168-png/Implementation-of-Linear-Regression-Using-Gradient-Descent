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
<img width="782" height="741" alt="Screenshot 2026-04-22 093625" src="https://github.com/user-attachments/assets/28f8eff6-1490-43d6-ab51-e872a4a7dac6" />
<img width="641" height="452" alt="Screenshot 2026-04-22 093641" src="https://github.com/user-attachments/assets/a2042a05-0b8d-4b1c-9366-45bc9b6bec98" />
<img width="786" height="559" alt="Screenshot 2026-04-22 093652" src="https://github.com/user-attachments/assets/cf35e5d1-b15d-4b27-a973-295fe9da3a1f" />

## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
