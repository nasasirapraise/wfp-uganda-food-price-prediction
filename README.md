 Uganda Food Price Prediction Using Machine Learning

 Project Overview

This project uses machine learning to predict food prices in Uganda using historical food price data from the World Food Programme (WFP).

The project explores historical food price patterns, identifies important factors associated with food prices, and develops predictive models that can support food price analysis and decision-making.

Problem Statement

Food prices in Uganda vary across commodities, locations, markets, and time. Accurately estimating food prices can therefore be challenging.

This project investigates whether machine learning can be used to predict food prices using historical market and commodity information.

Objectives

The main objective is to develop a machine learning model for predicting food prices in Uganda.

Specific objectives are to:
- Analyze historical food price patterns.
- Identify factors associated with food prices.
- Prepare and transform the dataset for machine learning.
- Develop and compare machine learning models.
- Evaluate model performance using appropriate regression metrics.
- Identify the best-performing model.

Dataset

The dataset used in this project is the Uganda Food Prices dataset from the World Food Programme (WFP).

Original Dataset

- Country: Uganda
- Observations: 30,933
- Features: 16
- Target variable: Price

Important variables include:

- Date
- Admin1
- Admin2
- Market
- Latitude
- Longitude
- Category
- Commodity
- Unit
- Pricetype
- Price

After data cleaning and feature preparation, the final modelling dataset contained 23,384 observations and 11 input features before categorical encoding.

 Data Preparation

The dataset was prepared for machine learning through the following steps:

- Examining the dataset structure and data types
- Checking missing values and duplicate records
- Cleaning the dataset
- Creating year and month features from the date
- Encoding categorical variables
- Selecting relevant features
- Splitting the data into training and testing sets

 Exploratory Data Analysis

The exploratory analysis examined food price distributions, commodity prices, food categories, geographical variables, and price trends over time.

Key Findings

- - Food prices were positively skewed, with most observations concentrated at lower price levels and some high-value observations.
- Fish (dry) and vegetable oil were among the higher-priced commodities.
- Cassava (fresh) was among the lower-priced commodities.
- Meat, Fish & Eggs recorded relatively higher average prices.
- Average food prices generally increased over time, with some periods of fluctuation.
- The relationship between geographical coordinates and price was relatively weak.
- Commodity type, food category, time, and market-related characteristics  appeared to be important factors for food price prediction.

 Machine Learning Models

The project used two regression models:

 Random Forest Regressor

Random Forest is a classical machine learning algorithm that combines multiple decision trees to make predictions and can capture nonlinear relationships between variables.

 Neural Network

A Neural Network was also developed to learn complex relationships between the input features and food prices.

Model Evaluation

The models were evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R-squared (R²)

 Results

| Model         | MAE  | RMSE  | R²    |
|---            |-     | ---:  |---:  |
| Random Forest |335.20|1242.19|90.74%|
| Neural Network|702.64|1513.58|86.25%|

Best-Performing Model

The Random Forest model performed better than the Neural Network across all three-evaluation metrics.

It achieved:

- MAE: 335.20
- RMSE: 1242.19
- R²: 90.74%

Therefore, Random Forest was selected as the best-performing model for this project.

Accessing the Demo

The working prediction interface is available in the Jupyter Notebook included in this repository.

Open `Uganda_Food_Price_Prediction_ML.ipynb` and run the demo/interface cells to interact with the food price prediction model.
The interface allows users to provide information such as:

- Administrative region
- Market
- Commodity
- Category
- Unit
- Price type
- Year
- Month
- Latitude and longitude

The model then generates a predicted food price.

Key Insights

The project demonstrates that machine learning can be used to predict food prices using historical market and commodity information.

The results also show that commodity type, food category, time, and market-related characteristics can contribute to food price prediction.

Recommendations

- Predictive analytics can support food security planning and decision-making.
- Farmers and traders can benefit from improved food price information.
- Food security organizations can use predictive models to monitor potential price changes.
- Future models should incorporate additional factors such as weather conditions, inflation, fuel prices, seasonal production, and supply conditions.
- The model should be updated regularly as new food price data becomes available.

Future Improvements

Future work could improve prediction performance by incorporating additional factors such as:

- Weather conditions
- Inflation
- Fuel prices
- Seasonal production
- Supply conditions
- Transportation costs
- Economic indicators

Integrating these additional factors may provide a more comprehensive representation of the drivers of food prices in Uganda.

Conclusion

This project demonstrates the potential of machine learning for food price prediction in Uganda.

The Random Forest model was the best-performing model, achieving an R² of 90.74%, MAE of 335.20, and RMSE of 1242.19.

The project provides a foundation for using machine learning to support food price analysis, prediction, and decision-making.
