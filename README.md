# 🏠 House Price Prediction Using Linear Regression

## 📌 Project Overview

This project focuses on predicting house prices using **Machine Learning**, specifically the **Linear Regression** algorithm.

The model learns the relationship between different characteristics of a house and its price. The main features used for prediction are:

* **Area of the house (sqft)**
* **Number of bedrooms**
* **Age of the house (years)**
* **Distance from the city (km)**

The target variable is the **House Price in Lakhs**.

This project demonstrates a complete basic machine learning workflow, including data loading, data exploration, feature selection, train-test splitting, model training, prediction, and model evaluation.

---

## 🎯 Objectives

The main objectives of this project are:

1. Load and explore the house price dataset.
2. Understand the structure of the dataset.
3. Select relevant features for prediction.
4. Split the dataset into training and testing sets.
5. Train a Linear Regression model.
6. Predict house prices using the trained model.
7. Compare actual and predicted prices.
8. Evaluate model performance using regression metrics.

---

## 📊 Dataset

The dataset contains information about houses and their prices.

### Features

| Feature            | Description                                       |
| ------------------ | ------------------------------------------------- |
| `Area_sqft`        | Area of the house in square feet                  |
| `Bedrooms`         | Number of bedrooms                                |
| `Age_years`        | Age of the house in years                         |
| `Distance_City_km` | Distance of the house from the city in kilometers |

### Target Variable

| Variable            | Description                 |
| ------------------- | --------------------------- |
| `House_Price_Lakhs` | Price of the house in lakhs |

The dataset contains approximately **160 records** and **6 columns**.

---

## 🧠 Machine Learning Algorithm

### Linear Regression

Linear Regression is a supervised machine learning algorithm used to predict a continuous numerical value.

In this project, Linear Regression is used to estimate house prices based on the selected input features.

The general form of the model is:

**House Price = Intercept + (Coefficient × Feature₁) + (Coefficient × Feature₂) + ...**

The model determines the coefficients during training and uses them to make predictions for unseen data.

---

## 🛠️ Technologies Used

The following Python libraries are used in this project:

* **Python**
* **Pandas** — for data manipulation and analysis
* **NumPy** — for numerical operations
* **Matplotlib** — for data visualization
* **Scikit-learn** — for machine learning and model evaluation
* **Jupyter Notebook** — for development and experimentation

---

## 📦 Installation

Make sure Python is installed on your computer.

Install the required libraries using:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

---

## 🚀 How to Run the Project

### Step 1: Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Step 2: Open the project folder

```bash
cd YOUR_REPOSITORY_NAME
```

### Step 3: Start Jupyter Notebook

```bash
jupyter notebook
```

### Step 4: Open the notebook

Open:

```text
Untitled2.ipynb
```

Then run the notebook cells from top to bottom.

---

## 🔄 Project Workflow

The project follows these steps:

```text
Dataset
   ↓
Data Loading
   ↓
Data Exploration
   ↓
Feature Selection
   ↓
Train-Test Split
   ↓
Linear Regression Model
   ↓
Model Training
   ↓
Price Prediction
   ↓
Model Evaluation
```

---

## 🔍 Data Loading and Exploration

The project uses Pandas to load the dataset and inspect its structure.

The dataset is explored using operations such as:

* Viewing the first few rows
* Checking the dataset shape
* Checking data types
* Understanding the available columns

This helps ensure that the data is suitable for machine learning.

---

## 🧮 Feature Selection

The following features are selected as input variables:

```python
X = df[["Area_sqft", "Bedrooms", "Age_years", "Distance_City_km"]]
```

The target variable is:

```python
y = df["House_Price_Lakhs"]
```

Therefore:

**Input (X):**

* Area_sqft
* Bedrooms
* Age_years
* Distance_City_km

**Output (y):**

* House_Price_Lakhs

---

## ✂️ Train-Test Split

The dataset is divided into training and testing data.

