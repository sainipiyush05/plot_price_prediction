# Plot_price_prediction

House Price Prediction Model
This project predicts house prices based on key features like BHK (Bedrooms, Hall, Kitchen), bathrooms, square footage, and location. Using real estate data from Bengaluru, the model incorporates extensive data cleaning, feature engineering, and machine learning techniques to deliver reliable predictions.

Table of Contents

Overview

Dataset

Data Preprocessing

Features

Model Training

Usage

Dependencies

Overview

The House Price Prediction Model analyzes property data and provides price estimates based on key inputs. The model uses Linear Regression for its predictions and is trained on a dataset containing various attributes of properties in Bengaluru.

Dataset

The dataset used contains information about:

Area type (e.g., Super Built-Up Area)

Size (e.g., 2 BHK, 3 BHK)

Total square footage

Price

Location

Data source: [Bengaluru Housing Dataset].

Data Preprocessing

Handling Missing Values
Removed rows with missing data in key fields.

Feature Engineering

Extracted numeric values for BHK from text.
Converted non-numeric ranges (e.g., 2100-2850 sqft) into average values.
Added a price_per_sqft feature for better outlier detection.
Dimensionality Reduction
Locations with fewer than 10 entries were grouped under the category "other".

Outlier Removal

Removed unrealistic entries where total_sqft/BHK < 300.
Eliminated properties with excessive bathrooms (bathrooms > BHK + 2).
One-Hot Encoding
Encoded location data to make it suitable for machine learning models.

Features

The final dataset includes:

BHK: Number of bedrooms, halls, and kitchens.
Bath: Number of bathrooms.
Total Square Footage.
Location: One-hot encoded categorical feature.
Price: Target variable (in lakhs).
Model Training
The model is trained using:

Linear Regression as the primary algorithm.

GridSearchCV for hyperparameter tuning and evaluating alternative models like:
Lasso Regression
Decision Tree Regressor
The trained model is serialized as a .pickle file for deployment.

Dependencies

Python 3.x

Libraries:

pandas

numpy

scikit-learn

matplotlib

pickle

json
