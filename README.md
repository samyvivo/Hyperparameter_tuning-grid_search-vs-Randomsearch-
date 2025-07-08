# Hyperparameter_tuning-grid_search-vs-Randomsearch-


🔍 Grid Search vs Random Search in Hyperparameter Tuning 🔍

🧠 Machine Learning models aren’t just about choosing the right algorithm—they’re about fine-tuning it too!
In my latest notebook, I explored two widely used methods for hyperparameter tuning: Grid Search and Random Search, and applied both on a classification task using RandomForestClassifier.

💡 What's the Difference?
🔎 Grid Search: Tries all possible combinations of the given hyperparameter grid. It’s exhaustive and great for small, well-defined spaces—but can be computationally expensive.
🔍Random Search: Selects random combinations over the search space. It's faster and often finds good results with fewer iterations, especially in high-dimensional spaces.

📊 What I Did:
Used GridSearchCV and RandomizedSearchCV from scikit-learn
• Defined the same parameter grid for both
• Measured accuracy and fit times to compare efficiency and performance

Explanation of the code:
📘 "Hyperparameter Tuning (GridSearch vs RandomSearch)"

✅ 1. Imports and Dataset Loading
• Loads the Breast Cancer dataset from scikit-learn.
• Converts it into a pandas DataFrame for ease of exploration.

🧹 2. Data Preparation
• X: input features (30 features)
• y: target variable (0 = malignant, 1 = benign)

📦 3. Train/Test Split
•Splits dataset into training (80%) and test (20%) sets using a fixed seed for reproducibility.

📐 4. Model Setup: Support Vector Machine Classifier

🔍 5. Grid Search CV
• Performs exhaustive search over all parameter combinations (4×4 = 16 models).
• 5-fold cross-validation is used for each.
• Best model found is stored in grid_search.best_estimator_.

🔍 6. Random Search CV
• Tries only 10 random combinations from a wider parameter distribution.
• Much faster than grid search, especially for large search spaces(

📈 7. Performance Comparison
• Evaluates both tuned models on the same test set.
 Best Parameters = {C : 2, kernel : linear}
• Compares final accuracy scores.
 Highest Accuracy = 95.8%

📌 Key Results and Insights
• Grid Search finds the optimal hyperparameters by brute force but can be slow.
• Run time in my laptop with Intel Core i7-9750H, 2.60 GHz : 
⏱ 38.7 sec for Grid Seaech 
⏱ 30.9 sec for Random Search
• Random Search often gets almost as good results (or better in some cases) faster.
• In practical ML projects, Random Search is usually preferred for large or expensive models.
