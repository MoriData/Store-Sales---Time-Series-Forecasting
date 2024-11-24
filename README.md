# Store Sales - Time Series Forecasting

## Project Overview

This project focuses on predicting daily sales for multiple stores using historical sales data. Accurate sales forecasting is crucial for optimizing inventory management, staffing, and promotional strategies.

## Dataset Description

The dataset comprises the following files:
- `train.csv`: Historical sales data with features such as store number, product family, and promotion status, along with the target variable `sales`.
- `test.csv`: Data for which sales predictions are to be made, containing the same features as the training set.
- `stores.csv`: Metadata about each store, including city, state, type, and cluster information.
- `oil.csv`: Daily oil prices, which can influence economic conditions and, consequently, sales.
- `holidays_events.csv`: Information on holidays and events that may impact sales patterns.

## Approach

### 1. Data Preprocessing
- Merged datasets to create a comprehensive training set.
- Handled missing values and performed data cleaning.
- Extracted date-related features such as day of the week, month, and year.

### 2. Feature Engineering
- Created lag features to capture past sales trends.
- Incorporated rolling mean and standard deviation to account for seasonality.
- Included external factors like oil prices and holiday indicators.

### 3. Modeling
- Utilized the CatBoost Regressor, a gradient boosting algorithm that handles categorical features efficiently.
- Applied log transformation to the target variable to stabilize variance and improve model performance.

### 4. Validation
- Employed a time-based validation split to simulate real-world forecasting scenarios.
- Evaluated model performance using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

## Results

The model demonstrated strong predictive capabilities, achieving:
- **Validation MAE**: 87.27
- **Validation RMSE**: 317.18

These metrics indicate the model's effectiveness in capturing sales patterns and trends.
