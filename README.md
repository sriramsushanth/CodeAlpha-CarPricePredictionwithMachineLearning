# CodeAlpha-CarPricePredictionwithMachineLearning

## Project Overview
This project focuses on predicting the selling price of used cars using Machine Learning techniques. The main objective of this project is to build a smart and reliable regression model that can estimate car resale prices based on important vehicle-related features such as manufacturing year, showroom price, fuel type, kilometers driven, transmission type, seller type, and ownership details.

In the automobile market, estimating the correct resale value of a car manually can be difficult because multiple factors influence the final price. This project solves that problem using data-driven Machine Learning models which can learn pricing patterns from historical car data and generate accurate predictions.

Instead of using only one traditional regression model, this project follows a hybrid ensemble learning approach where multiple advanced Machine Learning algorithms are combined together to improve overall prediction accuracy and robustness.

The project was developed using Python programming language along with several powerful libraries such as Pandas, NumPy, Scikit-learn, XGBoost, CatBoost, Matplotlib, and Seaborn.

## Dataset Information
The dataset contains a total of 301 rows and 9 columns. The target variable in this project is Selling_Price, which represents the resale value of the vehicle.

The dataset contains the following columns:
* Car_Name – Name of the car model
* Year – Manufacturing year of the vehicle
* Selling_Price – Selling price of the car
* Present_Price – Current showroom price of the car
* Driven_kms – Total kilometers driven
* Fuel_Type – Petrol, Diesel, or CNG
* Selling_type – Dealer or Individual seller
* Transmission – Manual or Automatic
* Owner – Number of previous owners

Since the target variable contains continuous numerical values, this becomes a supervised Machine Learning regression problem.

## Project Approach
This project follows a complete Machine Learning workflow starting from data preprocessing to model training, evaluation, visualization, and model saving.

1) Initially, the dataset was loaded and analyzed to understand its structure, data types, missing values, and statistical information. Basic preprocessing steps were performed to prepare the dataset for Machine Learning training.
2) The dataset contains categorical columns such as Car_Name, Fuel_Type, Selling_type, and Transmission. Since Machine Learning models cannot directly understand text-based categorical data, Label Encoding was applied to convert these columns into numerical values.
3) After preprocessing, the dataset was divided into training and testing sets using an 80:20 ratio. Multiple advanced regression models were then trained individually on the dataset.

The models used in this project are:
* XGBoost Regressor
* Random Forest Regressor
* CatBoost Regressor

Instead of depending on only one model, all three algorithms were combined together using a *Stacking Regressor* with *Ridge Regression* as the final meta-model.

This hybrid ensemble learning approach improves prediction performance because different models learn different patterns from the dataset. Combining their predictions helps reduce individual model weaknesses and improves overall stability and accuracy.

## Why This Pipeline Was Chosen
The pipeline used in this project was selected carefully based on the characteristics of the car price dataset.

The dataset contains:
* Structured tabular data
* Numerical and categorical features
* Non-linear relationships between features and target values

Traditional Linear Regression models often struggle to capture complex feature relationships present in real-world automobile datasets. Therefore, advanced ensemble learning models were selected.

1) XGBoost Regressor: 
XGBoost was chosen because it performs extremely well on structured datasets and can capture complex non-linear patterns efficiently. It also provides high accuracy and strong feature importance analysis.

2) Random Forest Regressor: 
Random Forest was used because it reduces overfitting by combining predictions from multiple decision trees. It performs well on tabular datasets and provides stable predictions.

3) CatBoost Regressor: 
CatBoost was selected because it handles categorical features effectively and improves prediction performance with minimal preprocessing requirements.

4) Stacking Regressor: 
Instead of selecting only one “best” model, predictions from all three models were combined using a Stacking Regressor with Ridge Regression as the final estimator. This hybrid ensemble learning approach improves generalization performance and prediction robustness.

This process is highly suitable for the current dataset because ensemble learning models perform exceptionally well on structured automobile pricing data.

## Machine Learning Workflow
The complete workflow of the project follows the following pipeline:
*Data Collection → Data Analysis → Data Preprocessing → Label Encoding → Train-Test Split → Model Training (XGBoost + RandomForest + CatBoost) → Stacking Ensemble Learning → Prediction → Model Evaluation → Visualization Dashboard → Model Saving*

## Model Evaluation
Different evaluation metrics were used to measure the performance of the trained model properly.

1) R² Score:
R² Score measures how well the model explains the variance in the dataset. Higher R² values indicate better prediction performance.
2) MAE (Mean Absolute Error): 
MAE measures the average prediction error between actual and predicted selling prices.
3) RMSE (Root Mean Squared Error): 
RMSE measures the overall prediction error magnitude and penalizes larger errors more strongly.
4) MAPE (Mean Absolute Percentage Error): 
MAPE measures prediction error percentage relative to actual values.

Cross-validation was also performed to check model stability and consistency across different training folds.

## Data Visualization
This project also includes a professional visualization dashboard for better understanding of dataset behavior and model performance.

The visualizations are:
* Correlation Heatmap
* Actual vs Predicted Plot
* Feature Importance Graph
* Price Distribution Histogram
* Top 15 Cars by Median Selling Price
* Residual Error Plot

These visualizations help analyze feature relationships, model prediction quality, residual patterns, and important pricing factors.

## Technologies Used
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* XGBoost
* CatBoost
* Joblib

## Real-World Applications
This project demonstrates how Machine Learning can automate vehicle price estimation in real-world business scenarios.

Similar systems are used in:
1) Online automobile marketplaces
2) Car resale platforms
3) Vehicle dealerships
4) Insurance companies
5) Automotive valuation systems

The project also provides practical understanding of regression modeling, ensemble learning, model evaluation, and predictive analytics.

## Future Improvements
This project can be improved further in the future by:
* Using larger automobile datasets
* Applying advanced feature engineering techniques
* Deploying the model using Streamlit or Flask
* Creating a real-time prediction web application
* Using Deep Learning-based regression models
* Performing advanced hyperparameter optimization

## Conclusion
The Car Price Prediction project successfully demonstrates the complete Machine Learning regression workflow using a hybrid ensemble learning approach. Instead of relying on a single regression model, multiple advanced algorithms were combined using a Stacking Regressor to improve prediction accuracy and robustness.

The project highlights important Machine Learning concepts such as preprocessing, ensemble learning, model evaluation, visualization, cross-validation, and predictive system development. It serves as a strong practical implementation of Machine Learning for real-world automobile price prediction problems.
