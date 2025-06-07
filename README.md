# Air Quality Prediction Under Changing Climate Using Deep Ensemble Models

## Overview
Air quality has become a critical global concern, especially under the escalating impacts of climate change. Rising temperatures, shifting weather patterns, and increasing urbanization have intensified air pollution levels, necessitating advanced predictive modeling approaches. This project aims to predict PM2.5 concentrations, a key indicator of air quality, using a deep ensemble learning framework. By leveraging multiple deep learning models, the ensemble approach mitigates individual model biases and enhances the robustness and accuracy of predictions. This methodology not only improves generalization across varying climatic scenarios but also provides a reliable tool for policymakers and environmental agencies to anticipate air quality trends and implement timely interventions.

## Dataset
The dataset includes various environmental and climatic features:
- Temperature
- Humidity
- Wind Speed
- CO2
- NO2
- SO2
- O3
- PM2.5 (Target Variable)

The data is stored in `air_quality_climate_data.xlsx`.

## Requirements
- Python 3.x
- TensorFlow
- Pandas
- NumPy
- Scikit-learn
- Joblib

Install the required libraries:
```bash
pip install tensorflow pandas numpy scikit-learn joblib
```

## Usage
1. Load the dataset.
2. Preprocess the data (standardization).
3. Train an ensemble of deep learning models.
4. Predict and evaluate using Mean Squared Error and R-squared metrics.
5. Save the trained models and scaler for future use.

## Model Architecture
Each model in the ensemble has the following architecture:
- Dense layer (128 units, ReLU activation)
- Dropout (30%)
- Dense layer (64 units, ReLU activation)
- Dropout (30%)
- Dense layer (32 units, ReLU activation)
- Output Dense layer (1 unit, no activation)

Optimizer: Adam with learning rate 0.001
Loss: Mean Squared Error

## Output
- Trained model files: `air_quality_model_0.h5`, `air_quality_model_1.h5`, etc.
- Scaler file: `scaler.pkl`
- Evaluation metrics printed on console.

## Author
**Ayebawanaemi Geraldine Winston**
