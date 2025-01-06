# Nutrition-aware Food Recommender Engine

## Project Overview

This project is a **hybrid food recommendation system** that combines **content-based filtering** (nutritional and ingredient similarity) and **collaborative filtering** (user ratings) to provide personalized and nutrition-aware recipe recommendations. The system helps users discover recipes that align with their dietary preferences and nutritional needs.

---

## Features

1. **Hybrid Recommendations:**
   - Combines **content-based filtering** (based on recipe ingredients and nutritional values) and **collaborative filtering** (based on user ratings) for personalized recommendations.

2. **Nutritional Awareness:**
   - Filters recipes based on maximum nutritional values (e.g., calories, fat, protein) to ensure recommendations meet dietary requirements.

3. **Model Evaluation:**
   - Evaluates the collaborative filtering model using **Root Mean Squared Error (RMSE)** and cross-validation to ensure accuracy and consistency.

4. **Visualization:**
   - Provides visualizations of top recommendations and nutritional distributions for better insights.

---

## Outputs

### Hybrid Recommendations
The system generates a list of recommended recipes based on user preferences and nutritional constraints. Here’s an example output:
Hybrid Recommendations: [500481, 6536, 444942, 314004, 469399, 9116, 336285, 373791, 3748, 3877]

---

### Model Evaluation
The collaborative filtering model (SVD) is evaluated using 3-fold cross-validation. Here are the results:
                  
                  Fold 1  Fold 2  Fold 3  Mean    Std     
RMSE (testset)    1.2280  1.2278  1.2299  1.2286  0.0010  
Fit time          19.65   20.12   20.20   19.99   0.24    
Test time         4.54    3.21    3.92    3.89    0.55    
Cross-Validation RMSE: 1.2285657780442316

---

## Datasets
The following datasets were used in this project:

1. **Recipes Dataset**:
   - Contains recipe details such as `RecipeId`, `Name`, `Calories`, `FatContent`, `ProteinContent`, and `RecipeIngredientParts`.
   - **Download Link**: [Recipes Dataset](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions)

2. **Reviews Dataset**:
   - Contains user reviews, including `AuthorId`, `RecipeId`, and `Rating`.
   - **Download Link**: [Reviews Dataset](https://www.kaggle.com/datasets/shuyangli94/food-com-recipes-and-user-interactions)

---

### Model Details

**Content-Based Filtering**:

Uses TF-IDF vectorization to analyze recipe ingredients.

Computes cosine similarity between recipes based on nutritional values and text features.

**Collaborative Filtering**:

Uses Singular Value Decomposition (SVD) to predict user ratings.

Evaluated using RMSE and cross-validation.

**Hybrid Model**:

Combines content-based and collaborative filtering recommendations for improved accuracy and relevance.

---

### Results
The SVD model achieves an RMSE of 1.2286, indicating good predictive accuracy.

The hybrid recommendations are diverse and nutritionally balanced, as shown in the example outputs.

Top Hybrid Recommendation:
+----------+--------------+--------------------+-------------------+---------------------+--------------------+
| RecipeId |     Name     |      Calories      |    FatContent     |   ProteinContent    |       Rating       |
+----------+--------------+--------------------+-------------------+---------------------+--------------------+
|   3748   | A-To-Z Bread | 0.5365402544340938 | 0.703536973719064 | -0.5721761988149869 | 4.7727272727272725 |
+----------+--------------+--------------------+-------------------+---------------------+--------------------+

---

### Contact

For questions or feedback, please contact:

Ahmed Ashraf Mohamed
Email: ahmed.radwan@gu.edu.eg
GitHub: AhmedElkomi

---
