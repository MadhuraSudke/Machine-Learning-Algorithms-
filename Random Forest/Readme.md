🧠 Ensemble Learning — Comprehensive Notes
Overview

Ensemble Learning is a powerful technique in Machine Learning where we combine multiple models (learners) to create a single, more accurate and robust model.
The key idea is that a group of weak learners can come together to form a strong learner — similar to the wisdom of crowds.

There are different ways to make models diverse:

Using different algorithms (e.g., Decision Tree, Logistic Regression, SVM)

Using same algorithms trained on different subsets of the data

Using different hyperparameters or feature subsets

⚖️ Why Ensemble Learning?

Real-world data is complex, and a single model often cannot capture all patterns.
Ensemble methods help by:

Reducing bias (underfitting)

Reducing variance (overfitting)

Increasing robustness of predictions

However, they come with increased computational cost and complexity since multiple models must be trained.

🧩 Types of Ensemble Learning
1. Voting Ensemble

Concept: Combines predictions from multiple different models trained on the same dataset.

Classification: Uses majority voting (hard voting) or average of predicted probabilities (soft voting).

Regression: Takes the average of predictions.

Example: Combine SVM, Logistic Regression, and Decision Tree.

2. Bagging (Bootstrap Aggregation)

Concept: Uses the same algorithm but trains each base model on a different random subset of the data (with replacement).

Goal: Reduce variance and prevent overfitting.

Famous Example: Random Forest (ensemble of decision trees).

Intuition: Each tree “votes,” and the final result is the majority or mean.

3. Boosting

Concept: Trains models sequentially, where each model tries to correct the errors of the previous one.

Goal: Reduce bias and variance by focusing more on difficult samples.

Popular Algorithms:

AdaBoost

Gradient Boosting

XGBoost

LightGBM

CatBoost

Each subsequent model learns from the mistakes of earlier ones, leading to a strong final model.

4. Stacking (Stacked Generalization)

Concept: Combines predictions of multiple base models (level-0 models) and feeds them into a meta-model (level-1) for final prediction.

How it works:

Train multiple base models on the same dataset (e.g., SVM, Logistic Regression, Decision Tree)

Collect their predictions

Train a meta-model (e.g., KNN, Linear Regression) on these predictions

Advantage: Learns how to best combine models — instead of simple voting.

⚙️ When to Use Ensemble Learning?

✅ When your model has high variance (e.g., Decision Trees)
✅ When your single model’s performance has plateaued
✅ When your dataset is complex or noisy
✅ Practically — almost always, as ensembles often outperform individual models in competitions and production.

📈 Advantages

Improves accuracy and generalization

Reduces bias and variance

Increases model robustness

Works well even with simple base learners

⚠️ Disadvantages

Computationally expensive

Harder to interpret

Training time increases

Requires careful hyperparameter tuning

