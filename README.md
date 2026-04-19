# Concrete Compressive Strength Prediction

This project builds a machine learning model to predict **concrete compressive strength** based on different cement mixture components and curing age. The model is implemented in **PyTorch** and uses several preprocessing and evaluation techniques to achieve reliable predictions.

## Project Goal

The goal of this project is to predict the **compressive strength of concrete (`Strength`)** using different material composition features such as cement, water, aggregates, and curing time.

The problem is formulated as a **regression task** where the model learns the relationship between mixture composition and final concrete strength.

## Dataset

The dataset is stored in the `Data` directory and contains two files:

- `train.csv`
- `test.csv`

### Training Data

The training dataset contains **824 rows and 12 columns**.

#### Features

- **Cement** — Cement amount (kg per m³)
- **Blast Furn Slag** — Blast furnace slag (kg per m³)
- **Fly Ash** — Fly ash content (kg per m³)
- **Water** — Water amount (kg per m³)
- **Superplas** — Superplasticizer amount (kg per m³)
- **Coarse Ag** — Coarse aggregate (kg per m³)
- **Fine Aggre** — Fine aggregate (kg per m³)
- **Age** — Concrete curing age (days)
- **cement per water** — Cement-to-water ratio
- **Cement Impurity Factor** — Cement impurity indicator
- **Cement Moisture Factor** — Cement moisture indicator

#### Target

- **Strength** — Concrete compressive strength (MPa)

## Technologies Used

- **Python**
- **NumPy**
- **Pandas**
- **PyTorch**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**

## Libraries

The notebook uses the following libraries:
```python
import numpy as np
import pandas as pd
import torch
import torch.nn as nn
import torch.optim as optim

import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split
from sklearn.metrics import (
mean_squared_error,
r2_score,
mean_absolute_error,
mean_absolute_percentage_error
)

## Workflow

The project follows these main steps:

1. Data loading
2. Exploratory Data Analysis (EDA)
3. Data preprocessing and normalization
4. Train-test split
5. Neural network model creation using PyTorch
6. Model training
7. Model evaluation
8. Visualization of results

## Model

A neural network regression model is implemented using **PyTorch**. The model learns to map input features representing material composition to the target variable: **concrete strength**.

## Evaluation Metrics

The model is evaluated using:

- **Mean Squared Error (MSE)**
- **Mean Absolute Error (MAE)**
- **Mean Absolute Percentage Error (MAPE)**
- **R² Score**

These metrics provide insight into prediction accuracy and model performance.

## Visualization

The project uses **Matplotlib** and **Seaborn** to visualize:

- Feature distributions
- Correlations
- Model performance

## Project Structure


.
├── Data
│   ├── train.csv
│   └── test.csv
├── notebook.ipynb
└── README.md

## How to Run

1. Clone the repository

bash
git clone https://github.com/amirclear/concrete-strength-prediction.git
cd concrete-strength-prediction

2. Install dependencies

bash
pip install numpy pandas torch matplotlib seaborn scikit-learn

3. Run the notebook

bash
jupyter notebook notebook.ipynb

## Future Improvements

- Hyperparameter tuning
- Trying different neural network architectures
- Feature engineering
- Cross-validation
- Model comparison with classical ML models (Random Forest, XGBoost, etc.)

## License

This project is for educational and research purposes.
`

If you want, I can also:
- make a **much more professional GitHub README (with badges, images, and results section)**  
- or add **model architecture + training results sections** based on the notebook.

## Source

https://quera.org/problemset/314559?tab=description