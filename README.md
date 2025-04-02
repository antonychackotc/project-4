# project-4

# Employee Attrition Analysis

## Project Overview
This project analyzes employee attrition using machine learning techniques to identify key factors influencing employee turnover. The goal is to build a predictive model that helps organizations retain valuable employees by addressing potential attrition risks.

## Dataset
The dataset includes various employee attributes such as:
- Demographics (Age, Gender, Marital Status, etc.)
- Job-related factors (Department, Job Role, Years at Company, etc.)
- Compensation details (Salary, Bonus, etc.)
- Work-life balance indicators
- Performance metrics

## Approach
1. **Data Preprocessing**
   - Handled missing values using mean/median imputation.
   - Scaled numerical features using MinMax scaling.
   - Encoded categorical features using one-hot and label encoding, then applied transformation methods to decode the encoded values and saved them as a `.pkl` file.
   - Outliers handled using multiple techniques:
     - **Log Transformation** for skewed data.
     - **Square Root (Sqrt) Transformation**, but required a larger dataset for better results.
     - **Winsorization** (5th & 95th percentiles) to cap extreme values.
     - **Interquartile Range (IQR) Method** to remove extreme outliers.
   - Created additional feature engineering columns to enhance model predictions.
   
2. **Exploratory Data Analysis (EDA)**
   - Visualized key attrition trends using bar plots, histograms, and box plots.
   - Analyzed correlation between features and attrition rate using correlation heatmaps.
   
3. **Feature Selection**
   - Used multiple feature selection methods:
     - **Chi-Square Test (chi2):** Selected categorical features most relevant to the target variable.
     - **ANOVA (Analysis of Variance):** Identified significant numerical features.
     - **Mutual Information (MI):** Measured dependency between features and attrition.
     - **Recursive Feature Elimination (RFE):** Iteratively removed least important features to enhance model performance.
     - **Correlation Heatmap:** Removed highly correlated features to avoid multicollinearity.

4. **Model Training & Evaluation**
   - Used classification models including:
     - Logistic Regression
     - Random Forest
   - Evaluated models based on Accuracy, Precision, Recall, and F1-Score.
   - Performed hyperparameter tuning to improve model performance.

## Key Findings
- Work-life balance and job satisfaction were strong indicators of attrition.
- Employees with lower salaries and fewer years at the company had higher turnover rates.
- Random Forest performed best in predicting attrition, with an accuracy of over 85%.

## Learnings
- **Handling Outliers:** Applied winsorization, log transformation, sqrt transformation (for larger datasets), and IQR methods to maintain data integrity.
- **Feature Selection:** Experimented with Chi-Square, ANOVA, MI, RFE, and correlation heatmaps to identify the most relevant features.
- **Feature Engineering:** Created additional meaningful columns to improve prediction accuracy.
- **Model Performance Tuning:** Adjusted hyperparameters and selected optimal features to enhance performance.
- **EDA Techniques:** Learned how to visualize and interpret employee attrition trends effectively.

## Conclusion
This project provides insights into employee attrition factors and demonstrates how predictive models can help HR teams make data-driven retention strategies. Future improvements may include integrating real-time employee feedback and sentiment analysis for better predictions.

## Author
TC Antony

