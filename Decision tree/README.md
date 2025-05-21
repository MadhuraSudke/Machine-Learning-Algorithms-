# 🌳 Decision Tree Regression – Understand the Algorithm Step-by-Step

## 📌 Goal

This mini-project focuses on **understanding how Decision Tree Regression works**—not exploring the dataset or performing EDA. The goal is to **learn the internal working of the algorithm**, how it splits data, and how it makes predictions, using a small salary dataset based on position levels.

---

## 🧠 What's the Idea Behind Decision Tree Regression?

A Decision Tree splits the data step by step based on certain conditions, until each group has similar enough values to make accurate predictions.

Here's how it works, step by step:

---

### 🔍 Step-by-Step Intuition

1. **The Algorithm Starts Splitting the Data**
   - It looks at all possible features and values to split the dataset into subsets.
   - The goal? To make the groups more predictable (i.e., reduce uncertainty).

2. **It Uses a Math Concept: Entropy or Variance**
   - In regression tasks, it mainly focuses on **variance reduction**—how much spread (uncertainty) is reduced after a split.

3. **Each Split Tries to Add More Information**
   - The algorithm chooses the split that **best reduces the variance** in the target values.

4. **When Does It Stop Splitting?**
   - It stops when no further meaningful information can be gained—when splitting doesn't reduce uncertainty anymore.
   - At this point, the split becomes a **terminal leaf**.

5. **Leaves = Predictions**
   - The data that reaches each leaf node is averaged to give the final prediction.
   - These leaves are the model's learned knowledge.

6. **Final Goal**
   - Break the dataset into pieces where each piece is easy to predict.
   - These breaks (splits) are chosen based on **minimizing impurity** or **reducing variance**.

---
