AI-Based Food Demand Forecasting System to Reduce Food Waste
Project Overview

Food waste is a major issue in the hospitality and food service industry. One of the main causes of food waste is over-preparation, which happens when more food is produced than customers actually order. This project explores how machine learning can be used to predict food demand and help kitchens prepare a more accurate number of meals.

The goal of this project is to build a predictive model that forecasts the number of food orders based on historical data. By improving demand estimation, food service providers can reduce unnecessary waste while still meeting customer demand.

Objective

The objective of this project is to develop a machine learning model that predicts weekly food demand. The model analyzes historical order data along with factors such as pricing, promotions, and meal categories. Based on the prediction, the system provides a recommended preparation quantity that helps reduce overproduction.

Dataset

The project uses a food demand forecasting dataset that includes three main data files:

train.csv – historical order data

meal_info.csv – information about meal categories and cuisines

center_info.csv – information about fulfillment centers

The dataset contains several important variables including:

week (time index)

center_id (fulfillment center location)

meal_id (meal identifier)

checkout_price (final selling price)

base_price (original price)

emailer_for_promotion (promotion indicator)

homepage_featured (homepage promotion indicator)

num_orders (target variable representing total orders)

Methodology

The project follows a typical machine learning workflow.

First, the datasets are merged and cleaned to create a single structured dataset. Categorical variables such as cuisine and category are converted using one-hot encoding so that they can be used by the machine learning model.

The dataset is then divided into training and testing sets using an 80/20 split.

A Random Forest Regressor model is used to predict food demand. Random Forest is an ensemble learning method that combines multiple decision trees to produce more accurate and stable predictions.

After generating the prediction, a preparation coefficient of 0.95 is applied to slightly reduce the predicted quantity. This strategy helps reduce food waste while still preparing enough food to meet expected demand.

Model Evaluation

The performance of the model is evaluated using two common regression metrics:

RMSE (Root Mean Squared Error): 28.45
R² Score: 0.88

The R² score indicates that the model explains approximately 88% of the variation in food demand, which suggests that the model performs well on this dataset.

Example Output

Example prediction from the system:

Predicted demand: 236 portions
Preparation coefficient: 0.95
Recommended preparation: 224 portions

This recommendation helps kitchen managers prepare food more efficiently and reduce the number of unused meals.

Technologies Used

Python

Jupyter Notebook

Pandas

NumPy

Scikit-learn

Matplotlib

Future Improvements

There are several ways this project could be improved in the future. Possible improvements include adding weather data, implementing real-time demand prediction, and exploring deep learning models such as LSTM for time-series forecasting.

Conclusion

This project demonstrates how machine learning can be applied to reduce food waste in food service operations. By using historical data to forecast demand, kitchens can make more informed preparation decisions, reduce unnecessary waste, and improve operational efficiency.