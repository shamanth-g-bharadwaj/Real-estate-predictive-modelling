# Home Buying Decision Prediction

A predictive analytics project focused on understanding and classifying home buying decisions using real estate data, feature engineering, and machine learning models.

## Project Overview

This project explores how predictive analytics can be used to understand home buying behaviour in the real estate market. The main objective was to build classification models that predict whether a property is likely to be bought based on a range of property features and market-related variables.

The project combines data preparation, exploratory analysis, feature engineering, and predictive modelling to generate insights that could support real estate agencies, property platforms, and decision-makers in understanding buyer preferences more effectively.

## Objective

The aim of this project was to predict the binary outcome of **buying_status** using housing-related features such as price, square footage, number of rooms, energy rating, availability, and renovation requirement.

## Dataset

The analysis used the **Ireland House Price Final** dataset.

### Initial dataset profile
- **13,320 rows**
- **12 columns**
- Included property-related variables such as:
  - property scope
  - availability
  - location
  - bedrooms
  - total square footage
  - bathrooms
  - balconies
  - buying status
  - BER
  - renovation needed
  - price per square foot

After cleaning and preprocessing, the final dataset contained:
- **10,319 rows**
- **11 columns**

## Project Workflow

### 1. Data Preparation and Initial Exploration
The project began with:
- loading the housing dataset
- inspecting its structure and completeness
- renaming columns for readability and consistency
- checking unique values
- performing initial exploratory analysis before cleaning

This early phase helped identify missing values, skewed distributions, and outliers in key numerical variables.

### 2. Data Cleaning and Standardization
Several preprocessing steps were applied to improve data quality:

- removed non-analytical columns such as `id`
- standardized mixed-format columns like `bedrooms` and `total_sqft`
- converted categorical variables into numeric/ordinal format
- encoded `buying_status`, `BER`, and `renovation_needed`
- handled outliers using the IQR method
- treated missing values using contextual imputation
- ensured all fields were ready for modelling

### 3. Feature Engineering
To improve predictive power, new derived variables were created, including:

- **log_total_sqft**
- **log_price_per_sqft**
- **sqft_per_room**

These features helped reduce skewness, improve linearity, and better capture space efficiency in a property.

### 4. Exploratory and Analytical Insights
The analysis showed that:

- `total_sqft` and `price_per_sqft` had moderate positive skewness
- log transformations improved symmetry and made the variables more suitable for modelling
- property size showed positive relationships with price, bedrooms, and balconies
- location-specific scatter plots revealed different market dynamics across regions

### 5. Predictive Modelling
Two classification models were developed:

- **Logistic Regression**
- **Random Forest Classifier**

The target variable was **buying_status**, and the data was split into training and testing sets using an 80/20 split.

## Model Performance

### Logistic Regression
- Accuracy: **72.77%**

### Random Forest Classifier
- Initial Accuracy: **72.62%**
- Tuned Accuracy: **74.66%**

After hyperparameter tuning, the Random Forest model performed better and was selected as the stronger model for this project.

## Key Predictors

Feature importance analysis showed that the most influential variables were:

- `price_per_sqft`
- `log_price_per_sqft`
- `sqft_per_room`
- `total_sqft`
- `log_total_sqft`
- `BER`

These findings suggest that buyers are strongly influenced by:
- price
- property size
- space efficiency
- energy efficiency

## Tools Used

- **Python**
- **pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **scikit-learn**
- Jupyter Notebook

## Project Value

This project demonstrates practical skills in:

- data cleaning and preprocessing
- handling missing values and outliers
- feature engineering
- exploratory data analysis
- classification modelling
- model comparison and evaluation
- interpretation of predictive insights in a real estate context

## License

This project is intended for academic and portfolio use unless otherwise stated.
