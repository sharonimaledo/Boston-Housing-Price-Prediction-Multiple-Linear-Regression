# Boston Housing Price Prediction – Multiple Linear Regression
## Transforming Housing Data into Predictive Pricing Intelligence
This repository contains a complete regression analysis of the Boston Housing dataset.
Using Python and Scikit-learn, housing features were transformed into an interpretable predictive model to estimate property prices and identify the key factors influencing value.
## Key Insights
- Price Drivers:
The number of rooms (RM) has the strongest positive impact on house prices.

- Socioeconomic Impact:
Higher values of LSTAT are associated with lower property prices.

- Environmental Effect:
Higher pollution levels (NOX) and higher crime rates (CRIM) reduce house value.

- Location Advantage:
Properties near the Charles River (CHAS) show higher predicted prices.
## Model Performance
R² = 0.73
The model explains 73% of the variation in house prices, indicating a strong relationship between the features and MEDV.

RMSE = 4.41
On average, the model’s predictions differ from the actual house prices by about 4.41 units.
## Tools Used
Python: Data analysis and model development
- Pandas: Data cleaning and transformation

- Scikit-learn: Multiple linear regression modeling

- Matplotlib: Model performance visualization
## Analytical Highlight (Python)

Log transformation was applied to skewed variables to improve model performance:
```
house['crim'] = np.log1p(house['crim'])
house['zn'] = np.log1p(house['zn'])
house['lstat'] = np.log1p(house['lstat'])
```

Multiple linear regression model training:
```
X = house.drop('medv', axis=1)
y = house['medv']

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

model = LinearRegression()
model.fit(X_train, y_train)
```
## Repository Structure
- Project Brief

- Analysis: Jupyter Notebook containing data cleaning, feature engineering, model training, and evaluation

- Report: Final presentation slides summarizing findings and recommendations.

Report
Exported PDF summarizing methodology, insights, and recommendations
