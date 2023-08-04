# South African Heart Disease Analysis

## Introduction

This repository contains a detailed analysis of the South African Heart Disease dataset (`SAheart.csv`). The project's objective is to predict the occurrence of coronary heart disease (`chd`) using various features like systolic blood pressure, tobacco usage, low-density lipoprotein cholesterol level, and more. The analysis includes data visualization, data balancing, model training, hyperparameter tuning, and feature importance analysis.

## Dataset Overview

The dataset consists of the following columns:

- `sbp`: Systolic blood pressure (int)
- `tobacco`: Cumulative tobacco consumption (float)
- `ldl`: Low-density lipoprotein cholesterol (float)
- `adiposity`: Adipose tissue concentration (float)
- `famhist`: Family history of heart disease (object)
- `typea`: Type-A behavior (int)
- `obesity`: Obesity index (float)
- `alcohol`: Alcohol consumption (float)
- `age`: Age (int)
- `chd`: Coronary heart disease (target variable, int)

### Data Distribution

- Cases without coronary heart disease: 302
- Cases with coronary heart disease: 160

![Countplot of CHD](countplot_chd.png)

## Preprocessing

- Upsampling of the minority class to balance the dataset.
- One-hot encoding of categorical variables.
- Splitting the dataset into training and testing sets.

## Models

### Logistic Regression

- Original Data Accuracy: 76.34%
- Balanced Data Accuracy: 71.07%

### Random Forest Classifier

- Hyperparameter Tuning with GridSearchCV
- Best Parameters: `{'max_depth': 9, 'max_features': 0.1, 'n_estimators': 500}`
- Best AUC-ROC Score: 0.9049
- Final Model Accuracy: 77.69%

## Feature Importance Analysis

- Tobacco: 14.62%
- Age: 13.30%
- LDL: 13.25%
- Adiposity: 12.12%
- Type-A Behavior: 11.07%
- Obesity: 10.73%
- SBP: 10.03%
- Alcohol: 9.62%
- Family History: 5.25%

## Requirements

- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Usage

1. Clone this repository.
2. Navigate to the directory containing the code.
3. Run the main script or Jupyter Notebook.

## Contribution

Feel free to fork the repository and contribute. If you have any questions or need further assistance, you can open an issue or contact the maintainers.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
