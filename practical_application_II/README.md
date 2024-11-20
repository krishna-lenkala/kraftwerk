# Used Car Price Analysis

## Overview
This project analyzes used car prices to identify key factors influencing pricing and to develop predictive models. The goal is to provide actionable insights for used car dealerships to optimize their inventory and pricing strategies.

## Key Findings
- **Data Overview**: The dataset includes various features of used cars, including price, year, odometer readings, condition, and manufacturer.
- **Price Distribution**: Most vehicles are priced lower, with a few high-value outliers.
- **Price vs. Year**: Newer cars generally command higher prices.
- **Price vs. Odometer**: Higher mileage typically results in lower prices.
- **Average Price by Manufacturer**: Certain brands consistently have higher average prices.

## Model Performance
We evaluated several regression models to predict used car prices:
| Model               | Test RMSE   | R² Score |
|---------------------|-------------|----------|
| Linear Regression    | 10,658.06   | 0.5156   |
| Ridge Regression     | 10,656.35   | 0.5157   |
| **Lasso Regression** | **10,655.29** | **0.5158** |

The best-performing model was **Lasso Regression** with an RMSE of **10,655.29** and an R² score of **0.5158**.

## Recommendations
### Inventory Management
1. **Focus on High-Value Brands**: Prioritize acquiring vehicles from manufacturers that yield higher average prices.
2. **Age and Mileage Balance**: Maintain a mix of newer vehicles (3-5 years old) with lower mileage.

### Pricing Strategy
1. **Dynamic Pricing Model**: Implement data-driven pricing strategies based on model predictions.
2. **Monitor Local Market Trends**: Regularly review local market data to adjust inventory and pricing.

### Marketing Focus
1. **Highlight Key Features**: Emphasize low mileage and good condition in marketing materials.
2. **Targeted Advertising**: Tailor marketing campaigns based on popular brands and models in your area.

### Continuous Improvement
1. **Data Collection**: Continuously collect sales data to refine predictive models.
2. **Model Updates**: Regularly retrain models with new data to maintain accuracy.

## Conclusion
This analysis provides valuable insights into the factors influencing used car prices and highlights effective strategies for inventory management and pricing optimization. By leveraging these findings, dealerships can enhance operations, improve customer satisfaction, and increase profitability.
