# BoomBikes-ML-Regression

## General Information
This project aims to build a multiple linear regression model to predict the demand for shared bikes in the American market. The dataset provided by BoomBikes contains daily records of bike rentals, including various features like season, weather conditions, temperature, humidity, and more, that could influence bike demand. The goal is to understand which factors significantly impact bike demand, allowing the company to optimize its operations and improve profitability after the COVID-19 lockdown.

## Business Problem
Due to the COVID-19 pandemic, BoomBikes, a US-based bike-sharing provider, has experienced a significant decline in revenue. To address this challenge, the company seeks to develop a business strategy based on a predictive model that forecasts bike demand once the lockdown restrictions are lifted. Understanding the demand dynamics will help BoomBikes prepare effectively for post-lockdown operations.

## Dataset
The dataset used in this project is sourced from BoomBikes and includes the following features:
- `instant`: Record index
- `dteday`: Date
- `season`: Season (1: Spring, 2: Summer, 3: Fall, 4: Winter)
- `yr`: Year (0: 2018, 1: 2019)
- `mnth`: Month (1 to 12)
- `holiday`: Whether the day is a holiday (1: Yes, 0: No)
- `weekday`: Day of the week (0 to 6)
- `workingday`: Whether the day is neither a weekend nor a holiday (1: Yes, 0: No)
- `weathersit`: Weather situation (1: Clear, 2: Mist + Cloudy, 3: Light Snow/Rain, 4: Heavy Rain/Snow)
- `temp`: Normalized temperature in Celsius
- `atemp`: Normalized feeling temperature in Celsius
- `hum`: Normalized humidity
- `windspeed`: Normalized wind speed
- `casual`: Count of casual users
- `registered`: Count of registered users
- `cnt`: Count of total bike rentals (target variable)

## Data Preparation
- Converted categorical features (`season`, `weathersit`, `mnth`, `weekday`) to dummy variables to handle them properly in the regression model.
- Retained the `yr` variable as it shows an increasing trend in bike demand from 2018 to 2019.
- Performed scaling for numerical variables to standardize them, ensuring consistent contribution to the model.

## Model Building
- Built a multiple linear regression model using the scikit-learn library.
- Split the dataset into training and test sets (80% training and 20% testing).
- Trained the model using the training data and evaluated it using the test data.

## Model Evaluation
- The model was evaluated using the R-squared metric, which measures the proportion of variance in the dependent variable that is predictable from the independent variables.
- Performed residual analysis to validate the assumptions of linear regression, such as linearity, normality of residuals, and homoscedasticity.

## Key Findings
- **Temperature (`temp`)**: Strong positive correlation with bike demand, indicating higher rentals in warmer weather.
- **Year (`yr`)**: Significant growth in demand from 2018 to 2019.
- **Season (`season_summer` and `season_fall`)**: Higher bike demand during summer and fall seasons.
- **Weather Situation (`weathersit`)**: Clear weather positively impacts bike demand, while adverse weather conditions reduce rentals.

## Conclusions
- The model indicates that temperature, year, and season are significant factors influencing bike demand.
- Weather conditions also play a critical role in determining rental activity.
- These insights will help BoomBikes optimize their bike inventory, pricing strategies, and marketing efforts based on predicted demand patterns.

## Technologies Used
- Python 3.8
- pandas 1.2.4
- scikit-learn 0.24.2
- matplotlib 3.3.4
- seaborn 0.11.1
- numpy 1.19.5

## Acknowledgements
- The dataset used in this project is credited to BoomBikes and "Event labeling combining ensemble detectors and background knowledge" by Fanaee-T, Hadi, and Gama, Joao (2013). The dataset is available for use under the associated publication's license.
- Special thanks to BoomBikes for providing the data and supporting this research.

## Contact
Created by [Pushkar Mishra] - [p2k3m_2002@yahoo.com]

Feel free to reach out for any questions or collaboration!

A data science project to build a multiple linear regression model for predicting bike rental demand for BoomBikes, a US-based bike-sharing service. The project analyzes various factors affecting bike demand, such as weather, season, temperature, and other variables, to help the company optimize its business strategy post-COVID-19 lockdown.
