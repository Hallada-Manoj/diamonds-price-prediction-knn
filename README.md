# 💎 Diamonds Price Prediction using KNN Regression

## 📌 Project Overview

This project focuses on predicting diamond prices using the K-Nearest Neighbors (KNN) Regression algorithm. The workflow includes data preprocessing, feature engineering, pipeline creation, hyperparameter tuning, and model evaluation.

The objective is to build a machine learning model that can accurately estimate the price of a diamond based on its physical and quality-related characteristics.

---

## 🎯 Problem Statement

Diamond prices depend on multiple factors such as:

- Carat
- Cut
- Color
- Clarity
- Depth
- Table
- Dimensions (x, y, z)

The goal of this project is to predict the price of a diamond using these features and evaluate the performance of a KNN Regression model.

---

## 📂 Dataset Information

The dataset contains information about diamonds and their attributes.

### Features

| Feature | Description                           |
| ------- | ------------------------------------- |
| carat   | Weight of the diamond                 |
| cut     | Quality of the cut                    |
| color   | Diamond color grade                   |
| clarity | Clarity grade                         |
| depth   | Total depth percentage                |
| table   | Width of top relative to widest point |
| x       | Length (mm)                           |
| y       | Width (mm)                            |
| z       | Depth (mm)                            |

### Target Variable

| Column | Description   |
| ------ | ------------- |
| price  | Diamond price |

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-Learn
- Jupyter Notebook

---

## 📊 Exploratory Data Analysis (EDA)

The dataset was analyzed to understand:

- Dataset shape
- Missing values
- Duplicate records
- Statistical summary of numerical features
- Price distribution

Basic exploratory analysis was performed before model building.

---

## ⚙️ Data Preprocessing

The following preprocessing steps were applied:

### Numerical Features

- StandardScaler

### Categorical Features

- OneHotEncoder

### Why Scaling?

KNN is a distance-based algorithm. Feature scaling ensures that features with larger values do not dominate distance calculations.

---

## 🔄 Machine Learning Pipeline

A Scikit-Learn Pipeline was used to combine preprocessing and model training into a single workflow.

Pipeline Components:

1. ColumnTransformer
2. StandardScaler
3. OneHotEncoder
4. KNN Regressor

Benefits:

- Cleaner code
- Prevents data leakage
- Simplifies model deployment

---

## 🎛️ Hyperparameter Tuning

GridSearchCV was used to identify the best model configuration.

### Parameters Tuned

```python
{
    'model__n_neighbors': [3,5,7,9],
    'model__metric': ['euclidean','manhattan']
}
```

### Best Parameters

```python
{
    'model__metric': 'manhattan',
    'model__n_neighbors': 5
}
```

---

## 📈 Model Evaluation

The model was evaluated using:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

### Results

| Metric   | Score  |
| -------- | ------ |
| Train R² | 0.9798 |
| Test R²  | 0.9683 |
| MAE      | 358.89 |
| RMSE     | 709.43 |

---

## 📉 Visualizations

The notebook includes visualizations such as:

- Price Distribution Analysis
- Actual vs Predicted Price Comparison

These visualizations help assess data distribution and model performance.

---

## 🚀 How to Run the Project

### Clone the Repository

```bash
git clone https://github.com/Hallada-Manoj/diamonds-price-prediction-knn.git
```

### Navigate to Project Folder

```bash
cd diamonds-price-prediction-knn
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Notebook

Open:

```text
diamonds_price_prediction_knn.ipynb
```

using Jupyter Notebook or Google Colab.

---

## 📁 Project Structure

```text
diamonds-price-prediction-knn/
│
├── diamonds_price_prediction_knn.ipynb
├── diamonds.csv
├── README.md
└── requirements.txt
```

---

## 🔮 Future Improvements

- Compare KNN with Linear Regression
- Compare KNN with Random Forest Regressor
- Implement advanced feature engineering
- Deploy the model using Streamlit or Flask
- Experiment with additional hyperparameters

---

## 🏆 Conclusion

The KNN Regression model successfully predicts diamond prices based on diamond characteristics.

Key achievements:

- Effective preprocessing using ColumnTransformer
- Automated workflow using Pipeline
- Hyperparameter optimization using GridSearchCV
- Strong predictive performance with Test R² of 0.9683

This project demonstrates a complete machine learning workflow from data preprocessing to model evaluation.

---

## 👨‍💻 Author

**Hallada Manoj**

Aspiring Data Analyst | Machine Learning Enthusiast

Skills:

- Python
- SQL
- Power BI
- Machine Learning
- Data Analysis

---
