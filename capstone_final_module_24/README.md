# Capstone Project: AI-Powered Nutrition Planner Final Report

## Summary
The AI-Powered Nutrition Planner helps busy people, fitness lovers, or anyone wanting a balanced diet create daily meal plans quickly. It aims to hit specific nutrition goals—2000 calories, 60g protein, 65g fat, and 250g carbs—using a dataset of 375 foods. By combining simple math models and a smart optimization tool, it suggests tasty, varied meals without the hassle of planning by hand.

---

## Define the Problem Statement
**Problem:** Planning meals that meet exact nutrition goals takes too much time and effort. People often guess portions or skip variety, missing targets like enough protein or the right calories.  
**Goal:** Build a tool that automatically designs three daily meals hitting 2000 calories, 60g protein, 65g fat, and 250g carbs, making healthy eating easy and fast.  
**Challenges:** Foods vary a lot (e.g., some have tons of fat, others zero protein), and balancing nutrients across meals is tricky.  
**Benefits:** Saves time, ensures balanced nutrition, and keeps meals interesting—perfect for anyone from gym-goers to busy parents.

---

## Model Outcomes or Predictions
**What We Did:** We used *regression*—a method to predict numbers like calories or protein based on food weight and type. We also used a *Genetic Algorithm (GA)*, a clever tool that mixes and matches foods to find the best meal combos.  
**Expected Output:** 
- Regression gives nutrient predictions for a single meal (e.g., how much chicken gives 20g protein).
- GA creates three meals totaling our targets (e.g., 1999.5 calories, 70.6g protein).<br>
**Learning Type:** Supervised learning—our models learned from food data with known nutrients to predict or plan meals.

---

## Data Acquisition
**Data Used:** We worked with a dataset of 375 foods, covering everything from apples to pizza. It includes columns like Food, Grams, Calories, Protein, Fat, and Carbs, plus categories (e.g., Dairy, Meat).  
**Source:** We started with the "Nutrition details for most common foods" dataset from Kaggle ([link](https://www.kaggle.com/datasets/niharika41298/nutrition-details-for-most-common-foods)), then added our own entries to reach 375 foods.<br>
**Why This Data:** It’s diverse—calories range from 0 to 1373, protein from 0 to 89g—letting us build flexible plans. We didn’t need multiple sources since this single set covers meats, veggies, carbs, and more.  
**Visualization:** In the notebook, a bar chart shows category counts (e.g., 34 Dairy items, 25 Vegetables R-Z), proving we’ve got enough variety to solve our meal-planning problem.

---

## Data Preprocessing/Preparation
**Cleaning:** The data was already clean—no missing numbers or weird entries. We just made sure columns like Calories were numbers, not text, using a simple check. No values were missing after this.  
**Techniques:** We didn’t need fancy fixes since the dataset was ready-to-go. We split foods into groups (meat, carbs, veggies) for meal planning, skipping junk like “Potato chips.”  
**Splitting:** For regression, we divided the data: 80% (300 foods) to train the models, 20% (75 foods) to test them. This split helps check if predictions work on new foods.  
**Encoding:** We turned categories (e.g., “Meat, Poultry”) into numbers (0s and 1s) so the models could use them, dropping one category to avoid overlap.

---

## Modeling
**Algorithms Chosen:**  
- **Linear Regression:** A basic model that predicts nutrients from food weight and category—like guessing calories from grams. Simple but a good start.  
- **Random Forest:** A smarter model that learns patterns better, using 100 “trees” to vote on predictions. It’s more accurate for tricky nutrient mixes.  
- **Genetic Algorithm (GA):** Not a predictor but a planner. It tests tons of meal combos, picking the best three to hit our targets, like a chef tweaking recipes.  
**Why These:** Linear Regression is easy to understand, Random Forest boosts accuracy, and GA solves the full-day challenge with variety.

---

## Model Evaluation
**Models Considered:** We focused on regression (predicting numbers like calories) since our goal is nutrient totals, not labels (e.g., “healthy” vs. “unhealthy”). GA isn’t a typical model but optimizes meal plans directly.  
**Evaluation Metrics:** 
- For regression, we used Mean Squared Error (MSE)—how far predictions miss the real numbers. Lower is better.  
- For GA, we used a “fitness score”—how close the three meals get to our targets, with penalties for repeats or overshooting protein.  
**Results:**  
- **Linear Regression:** Cross-validation MSE: 5584.48. Test MSE: {'Calories': 19981.59, 'Protein': 26.83, 'Fat': 182.76, 'Carbs': 381.22}. It’s decent but off on calories (big error: 19981.59).  
- **Random Forest:** Best settings: {'max_depth': None, 'min_samples_split': 5, 'n_estimators': 100}. Test MSE: {'Calories': 11525.55, 'Protein': 17.81, 'Fat': 73.41, 'Carbs': 422.29}. Better—cuts calorie error by 42% and protein by 33%.  
- **GA:** Total Nutrition: {'Calories': 1999.5, 'Protein': 70.6, 'Fat': 56.4, 'Carbs': 272.0}, Fitness Score: 674.21. Nearly perfect on calories (1999.5 vs. 2000), slightly high on protein (70.6 vs. 60) and carbs (272 vs. 250).  
**Best Model:** GA wins for full-day plans—it’s closest to our goals. Random Forest is tops for single-meal predictions due to lower errors.

---

## Important Findings
- **Variety Works:** With 375 foods across 15 categories, we can mix meats, carbs, and veggies to hit targets—Dairy and Vegetables give us lots of options.  
- **Accuracy Matters:** Random Forest beats Linear Regression (e.g., protein error 17.81 vs. 26.83), but GA nails the big picture (1999.5 calories!).  
- **Close but Adjustable:** GA’s plan (70.6g protein, 272g carbs) is a bit over—adding leaner meats or fewer carbs could perfect it.  
- **Time-Saver:** This tool turns hours of planning into minutes, keeping meals tasty and balanced.

---

## Suggestions for Next Steps
- **Test It Out:** Cook these meals—do they taste good and keep you full? Feedback could tweak portion sizes.  
- **More Foods:** Add options like low-carb veggies or plant-based proteins to hit 60g protein and 250g carbs exactly.  
- **App Idea:** Make this a phone app—enter your goals, get a plan. GA’s precision (674.21 fitness score) could sell it!  
- **Smarter Single Meals:** Upgrade regression to pick foods, not just scale them, for spot-on single-meal suggestions.

---

## How to Use
- **File:** `capstone_module_24.ipynb`  
- **Setup:** Install tools with `pip install pandas numpy matplotlib seaborn scikit-learn deap plotly scipy`  
- **Run:** Open the notebook, add the dataset in Cell 2, and run all cells to see meal plans and visuals.
