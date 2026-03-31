# Real Estate Buying Decision Prediction

A predictive analytics project focused on understanding and classifying home buying decisions using real estate transaction data, data preprocessing, feature engineering, and machine learning models.

## Project Overview

This project explores how predictive analytics can be used to support decision-making in the real estate market by predicting whether a property is likely to be purchased. The analysis is based on structured housing data containing property characteristics such as size, location, availability, pricing, energy rating, and renovation requirements.

The project places strong emphasis on data cleaning and preprocessing, including missing-value treatment, outlier handling, standardization, and feature engineering, before applying predictive models. Multiple classification techniques were compared to identify the most effective approach for predicting buying behaviour.

## Objective

The primary objective of this project was to prepare a real estate dataset for predictive modelling and build classification models that predict the binary target variable **buying_status**.

The project also aimed to:
- improve data quality through cleaning and preprocessing
- engineer meaningful features to enhance model performance
- compare multiple machine learning models
- identify the most influential factors driving buying decisions

## Dataset Overview

The dataset contains housing-related information such as:

- property scope
- availability
- location
- bhk / bedrooms
- total square footage
- bathrooms
- balcony
- price per square foot
- energy rating
- renovation needed
- buying status

### Initial dataset profile
- **13,320 rows**
- **12 columns**

The dataset included both numerical and categorical attributes, along with missing values and outliers that required preprocessing before modelling. :contentReference[oaicite:1]{index=1}

## Data Preparation and Preprocessing

A substantial part of the project focused on preparing the dataset for predictive analysis.

### Key preprocessing steps
- renamed columns for readability and consistency
- reviewed dataset structure, unique values, and summary statistics
- checked and handled missing values
- standardized mixed-format columns such as `bhk` and `total_sqft`
- converted categorical fields into numeric form
- rounded and formatted price-related columns
- removed the `ID` column as redundant
- identified and removed outliers using the IQR method
- saved the cleaned dataset for downstream modelling

Missing values were handled using suitable strategies such as filling with zero in selected fields and applying other context-aware cleaning choices depending on the variable. Outliers were removed to reduce distortion in modelling results and improve predictive reliability. :contentReference[oaicite:2]{index=2}

## Exploratory Data Analysis

Initial exploratory analysis was carried out to understand:
- distributions of numerical variables
- category frequencies
- missing-value patterns
- price variation
- potential outliers
- relationships between important real estate attributes

Histograms, bar plots, scatter plots, and summary statistics were used to examine the dataset and guide the cleaning process. This phase helped reveal skewness in numerical features and highlighted the need for preprocessing transformations before modelling. :contentReference[oaicite:3]{index=3}

## Feature Engineering

To improve model performance and analytical value, several new features were created:

- **bath_to_bed_ratio**  
  Captures the relationship between bathrooms and bedrooms.

- **area_to_bedroom_ratio**  
  Measures how much space is allocated per bedroom.

- **total_price**  
  Derived from `price_per_sqft × total_sqft`.

These engineered variables were designed to better reflect layout efficiency, property value, and practical buyer considerations. :contentReference[oaicite:4]{index=4}

## Models Used

The project compared four classification models for predicting **buying_status**:

- Logistic Regression
- Random Forest
- K-Nearest Neighbours (KNN)
- Decision Tree

These models were evaluated using:
- accuracy
- AUC
- precision
- recall
- confusion matrix analysis

## Model Performance Summary

### Logistic Regression
- Accuracy: **71.56%**
- Served as a strong and interpretable baseline
- Performed well on non-buyers but struggled more with identifying buyers

### Random Forest
- Accuracy: **72.38%**
- Better at capturing non-linear relationships
- Provided stronger and more balanced classification performance

### K-Nearest Neighbours (KNN)
- Accuracy: **67.83%**
- AUC: **0.68**
- Less effective due to sensitivity to noise and overlapping class boundaries

### Decision Tree
- Accuracy: **64.24%**
- AUC: **0.81**
- Easy to interpret, but prone to overfitting

### Tuned Random Forest
After hyperparameter tuning, the Random Forest model achieved:

- Accuracy: **75.63%**
- AUC: **0.93**

This made it the best-performing model in the project. :contentReference[oaicite:5]{index=5}

## Key Predictors

Feature importance analysis showed that the most influential variables included:

- `price_per_sqft`
- `total_sqft`
- `area_to_bedroom_ratio`
- `bath_to_bed_ratio`
- `energy_rating`
- `availability`
- `renovation_needed`
- `location`

These findings suggest that buyers are influenced not only by price and size, but also by layout efficiency, sustainability, readiness, and condition of the property. :contentReference[oaicite:6]{index=6}

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
- outlier detection and treatment
- missing-value handling
- feature engineering
- exploratory data analysis
- classification modelling
- model comparison and tuning
- interpretation of real estate analytics


## License

This project is intended for academic and portfolio use unless otherwise stated.
