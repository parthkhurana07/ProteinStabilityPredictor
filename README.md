# Predicting Protein Stability Changes (ΔΔG) with Deep Learning

## Project Overview
This project uses deep learning to predict changes in protein stability (ΔΔG) caused by mutations. Protein stability is key to proper function, and understanding changes due to mutations can help in designing stable proteins and studying genetic disorders.

## Dataset: ThermoMutDB
**ThermoMutDB** is used in this project. It contains experimental data on protein stability changes due to mutations.  
**How to get it:**  
- Search for ThermoMutDB on ResearchGate or in related publications.
- Place the downloaded file as `data/thermomutdb.json`.

## Project Workflow

### 1. Data Loading
Load the JSON data into a pandas DataFrame:
```python
import pandas as pd
df = pd.read_json('data/thermomutdb.json')
```

### 2. Data Preprocessing
- **Handle Missing Values**: Impute missing values (using the median for numeric data).
- **Feature Engineering**: Extract and create features (e.g., one-hot encoding for categorical data, hydrophobicity, and molecular weight changes).

### 3. Deep Learning Model
- **Model Architecture**: A deep neural network (DNN) with multiple layers, dropout for regularization, and ReLU activations.
- **Training**: Experiment with different architectures and hyperparameters to improve performance.
- **Saving the Model**: The best model is saved as `models/best_model.h5`.

### 4. Model Evaluation
Key metrics include:
- R² (Coefficient of Determination)
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)

### 5. Using the Model
Load the trained model and make predictions:
```python
from tensorflow.keras.models import load_model
model = load_model('models/best_model.h5')
predictions = model.predict(new_data)
```
Make sure your input data is preprocessed similarly to the training data.

## Required Libraries
- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- tensorflow
- scipy

## Contributions & Future Work
Contributions are welcome. Future work may include:
- Advanced hyperparameter tuning.
- Feature importance analysis.
- Further refinement of the neural network architecture.

## License
This project is released under the MIT License. Feel free to fork, modify, and contribute.

## Contact
For questions or collaboration, please reach out!
