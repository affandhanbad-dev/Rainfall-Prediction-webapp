# Rainfall-Prediction-webapp

# 📌 Rainfall Prediction using Random Forest

This project aims to predict whether rainfall will occur based on multiple meteorological features such as temperature, humidity, pressure, dew point, cloud cover, sunshine hours, wind direction, and wind speed.

A Random Forest Classifier is trained and optimized using GridSearchCV to improve prediction accuracy.



# 📂 Dataset Overview
The dataset used is Rainfall.csv containing 366 daily observations with the following columns:

Feature	Description
pressure	Atmospheric pressure
maxtemp	Maximum temperature of the day
temparature	Average temperature
mintemp	Minimum temperature
dewpoint	Dew point level
humidity	Humidity percentage
cloud	Cloud coverage
rainfall	Target variable (Yes/No → Converted to 1/0)
sunshine	Hours of sunshine
winddirection	Direction of wind (degrees)
windspeed	Wind speed (km/h)
🧹 Data Pre-processing Steps

✅ Removed unnecessary features (day, maxtemp, temparature, mintemp)
✅ Null values handled using median/mode
✅ Converted rainfall labels:

yes → 1  
no  → 0


✅ Used downsampling to handle class imbalance
✅ Data visualization with:

Histograms using histplot

Correlation Heatmap

Box plots for outlier study


# 🤖 Machine Learning Model
Model Used:
🔹 Random Forest Classifier

✅ Hyperparameter tuning with GridSearchCV
✅ Train-test split: 80% training / 20% testing
✅ Model performance measured using:

Accuracy

Confusion Matrix

Classification Report

# 🛠 Libraries Required
numpy
pandas
matplotlib
seaborn
scikit-learn
pickle

# 📈 Model Optimization Grid

The grid search tested different values for:

param_grid = {
    'n_estimators': [50, 100, 200],
    'max_depth': [None, 10, 20],
    'min_samples_split': [2, 5, 10],
    'min_samples_leaf': [1, 2, 4],
    'max_features': ['sqrt', 'log2']
}


⛔ Note: 'auto' parameter was removed since it's deprecated in newer sklearn versions.

# ✅ Final Output

The best model from GridSearchCV is used to:

✔ Predict rainfall
✔ Evaluate performance
✔ Save model using pickle (optional extension)

# 📌 Project Structure
📁 Rainfall_Prediction
│── Rainfall.csv
│── model.pkl  (optional if exported)
│── README.md
└── rainfall_model.ipynb / .py (your code file)
