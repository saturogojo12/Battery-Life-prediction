# Battery Remaining Useful Life Prediction

## Overview
This project focuses on predicting the Remaining Useful Life (RUL) of batteries using machine learning algorithms. The dataset used in this project contains battery data with various features and the target variable is the RUL of the battery. The objective is to evaluate and compare different regression algorithms to predict RUL effectively.

## Dataset
The dataset used is `Battery_RUL.csv`, which includes the following features:
- **Cycle Index**: Number of cycles.
- **Discharge Time (s)**: Time spent in discharge.
- **Decrement 3.6-3.4V (s)**: Time spent in the decrement range.
- **Max. Voltage Discharge (V)**: Maximum voltage during discharge.
- **Min. Voltage Charge (V)**: Minimum voltage during charging.
- **Time at 4.15V (s)**: Time at 4.15V.
- **Time Constant Current (s)**: Time at constant current.
- **Charging Time (s)**: Time spent charging.
- **RUL**: Remaining Useful Life (target variable).

## Project Steps

### 1. Data Loading and Description
- Loaded the dataset using `pandas`.
- Described the dataset and confirmed no missing data.

### 2. Exploratory Data Analysis (EDA)
- Visualized the distribution of RUL and other features using `seaborn` and `matplotlib`.
- Conducted correlation analysis and pair plots to understand relationships between features.
- Divided data into different ranges of RUL for better distribution.

### 3. Data Preprocessing
- Standardized features using `StandardScaler`.
- Split the dataset into training and testing sets.

### 4. Modeling with Whole Data
- Evaluated various regression algorithms:
  - **RandomForestRegressor**
  - **AdaBoostRegressor**
  - **GradientBoostingRegressor**
  - **BaggingRegressor**
  - **SVR**
  - **DecisionTreeRegressor**
  - **ExtraTreeRegressor**
  - **LinearRegression**
  - **SGDRegressor**
  - **KNeighborsRegressor**
- Compared performance using metrics such as MSE and RMSE.

### 5. Modeling with Divided Data
- Divided data into three segments based on RUL and performed regression analysis.
- Evaluated the same set of algorithms on each divided dataset.

### 6. Model Comparisons
- **RandomForestRegressor**: Compared results on whole data and divided data.
- **BaggingRegressor**: Compared results on whole data and divided data.
- **DecisionTreeRegressor**: Compared results on whole data and divided data.

### 7. Feature Importance
- Evaluated feature importance using the RandomForestRegressor.

## Results
- **RandomForestRegressor** showed the best performance with the lowest RMSE in most cases.
- **BaggingRegressor** and **DecisionTreeRegressor** also performed well, especially with the divided datasets.

## Installation
To run this project, you need the following Python libraries:
- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `plotly`
- `scikit-learn`

Install the necessary libraries using pip:
```bash
pip install numpy pandas matplotlib seaborn plotly scikit-learn
