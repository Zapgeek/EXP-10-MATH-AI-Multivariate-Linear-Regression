# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas as pd.

### Step2
Read the csv file.

### Step3
Get the value of X and y variables

### Step4
Create the linear regression model and fit.

### Step5
Predict the CO2 emission of a car where the weight is 2300kg, and the volume is 1300cm cube.
## Program:
```

"""
"""
Done by: Pranav Bhargav M
Reg No : 212224040239

"""
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("/content/car (1).csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
predictedCO2 = regr.predict(pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume']))
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)




```
## Output:

```
Coefficients: [0.00755095 0.00780526]
Intercept: 79.69471929115939
Predicted CO2 for the corresponding weight and volume: [114.75968007]

```

### Insert your output
<img width="1456" height="495" alt="image" src="https://github.com/user-attachments/assets/33cfc8a0-d51f-4120-a64f-144983497630" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
