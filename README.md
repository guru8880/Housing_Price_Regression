# Housing Price Prediction with Linear Regression

A compact regression project that explores housing data and trains a scikit-learn model to estimate home prices from numerical property features.

## Overview

The notebook demonstrates a complete baseline workflow: loading data, handling missing values, exploring relationships, splitting the dataset, fitting linear regression, and evaluating predictions.

If a local dataset is unavailable, the notebook creates a reproducible synthetic housing dataset so the workflow can still be executed.

## Workflow

```mermaid
flowchart LR
    A[Housing data] --> B[Explore and clean]
    B --> C[Impute missing values]
    C --> D[Train/test split]
    D --> E[Linear regression]
    E --> F[RMSE, MAE, and plots]
```

## Features

- exploratory summaries and visualizations
- missing-value handling with `SimpleImputer`
- linear regression baseline
- actual-versus-predicted and residual plots
- RMSE and MAE evaluation

The saved notebook run reports an RMSE of 6.14 and an MAE of 3.86 on its generated dataset. These values are tied to that dataset’s units.

## Tech Stack

- Python
- Pandas and NumPy
- scikit-learn
- Matplotlib
- Jupyter

## Project Structure

```text
.
|-- house_price_regression.ipynb
|-- requirements.txt
`-- README.md
```

## Installation and Usage

```bash
git clone https://github.com/guru8880/Housing_Price_Regression.git
cd Housing_Price_Regression
python -m venv venv
```

```bash
# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
```

```bash
pip install -r requirements.txt
jupyter lab
```

Open `house_price_regression.ipynb` and run the cells in order.

## Limitations

- Linear regression cannot naturally capture complex nonlinear price relationships.
- Synthetic-data metrics do not demonstrate performance on a real housing market.
- Location and other high-impact categorical variables are not modeled.

## Future Improvements

- evaluate on a documented real-world dataset
- add categorical and geospatial features
- compare regularized linear models and tree-based regressors
- use cross-validation and hyperparameter tuning
