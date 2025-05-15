# 🌳 Decision Tree Regression - Intuition & Implementation

This project is focused on **understanding the intuition behind Decision Tree Regression** using a **small dataset** and a clean, step-by-step breakdown. The goal is **not** just to apply a library, but to grasp **how** and **why** Decision Trees work the way they do in regression tasks.

---

## 🧠 Objective

To explain and visualize the **step-by-step working** of a Decision Tree Regression algorithm—from splitting the data to making predictions—using a simple example.

---

## 📊 Dataset

A small CSV file is used, consisting of two columns:

- `Level`: Represents a categorical/ordinal input feature (like job level or experience).
- `Salary`: Target variable to be predicted.

This simplicity helps us focus on **algorithmic understanding**, not on data preprocessing or complexity.

---

## 🔍 What is Decision Tree Regression?

A Decision Tree Regression algorithm builds a model in the form of a **tree structure**. It splits the data into smaller regions recursively, and for each region, the **mean** of target values is predicted.

---

## ⚙️ Step-by-Step Intuition Behind the Algorithm

### 1. **Start with the Whole Dataset**
The root node contains all data points. The model will attempt to split the data at different values of the input feature (`Level`) to reduce prediction error.

---

### 2. **Try All Possible Splits**
The algorithm checks **all midpoints between data points** in the `Level` feature. For example, if the values are `[1, 2, 3]`, possible splits are `1.5`, `2.5`, etc.

---

### 3. **Calculate the Mean Squared Error (MSE)**
For every possible split:
- It divides the data into two groups.
- Calculates the **mean of the target variable** (`Salary`) in each group.
- Computes the **MSE** for each split.
  
> MSE = average((actual - predicted)²)

The split with the **lowest MSE** is chosen.

---

### 4. **Recursive Splitting**
Once the best split is found:
- The data is divided into left and right nodes.
- The process repeats for each child node.
- Splitting stops when:
  - All data points in a node are the same
  - Or a minimum node size is reached
  - Or the MSE no longer improves significantly

---

### 5. **Prediction**
Once the tree is built:
- To predict a new value, the model traverses the tree from root to leaf based on the input.
- The output is the **average value of the target** in the leaf node.

---

## 📒 Notebook Overview

In `57b4a64b-4b69-4c27-bff7-9ed2b309411e.ipynb`, you'll find:
- Visualization of data.
- Manual step-by-step tree building.
- Comparison with `DecisionTreeRegressor` from `sklearn`.
- Visual tree plots for better understanding.

---

## 🚀 How to Run

```bash
pip install pandas matplotlib scikit-learn
