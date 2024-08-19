# Time Series-Based Energy Forecasting using LightGBM

Project Overview
-
This Jupyter Notebook provides an end-to-end pipeline for forecasting energy consumption using time series data. The project leverages LightGBM, a gradient boosting framework, to build an accurate and efficient forecasting model. The notebook includes data loading, preprocessing, feature engineering, model training, evaluation, and visualization.

Accurate energy consumption forecasting is essential for power grid management, energy trading, and optimizing resource allocation. This notebook demonstrates how to apply LightGBM for time series forecasting, focusing on energy consumption data. The project includes steps for data exploration, feature creation, and model evaluation to ensure reliable predictions.

Requirements
-
Before running the notebook, ensure you have the following Python packages installed:

- pandas
- numpy
- matplotlib
- seaborn
- xgboost
- sklearn
- jupyter

Install the required packages using the following command:

`bash
Copy code
pip install pandas numpy matplotlib seaborn xgboost scikit-learn jupyter`

Dataset
-
The dataset used in this project is the AEP Hourly Energy Consumption data, which contains hourly energy consumption values for a power plant. The dataset includes the following key columns:

Datetime: The timestamp of the recorded energy consumption.
AEP_MW: The energy consumption in megawatts (MW).
The dataset is loaded from a CSV file and is indexed by the Datetime column.

**Notebook Structure**
The notebook is organized into the following sections:

- Data Loading and Exploration: Load the dataset and perform an initial exploration to understand the structure and characteristics of the data.
- Data Preprocessing: Convert the Datetime column to a datetime format and set it as the index.
- Feature Engineering: Create additional features such as hour of the day, day of the week, month, year, and day of the year to enhance the model's predictive power.
- Data Visualization: Plot the data to visualize trends, seasonality, and daily patterns in energy consumption.
- Modeling: Train a LightGBM model using the engineered features, and evaluate its performance on a test set.
- Evaluation: Assess the model's accuracy using the Root Mean Squared Error (RMSE) and visualize the predictions against the actual values.
- Results and Analysis: Analyze the forecasting results and identify best and worst predicted days.
- Feature Engineering: Feature engineering is crucial for capturing temporal patterns in time series data. 

In this notebook, the following features are created:

Hour: The hour of the day (0-23).<br>
Day of the Week: The day of the week (0 = Monday, 6 = Sunday).<br>
Month: The month of the year (1-12).<br>
Year: The year extracted from the datetime.<br>
Day of the Year: The day of the year (1-365/366).<br>
These features help the model understand temporal cycles, such as daily and weekly patterns.

**Modeling**
The notebook uses the following modeling steps:

Train/Test Split: The data is split into training and testing sets based on a specific date (01-01-2015).<br>
Model Training: A LightGBM model is trained using the training data. The model's hyperparameters are tuned for better performance.<br>
Prediction: The model predicts energy consumption on the test set.<br>
Feature Importance: The importance of each feature is visualized to understand their contribution to the model.<br>
Evaluation: The model's performance is evaluated using the RMSE metric, which measures the difference between predicted and actual values. Additionally, the notebook includes visualizations to compare the predictions with the actual energy consumption data over time.<br>
