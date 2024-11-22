# Laptop Price Prediction using Machine Learning

This project uses machine learning algorithms to predict laptop prices based on their specifications. By analyzing a dataset of laptop models and their configurations, this project provides accurate price predictions, offering valuable insights into price trends and specification impacts.

---

## Project Overview

### Objective
To leverage machine learning techniques for predicting laptop prices based on their specifications, enabling better understanding and decision-making.

### Dataset

#### Original Features:
The original dataset contains the following features:
- **Company**: Laptop manufacturer
- **TypeName**: Type of laptop (e.g., Ultrabook, Gaming, Notebook)
- **Inches**: Screen size
- **ScreenResolution**: Resolution of the laptop screen
- **Cpu**: Processor model and brand
- **Ram**: Amount of RAM (e.g., 8GB, 16GB)
- **Memory**: Storage details (e.g., 512GB SSD, 1TB HDD)
- **Gpu**: Graphics card details
- **OpSys**: Operating system
- **Weight**: Weight of the laptop
- **Price**: Target variable representing the price of the laptop

#### Features After Preprocessing:
After preprocessing and feature engineering, the dataset contains:
- **Company**: Laptop manufacturer
- **TypeName**: Type of laptop
- **Ram**: Amount of RAM in GB
- **Weight**: Weight of the laptop in kg
- **Price**: Laptop price (target variable)
- **TouchScreen**: Binary feature indicating if the laptop has a touchscreen
- **IPS**: Binary feature indicating if the screen has IPS technology
- **ppi**: Pixels per inch (calculated from screen resolution and screen size)
- **Cpu brand**: Extracted brand name of the processor
- **HDD**: Binary feature indicating presence of HDD storage
- **SSD**: Binary feature indicating presence of SSD storage
- **Gpu brand**: Extracted brand name of the graphics card
- **os**: Simplified operating system categories

---

## Key Tasks

1. **Data Exploration**:
   - Explored relationships between laptop features and prices.

2. **Feature Engineering**:
   - Added derived features such as:
     - `TouchScreen`
     - `IPS`
     - `ppi` (Pixels Per Inch)
     - `Cpu brand`
     - `Gpu brand`
     - Simplified `os` categories
   - Converted categorical data into numerical features for model compatibility.

3. **Preprocessing**:
   - Cleaned the dataset, handled missing values, and converted data types.

4. **Model Building**:
   - Implemented various regression models:
     - Linear Regression
     - Decision Tree Regressor
     - Random Forest Regressor
     - AdaBoost Regressor
     - XGBoost Regressor

5. **Model Evaluation**:
   - Evaluated models using metrics such as:
     - R-squared (R²)
     - Mean Squared Error (MSE)
     - Root Mean Squared Error (RMSE)
     - Mean Absolute Error (MAE)

6. **Hyperparameter Tuning**:
   - Optimized Random Forest and XGBoost models for improved accuracy.

---

## Results

The following table highlights the performance metrics for each model:

| Model            | Train R² | Test R² | Test MSE | Test RMSE | Test MAE  |
|-------------------|----------|---------|----------|-----------|-----------|
| Linear Regression | 0.832685 | 0.815430 | 0.075368 | 0.274531  | 0.213859  |
| Decision Tree     | 0.868534 | 0.826653 | 0.070785 | 0.266054  | 0.203464  |
| Random Forest     | 0.926936 | 0.875013 | 0.051037 | 0.225914  | 0.174711  |
| AdaBoost          | 0.819083 | 0.804794 | 0.079711 | 0.282331  | 0.233961  |
| XGBoost           | 0.988499 | 0.896291 | 0.042348 | 0.205787  | 0.158527  |
| RF (Tuned 1)      | 0.938635 | 0.876449 | 0.051037 | 0.225914  | 0.174711  |
| RF (Tuned 2)      | 0.966848 | 0.886692 | 0.051037 | 0.225914  | 0.174711  |

The **XGBoost Regressor** outperformed other models with the highest Test R² (0.896291) and the lowest Test MSE (0.042348).
