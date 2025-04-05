🏘️ Real Estate Price Prediction
This project performs Exploratory Data Analysis (EDA) and builds a machine learning model to predict the house price per unit area based on factors such as age, proximity to MRT stations, convenience stores, and geographic location.

📊 Description
Using a dataset of 414 real estate transactions in Taiwan, we:

Clean and explore the data

Visualize trends and correlations

Build and evaluate regression models

Tune and validate predictions using cross-validation

Export a trained model using joblib

🔍 Dataset Overview
Feature	Description
age	Age of the house (in years)
nearest_MRT_station_dist	Distance to the nearest MRT station (in meters)
no_convenience_stores	Number of nearby convenience stores
latitude, longitude	Geographical coordinates
unit_area_price	House price per unit area (target variable)
⚙️ Machine Learning Pipeline
Preprocessing:
Standardized numerical features using StandardScaler.

Models tried:

Linear Regression

Decision Tree Regressor

✅ Random Forest Regressor (Best Performer)

Validation:

Cross-validated using RMSE

Final test RMSE: ~7.35

Exported Model:

Trained model is saved as Price_prediction.joblib for reuse.

📈 Key Insights
Distance to MRT station is negatively correlated with price.

Number of convenience stores and location (lat/long) have a positive correlation.

Random Forest performed best with low training RMSE and acceptable generalization on the test set.

🧪 Technologies Used
Python 🐍

pandas, NumPy

scikit-learn

matplotlib, seaborn

joblib

🚀 How to Use
Clone the repo:

bash
Copy
Edit
git clone https://github.com/yourusername/real-estate-price-prediction.git
cd real-estate-price-prediction
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the notebook or Python script to train and evaluate the model.

Load the saved model:

python
Copy
Edit
from joblib import load
model = load('Price_prediction.joblib')
