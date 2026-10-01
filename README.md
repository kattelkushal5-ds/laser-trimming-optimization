# Laser Trimming Optimizer

[Live at](https://jumo-nc-prediction.vercel.app)
## Industrial Machine Learning Decision Support System

A machine learning-based decision support system developed as a team project to predict the optimal laser correction value (NCTr) for platinum thin-film resistance temperature sensors.

The system combines data preprocessing, feature engineering, XGBoost-based machine learning, MLflow tracking, a FastAPI backend, and a React frontend. The application was also deployed using Docker and Microsoft Azure.

## Key Results

- NCTr regression RMSE: **0.0202**
- R²: **0.9492**
- **99.63%** of predictions within the ±0.1 resistance tolerance
- Yield classification accuracy: **94.52%**

## Technologies

- Python
- Pandas / NumPy
- Scikit-learn
- XGBoost
- Optuna
- MLflow
- FastAPI
- React
- Vite
- SQLite
- Docker
- Microsoft Azure

## System Overview

```text
Manufacturing Data
        ↓
Data Preprocessing
        ↓
Feature Engineering
        ↓
XGBoost ML Model
        ↓
FastAPI Backend
        ↓
React Frontend
        ↓
Microsoft Azure
```

## Main Components

### Data Processing
- Integration of multiple manufacturing tables
- Sensor grouping
- Missing-value treatment
- Physical feature transformations
- Rolling historical features
- Leakage-safe train/test splitting

### Machine Learning
- XGBoost regression for NCTr prediction
- Hyperparameter optimization with Optuna
- Model evaluation using RMSE and R²
- MLflow for experiment and model tracking

### Backend
- REST API implemented with FastAPI
- Prediction endpoint for NCTr calculation
- Configuration endpoints
- Prediction history and audit logging

### Frontend
- React-based dashboard
- Sensor and manufacturing parameter input
- NCTr prediction visualization
- Tolerance and yield information
- Prediction history

### Deployment
- Backend containerized using Docker
- Backend deployed to Azure Container Apps
- Frontend deployed to Azure Static Web Apps
- GitHub Actions used for automated deployment

## Documentation

Detailed documentation is available in the `docs/` directory:

- [Project Overview](docs/01_PROJECT_OVERVIEW.md)
- [System Architecture & Deployment](docs/02_SYSTEM_ARCHITECTURE_AND_DEPLOYMENT.md)
- [Data Preprocessing & Sensor Grouping](docs/04_ML_MODELING_AND_VALIDATION_RESULTS.md)
- [ML Modeling & Validation](docs/04_ML_MODELING_AND_VALIDATION_RESULTS.md)
- [API & Frontend](docs/05_API_AND_FRONTEND_GUIDE.md)
- [Future Improvements](docs/06_FUTURE_IMPROVEMENTS_AND_RECOMMENDATIONS.md)

## My Contribution

My main contributions included:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- NCTr target definition and chronological target alignment
- Missing-value analysis and treatment
- Leakage-safe data splitting
- Feature engineering
- Model evaluation and validation

The chronological alignment of the training target with the final NCTr measurement reduced the regression RMSE from 0.1044 to 0.0202.

## Confidentiality

This project was developed using manufacturing data and project resources that are not publicly available.

For confidentiality reasons, the original production dataset, databases, MLflow tracking files, and proprietary source code are not included in this repository. This repository provides project documentation and selected non-sensitive information for portfolio purposes.
