# ProteinStabilityPredictor

ProteinStabilityPredictor is a machine learning-based tool designed to predict the stability changes (ΔΔG) in proteins caused by mutations. This project leverages advanced feature engineering, outlier handling, and deep learning techniques to provide accurate predictions of protein stability changes.

## Features

- **Feature Engineering**:
  - One-hot encoding of categorical variables such as secondary structure, mutation type, and amino acids.
  - Calculation of physicochemical property changes (e.g., hydrophobicity, volume, and charge).
- **Outlier Handling**:
  - Removal of outliers using statistical methods like Z-scores or IQR.
- **Machine Learning Models**:
  - Support for Random Forest, Gradient Boosting, and Deep Learning models using TensorFlow/Keras.
- **Evaluation Metrics**:
  - Mean Squared Error (MSE), R² Score, Mean Absolute Error (MAE), and ROC AUC for classification tasks.
- **Visualization**:
  - Actual vs. Predicted plots for regression.
  - ROC AUC curves for classification.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ProteinStabilityPredictor.git
   cd ProteinStabilityPredictor