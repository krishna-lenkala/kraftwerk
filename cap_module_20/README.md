# Nutritional Data Analysis and Meal Suggestion Project

## Overview

This project focuses on exploring a dataset of nutritional information for various foods, performing Exploratory Data Analysis (EDA), and developing a baseline model for personalized meal suggestions using Linear Regression. Here's a breakdown of what's been accomplished:

### Data Loading and Preprocessing
- Loaded and cleaned a dataset containing nutritional data for different foods.
- Handled non-numeric entries, converted data types, and removed rows with missing data to ensure a clean dataset for analysis.

### Exploratory Data Analysis (EDA)
- **Basic Statistics:** Provided an overview of the distribution of nutritional values like calories, protein, fat, and carbohydrates.
- **Correlation Analysis:** Examined the relationships between different nutrients to understand dietary patterns.
- **Distribution Visualizations:** Created histograms to visualize the spread of each nutrient across food items.
- **Nutrient by Category:** Analyzed how nutrients vary across food categories, offering insights into dietary choices by group.

### Feature Engineering
- Engineered a new feature, `Energy_Density`, to assess the caloric content per gram of foods, useful for understanding energy efficiency.

### User Profile and Suitability
- Defined a user profile to match dietary needs with food items.
- Calculated a 'suitability' score for foods based on how well they align with the user's nutritional requirements.

### Baseline Model - Linear Regression
- Implemented a Linear Regression model to predict food suitability for meal planning.
- Evaluated model performance using metrics like Mean Squared Error (MSE) and R-squared.

### Meal Suggestion
- Generated meal plans based on the suitability scores predicted by the linear regression model, aiming for balanced nutrition across meals.

### Findings
- **Data Quality:** Managed to keep **273** entries post-cleaning, providing a solid base for analysis.
- **Correlations:** Strong correlation between calories and fat (r = 0.85), suggesting high-calorie foods are often high-fat.
- **Distributions:** Noted right-skewed distributions for fats and carbs, indicating few high-value outliers.
- **Model Performance:** The model showed moderate success with an R-squared of **0.63** and MSE of **0.015**.
- **Meal Plan Examples:** 
  - **Meal 1:** Included items like white bread and duck, focusing on carbs and protein.
  - **Meal 2:** Combines rolls with ice cream, showcasing high sugar and fat content.
  - **Meal 3:** A mix of beer, ice cream, flour, and rice, not ideal for balance but high in calories.

## Future Work
- **Module 24:** Planned to introduce K-means clustering for more nuanced meal suggestions based on dietary habits or nutritional profiles.


