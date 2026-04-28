# Implementation-of-Logistic-Regression-Model-to-Predict-the-Placement-Status-of-Student

## AIM:
To write a program to implement the the Logistic Regression Model to Predict the Placement Status of Student.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:

1. Collect student data and clean it properly.
2. Train the Logistic Regression model using the data.
3. Use the model to predict whether a student is placed or not.
4. Check the accuracy of the model results. 

## Program:
```
/*
Program to implement the the Logistic Regression Model to Predict the Placement Status of Student.
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression

# Load dataset
data = pd.read_csv("Placement_Data (1).csv")

# Drop salary column (contains missing values)
data = data.drop("salary", axis=1)

# Convert categorical data to numeric
data = pd.get_dummies(data, drop_first=True)

# Features and target
X = data.drop("status_Placed", axis=1)
y = data["status_Placed"]

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Train model
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)

# Accuracy
print("Accuracy:", model.score(X_test, y_test))


# -------------------------------
# 📈 Logistic Regression Plot
# -------------------------------

# Use only ONE feature for plotting
X1 = X.iloc[:, 0].values.reshape(-1, 1)

# Train model on single feature
model_plot = LogisticRegression(max_iter=1000)
model_plot.fit(X1, y)

# Scatter plot
plt.scatter(X1, y, color='blue')

# Sigmoid curve
x_values = np.linspace(X1.min(), X1.max(), 100)
y_values = model_plot.predict_proba(x_values.reshape(-1,1))[:,1]

plt.plot(x_values, y_values)

plt.xlabel("Feature")
plt.ylabel("Probability")
plt.title("Logistic Regression Curve")
plt.show()
Developed by: Ritika S
RegisterNumber: 212225220086
*/
```

## Output:
![the Logistic Regression Model to Predict the Placement Status of Student](sam.png)
<img width="765" height="641" alt="Screenshot 2026-04-28 113100" src="https://github.com/user-attachments/assets/7b75a438-f154-4ad7-87de-9b7d38252d8f" />


## Result:
Thus the program to implement the the Logistic Regression Model to Predict the Placement Status of Student is written and verified using python programming.
