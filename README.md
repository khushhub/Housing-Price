#  House Price Prediction using Machine Learning

A complete end-to-end Machine Learning project that predicts house prices using the California Housing Dataset (used as a proxy for Gurgaon housing data). The project demonstrates the entire ML workflow, from data preprocessing and exploratory data analysis (EDA) to model training, evaluation, and deployment using Scikit-learn pipelines.

---

##  Project Overview

This project aims to build a robust house price prediction model by following industry-standard machine learning practices.

The workflow includes:

- Data Collection
- Exploratory Data Analysis (EDA)
- Data Cleaning
- Feature Engineering
- Data Preprocessing
- Model Training
- Model Evaluation
- Cross Validation
- Model Persistence
- Prediction on New Data

The California Housing dataset is used as a simulated Gurgaon housing dataset.

---

##  Features

- End-to-End Machine Learning Pipeline
- Exploratory Data Analysis (EDA)
- Missing Value Handling
- Feature Scaling
- One-Hot Encoding for Categorical Features
- Stratified Train-Test Split
- Multiple Regression Models
- Cross Validation
- Model Saving using Joblib
- Inference on New CSV Files
- Production-Ready Preprocessing Pipeline

---

##  Project Structure

```
House-Price-Prediction/
│
├── housing.csv              # Training dataset
├── input.csv                # New input data
├── output.csv               # Predictions
│
├── model.pkl                # Saved Random Forest Model
├── pipeline.pkl             # Saved Preprocessing Pipeline
│
├── train.py                 # Model Training Script
├── predict.py               # Inference Script
│
├── requirements.txt
└── README.md
```

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib

---

##  Dataset

Dataset Used:

- California Housing Dataset

The dataset contains housing-related attributes such as:

- Longitude
- Latitude
- Housing Age
- Total Rooms
- Total Bedrooms
- Population
- Households
- Median Income
- Ocean Proximity
- Median House Value (Target)

---

##  Exploratory Data Analysis (EDA)

The following analyses are performed:

- Dataset Overview
- Missing Value Detection
- Statistical Summary
- Feature Distribution
- Correlation Analysis
- Scatter Plots
- Scatter Matrix
- Geographic Visualization

Useful commands:

```python
df.head()
df.info()
df.describe()
df.value_counts()
```

---

##  Data Preprocessing

The preprocessing pipeline includes:

- Missing Value Imputation
- Numerical Feature Scaling
- One-Hot Encoding
- Stratified Sampling
- ColumnTransformer
- Pipeline

Numerical Pipeline:

- Median Imputation
- StandardScaler

Categorical Pipeline:

- OneHotEncoder

---

##  Machine Learning Models

The following regression models are trained:

### Linear Regression

- Simple baseline model

### Decision Tree Regressor

- Captures non-linear relationships

### Random Forest Regressor

- Ensemble learning method
- Best performing model

<img width="872" height="291" alt="image" src="https://github.com/user-attachments/assets/64af6d26-2e67-4e52-ae8d-12957ee62447" />


---

##  Model Evaluation

Performance is evaluated using:

- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- Cross Validation

Evaluation Metrics:

```text
RMSE
MAE
Cross Validation Score
```

---

##  Cross Validation

10-Fold Cross Validation is used to estimate model performance and reduce overfitting.

```python
cross_val_score(
    model,
    X_train,
    y_train,
    scoring="neg_root_mean_squared_error",
    cv=10
)
```

---

##  Model Persistence

The trained model and preprocessing pipeline are saved using Joblib.

```python
joblib.dump(model, "model.pkl")
joblib.dump(pipeline, "pipeline.pkl")
```

Later they can be loaded without retraining.

```python
model = joblib.load("model.pkl")
pipeline = joblib.load("pipeline.pkl")
```

---

##  Inference

To predict prices for new houses:

1. Place the new data inside:

```
input.csv
```

2. Run the prediction script.

3. Predictions will be saved as:

```
output.csv
```

---

##  Workflow

```
Load Dataset
      │
      ▼
Exploratory Data Analysis
      │
      ▼
Train-Test Split
      │
      ▼
Preprocessing Pipeline
      │
      ▼
Feature Engineering
      │
      ▼
Model Training
      │
      ▼
Model Evaluation
      │
      ▼
Cross Validation
      │
      ▼
Save Model
      │
      ▼
Inference on New Data
```

---

##  Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/House-Price-Prediction.git
```

Move into the project directory:

```bash
cd House-Price-Prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

##  Running the Project

### Train the Model

```bash
python train.py
```

### Predict House Prices

```bash
python predict.py
```

---

##  Future Improvements

- Hyperparameter Tuning
- XGBoost
- LightGBM
- CatBoost
- Feature Selection
- Model Explainability (SHAP)
- Flask/FastAPI Deployment
- Streamlit Web Application
- Docker Support
- CI/CD Integration

---

##  Learning Outcomes

This project demonstrates:

- Machine Learning Workflow
- Data Cleaning
- Feature Engineering
- EDA
- Scikit-learn Pipelines
- Regression Algorithms
- Model Evaluation
- Cross Validation
- Model Serialization
- Production-Ready Inference

---

##  Author

**Khushi**

B.Tech Computer Science Engineering
