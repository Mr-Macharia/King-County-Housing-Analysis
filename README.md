
---

# **King County Housing Data Regression Analysis**

## **Project Overview**

This project explores a comprehensive **regression analysis** of the King County housing market using machine learning algorithms. Our main goal was to predict housing prices by analyzing various features of the properties, such as size, location, and year of construction, among others. Leveraging tools like **StatsModels** and **Scikit-Learn**, we applied multiple regression models, with a focus on improving accuracy and minimizing error metrics like RMSE.

As a team, we set out to achieve the following objectives:
1. **Build a regression model** with high accuracy and low RMSE (Root Mean Square Error), which would serve as our evaluation metric for model selection.
2. **Extract insights** from the data, identifying key factors that influence housing prices both positively and negatively.
3. **Understand the impact of independent features** (predictors) on the house prices to provide meaningful insights into the market dynamics.

---

## **Business Objectives**

We defined the following business objectives for the project:

- **Predict Housing Prices:** Develop a model capable of accurately predicting house prices based on various features.
- **Identify Key Features:** Uncover the most influential factors that impact housing prices in King County, such as location, house size, and market trends.
- **Enhance Understanding of Market Dynamics:** By analyzing the relationships between features and housing prices, we aim to provide insights that could be useful for real estate investors, developers, and buyers.

---

## **Data Source and Description**

The project is based on **King County housing data**, which contains a variety of features related to house sales. The dataset includes:
- **Sale prices** (target variable)
- **House attributes** like number of bedrooms, bathrooms, living area size, lot size, etc.
- **Geographical information** such as location (latitude, longitude) and zip codes.
- **Date of sale**, providing potential for feature engineering around seasonal trends.

We used a provided **data dictionary** to understand the meaning of each feature, ensuring we appropriately interpreted the data during analysis and modeling.

---

## **Project Workflow**

### **1. Data Cleaning**
Before diving into analysis, we performed a thorough **data cleaning** process to ensure the quality and integrity of the dataset:
- **Handled missing values** by either imputing or dropping them, depending on the significance of the feature.
- Ensured **categorical variables** with missing values were addressed by creating new categories rather than using common methods like mode or median imputation.
- Verified **date columns** and ensured they were in the correct format to facilitate feature engineering.
- Checked for **outliers** and decided on appropriate strategies for dealing with skewed data.

### **2. Data Analysis and Visualization**
With a clean dataset, we conducted an exploratory data analysis (EDA) to uncover patterns and relationships between the predictors and the target variable:
- **Histograms, scatter plots, and distribution plots** were used to visualize the distribution of features and identify trends.
- **Price distribution** was found to range from \$78,000 to over \$7,000,000, reflecting the wide variance in property values across King County.
- **Correlations between features** were checked to ensure that highly correlated predictors could be properly managed to avoid multicollinearity.

### **3. Feature Engineering**
One of the most critical aspects of this project was **feature engineering**:
- Created new features based on **domain knowledge**, such as seasonality in house prices. We noted that house prices often fluctuate depending on the time of year, with certain periods exhibiting higher sales activity.
- Engineered features like **house age** and **distance to important amenities**.
- Mapped and encoded categorical variables to numerical representations to ensure compatibility with machine learning models.

### **4. Model Building**
We developed several models to predict house prices, ensuring each model was fine-tuned for accuracy:
- Models included **StatsModels OLS Regression**, **Scikit-Learn Linear Regression**, **RandomForest Regressor**, **XGBoost**, and **LightGBM**.
- Our best-performing model was the **XGBoost algorithm**, with an **accuracy score of 86.5%** and a **normalized RMSE of 0.0172**. XGBoost performed well due to its ability to handle complex relationships and its efficient performance in gradient boosting.
- We used **cross-validation** to ensure that our models did not overfit the data and generalize well to unseen data.

### **5. Model Evaluation**
To evaluate the models:
- We used the **RMSE** as a measure of how well the model’s predictions aligned with the actual values.
- **Accuracy scores** were calculated, and we compared different models using metrics like R-squared.
- **Partial Dependency Plots (PDPs)** were employed to better understand the influence of individual features on the predictions.

---

## **Key Insights and Results**

- **Feature Importance:** Through Partial Dependency Plots (PDPs), we found that factors such as **square footage**, **location**, and **age of the house** significantly impacted house prices.
- **Seasonality:** As expected, house prices showed a seasonal trend, with higher sales and prices in specific periods of the year.
- **Geographical Influence:** Properties located in certain neighborhoods or zip codes demonstrated a higher average price, underlining the importance of location in real estate.

---

## **Challenges**

1. **Missing Data:** Key features like certain property attributes had missing values. This required careful handling to avoid negatively impacting the model.
2. **Skewed Data:** Many features were skewed, leading to challenges in deciding whether to log-transform or standardize the data.
3. **Domain Learning:** As a group, we had to familiarize ourselves with **real estate concepts**, especially for feature engineering. This was a valuable learning experience as it improved our understanding of the domain.

---
