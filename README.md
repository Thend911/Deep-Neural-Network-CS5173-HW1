# Cancer Mortality Rate Prediction

This project uses deep learning to predict cancer mortality rates using various neural network architectures implemented with TensorFlow.

## Project Structure

```
HW1_DL/
├── cancer_morality_rate.ipynb    # Main Jupyter notebook
├── cancer_reg-1.csv              # Dataset
├── requirements.txt              # Project dependencies
├── answer.md                     # Answers for step 1 
├── weights.md                    # Model weights documentation
└── README.md                     # This file
```
## Setup Instructions

### Prerequisites

- Python 3.8 or higher
- PowerShell (Windows)

### 1. Open the Project

Unzip folder and navigate to project directory:
```powershell
cd "...\HW1_DL"
```

### 2. Create Virtual Environment

```powershell
# Create virtual environment
python -m venv venv

# Activate virtual environment
.\venv\Scripts\Activate.ps1
```

**Note:** If you encounter PowerShell execution policy issues:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
```

### 3. Install Dependencies

```powershell
pip install -r requirements.txt
```

This will install:
- numpy>=1.26.0
- pandas>=2.1.0
- tensorflow>=2.15.0
- scikit-learn>=1.3.0
- matplotlib>=3.8.0

### 4. Install Jupyter

```powershell
pip install jupyter
```

## Running the Project

### Option A: Jupyter Notebook (Recommended)

```powershell
# Start Jupyter Notebook
jupyter notebook

# Open cancer_morality_rate.ipynb in your browser
```

### Option B: VS Code

1. Open the project folder in VS Code
2. Select your virtual environment as the Python interpreter
3. Open `cancer_morality_rate.ipynb`
4. Run cells all at once

## Usage

1. **Data Loading**: The notebook automatically loads the cancer dataset
2. **Data Preprocessing**: Handles missing values and skewed distributions
3. **Model Training**: Choose from 5 different model architectures
4. **Evaluation**: View MSE, R² scores, and loss plots

To test different models, modify the model selection in the testing section:
```python
# Choose model: 0-4
test_model(model_names[1])  # Change index to test different models
```

## Model Architectures

- `linear-reg`: Simple linear regression
- `dnn-16`: Single hidden layer (16 neurons)
- `dnn-30-8`: Two hidden layers (30, 8 neurons)
- `dnn-30-16-8`: Three hidden layers (30, 16, 8 neurons)
- `dnn-30-16-8-4`: Four hidden layers (30, 16, 8, 4 neurons)

## Hyperparameters

- Learning Rate: 0.001
- Epochs: 200
- Gradient Clipping: 5.0

## Deactivating Environment

When finished:
```powershell
deactivate
```

## Dependencies

See `requirements.txt` for the complete list of required packages and their versions.

## Results

The project evaluates each model using:
- Mean Squared Error (MSE) on test set
- R² Score for regression performance
- Training/validation loss plots
