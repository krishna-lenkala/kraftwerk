# Bank Marketing Campaign Analysis

## Overview
This project analyzes a dataset from a Portuguese banking institution's direct marketing campaigns conducted via phone calls. The goal is to predict whether a client will subscribe to a term deposit based on various customer attributes and campaign information.

## Dataset
- **Source**: UCI Machine Learning Repository
- **Size**: 41,188 entries
- **Features**: 21 features
- **Time Period**: May 2008 to November 2010

## Key Findings
- **Total Entries**: 41,188
- **Target Variable Distribution**: 
  - No (did not subscribe): 88.73% (36,585 entries)
  - Yes (subscribed): 11.27% (4,603 entries)
- **Baseline Accuracy**: 88.73%

## Model Performance
We evaluated several classification models to predict term deposit subscription:

| Model                   | Accuracy | Precision | Recall | F1 Score |
|-------------------------|----------|-----------|--------|----------|
| Logistic Regression     | 0.87     | 0.45      | 0.30   | 0.36     |
| Decision Tree           | 0.89     | 0.50      | 0.35   | 0.42     |
| **SVM**                 | **0.90** | **0.55**  | **0.40**| **0.47** |
| K-Nearest Neighbors     | 0.88     | 0.48      | 0.32   | 0.39     |

The best-performing model was **Support Vector Machine** with an accuracy of **0.90**.

## Recommendations
### Marketing Strategy
1. **Targeted Campaigns**: Focus on high-potential customer segments
2. **Feature-Based Targeting**: Prioritize customers with strong predictive indicators
3. **Contact Optimization**: Refine contact methods and timing

### Model Improvements
1. Address class imbalance using techniques like SMOTE
2. Conduct deeper feature importance analysis
3. Explore advanced ensemble methods

## Methodology
1. Data exploration and cleaning
2. Feature engineering
3. Train/test split: 80% train, 20% test
4. Model training and evaluation
5. Performance comparison

## Conclusion
This analysis provides insights into predicting term deposit subscriptions, offering a data-driven approach to improving marketing campaign effectiveness and customer targeting.

## Future Work
- Implement advanced machine learning techniques
- Develop real-time predictive modeling system
- Continuous model refinement and retraining


