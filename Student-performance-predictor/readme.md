# **Student Performance Predictor (Linear Regression)**

## **Project Overview**

This project develops a linear regression model to predict a student's **Overall Cumulative Grade Point Average (CGPA)** based on a diverse set of academic, behavioral, and demographic features.

The key objective was to demonstrate the impact of **Feature Selection** and **Data Encoding** on model accuracy, specifically showcasing the transformation from an ineffective single-feature model to a highly predictive multi-feature model.

## **Initial Problem Statement & Solution**

### **Initial Approach (Single Feature)**

The model was first trained using only **Preparation** hours as the feature.

* **Result (R-squared)**: ≈0.003  
* **Conclusion**: The model was ineffective, proving that a student's overall performance is not linearly dependent on a single factor.

### **Improved Approach (Multi-Feature Success)**

To achieve a high-performance model, the feature set (X) was expanded to include critical, highly correlated variables such as HSC, SSC, Last semester performance, and behavioral factors (Attendance, Gaming).

* **Result (R-squared)**: ≈0.89  
* **Conclusion**: The significant increase in the R2 score demonstrates that by providing the model with a richer context, its predictive power improved dramatically, successfully modeling **89%** of the variance in the student's CGPA.

## **Final Model Performance**

The following metrics were achieved by the final Linear Regression model, trained using a multi-feature set:

| Metric | Value | Interpretation |
| :---- | :---- | :---- |
| **R-squared (**R2**) Score** | **0.8914** | The model explains 89.14% of the variability in the Overall CGPA. (Excellent fit) |
| **Mean Absolute Error (MAE)** | 0.1448 | The model's average prediction error is only 0.14 CGPA points. |
| **Root Mean Squared Error (RMSE)** | 0.2013 | Measures the overall spread of errors, indicating low volatility in predictions. |

## **Technical Implementation Details**

The solution is implemented entirely in Python using the standard scikit-learn stack, focusing on a clean, modular structure.

### **Key Techniques Used**

1. **Modular Code Design**: The entire workflow is split into clear functions (load\_data, pre\_process, build\_pipeline, evaluate) for high readability and easy maintenance.  
2. **Data Encoding**: All string-based categorical variables (Preparation, Gaming, Job, Extra, Attendance) were mapped to numerical values using custom Python dictionaries for feature engineering.  
3. **Scikit-learn Pipeline**: A Pipeline object was used to chain the preprocessing (handling missing values via SimpleImputer) and the model training (LinearRegression) into a single, reliable workflow. This prevents data leakage and ensures consistency.

### **Requirements**

To run this script, you need the following Python libraries:

pip install pandas numpy scikit-learn

**Note**: This script assumes the presence of a file named ResearchInformation3.csv in the same directory, containing the defined dataset attributes.