The project uses:

* **80%** of the data for training
* **20%** of the data for testing

The split uses `random_state=42` to make the results reproducible.

```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.20, random_state=42
)
```

---

## 🤖 Model Training

A Linear Regression model is created using Scikit-learn:

```python
model = LinearRegression()
model.fit(X_train, y_train)
```

The model learns how the selected house features are related to the house price.

---

## 📈 Predictions

After training, the model predicts prices for the test dataset:

```python
y_pred = model.predict(X_test)
```

The project also compares the actual house prices with the predicted prices.

This allows us to understand how accurately the model is predicting house prices.

---

## 📏 Model Evaluation

The model performance is evaluated using regression metrics such as:

### Mean Squared Error (MSE)

Mean Squared Error measures the average squared difference between actual and predicted values.

A lower MSE generally indicates better prediction performance.

### R² Score

The R² score measures how well the model explains the variation in the target variable.

An R² score closer to **1** generally indicates a better fit.

---

## 📋 Model Coefficients

The project also examines the coefficients learned by the Linear Regression model.

The coefficients help understand how each feature contributes to the predicted house price while keeping the other features fixed.

For example:

* A positive coefficient indicates that an increase in the feature is associated with an increase in predicted price.
* A negative coefficient indicates that an increase in the feature is associated with a decrease in predicted price.

The actual effect should be interpreted using the model's calculated coefficients and the scale of each feature.

---

## 📁 Project Structure

A recommended repository structure is:

```text
House-Price-Prediction/
│
├── README.md
├── Untitled2.ipynb
└── dataset.csv
```

If you later add Python scripts, you could organize it as:

```text
House-Price-Prediction/
│
├── README.md
├── requirements.txt
├── Untitled2.ipynb
├── dataset/
│   └── house_prices.csv
│
└── src/
    └── house_price_prediction.py
```

---

## 💡 Key Learnings

Through this project, the following machine learning concepts are demonstrated:

* Loading datasets using Pandas
* Exploring and understanding data
* Selecting features and target variables
* Splitting data into training and testing sets
* Building a Linear Regression model
* Training a machine learning model
* Making predictions
* Understanding model coefficients
* Evaluating regression models
* Comparing actual and predicted values

---

## ⚠️ Limitations

This project is a basic machine learning demonstration and has some limitations:

* The dataset is relatively small.
* Only a limited number of features are used.
* Linear Regression assumes a linear relationship between the features and target.
* Real-world house prices can depend on many additional factors.
* The model may not perform equally well on data from different locations or markets.

---

## 🔮 Future Improvements

The project can be improved by:

1. Using a larger and more diverse dataset.
2. Adding more features such as:

   * Location
   * Bathrooms
   * Parking spaces
   * Property type
   * Neighborhood
   * Floor number
3. Performing detailed exploratory data analysis.
4. Adding data visualizations.
5. Handling missing values and outliers.
6. Comparing multiple machine learning algorithms.
7. Performing cross-validation.
8. Hyperparameter tuning for suitable models.
9. Creating a user interface for price prediction.
10. Deploying the model as a web application.

---

## 📌 Conclusion

This project demonstrates how **Linear Regression** can be used to predict house prices from property-related features.

It provides a simple introduction to the machine learning workflow, starting from data exploration and feature selection and continuing through model training, prediction, and evaluation.

Although the project is designed as a learning exercise, the same fundamental workflow can be extended to larger datasets and more advanced machine learning models for improved prediction performance.

---

## 👨‍💻 Author

**Abhay Chandel**

This project was created as a machine learning project to practice data analysis, regression, and predictive modeling using Python and Scikit-learn.

---

## ⭐ Acknowledgement

This project was developed for learning and demonstrating fundamental concepts of **Machine Learning, Python, Data Analysis, and Linear Regression**.

If you find this project useful, consider giving the repository a ⭐ on GitHub.
