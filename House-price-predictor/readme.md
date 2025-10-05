🏠 House Price Prediction Project: Optimized XGBoost Model
This document summarizes the end-to-end development of a highly optimized machine learning model for predicting house prices. This project showcases proficiency in advanced data science techniques, model optimization, and building a reproducible workflow.

Project Objective
The goal was to build a robust and highly accurate regression model using the XGBoost algorithm, demonstrating a significant improvement over a simple baseline model.

Final Results & Performance
The final model achieved a strong predictive score for real-world housing data, proving the success of the feature engineering and tuning process.

Initial Baseline Model (Linear Regression): R² Score ≈ 0.65

Final Optimized Model (Tuned XGBoost): R² Score ≈ 0.67

This 2% gain represents a significant reduction in prediction error achieved through professional model tuning and feature selection.

🛠️ Key Techniques Implemented
1. Professional Pipeline and Reproducibility
Pipeline (sklearn.pipeline): The entire workflow—from data cleaning to the final model—is contained within a single Pipeline object.

ColumnTransformer: Used to apply different preprocessing steps simultaneously to different data types:

Numerical Features: Handled missing values (SimpleImputer) and scaled using StandardScaler.

Categorical Features: Encoded using OneHotEncoder.

Reproducibility: Used a random_state in the training and search steps to ensure consistent results on every run.

2. Feature Engineering and Selection
This phase was critical for moving past the R² barrier of 0.65.

Feature Creation: Derived highly predictive features from raw inputs:

TotalRooms: Sum of bedrooms and bathrooms.

rooms_per_bedroom: Ratio calculated to measure house balance and space utilization.

Multicollinearity Resolution: The original, redundant bedrooms and bathrooms features were removed to prevent the model from being confused by highly correlated inputs.

Target Transformation: The highly skewed target variable (price) was transformed using the logarithmic function (np.log1p) to normalize its distribution, which is essential for maximizing the performance of most ML algorithms.

3. Advanced Model Tuning
Model Choice: XGBoost (XGBRegressor) was selected for its superior ability to handle the non-linear feature interactions common in house pricing data.

Efficient Tuning: RandomizedSearchCV was implemented to efficiently sample 50 combinations of complex hyperparameters (n_estimators, max_depth, learning_rate, etc.). This approach found the optimal model settings much faster than a full grid search.

⚙️ How to Run the Project
The entire solution is contained within the main Python script.

Dependencies: Install the necessary libraries using the following command:

pip install pandas numpy scikit-learn xgboost

Execution: Run the main script from your terminal:

python your_script_name.py

The script will load the data, run the full tuning process, and print the final evaluation metrics and best-performing parameters