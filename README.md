🍷 Wine Quality Prediction & Model Comparison
🚀 Project Overview

This project builds and evaluates machine learning models to predict wine quality using physicochemical features. It compares Logistic Regression and Random Forest to understand model behavior on real-world, imbalanced datasets.

🎯 Objective
Predict wine quality (multi-class classification)
Compare model performance
Identify challenges like class imbalance and overlapping classes
Derive actionable insights from model evaluation

📊 Dataset
Red Wine Dataset
White Wine Dataset
Target Variable: Quality Score (3–9)

🧠 Approach

🔹 Data Preparation
Removed duplicates
Handled data consistency
Train-test split with stratification

🔹 Feature Engineering
Standardization applied (for Logistic Regression)
No scaling required for Random Forest

🔹 Model Building
Logistic Regression (baseline model)
Random Forest (ensemble model)

📈 Evaluation Strategy

To ensure balanced evaluation across all classes:

Accuracy
Confusion Matrix
Classification Report
⭐ Macro F1-score (primary metric)

📊 Results Summary
Dataset	Model             	Accuracy	Macro F1
Red	Logistic Regression      	0.58	    0.27
Red	Random Forest	            0.62	    0.29
White	Logistic Regression	    0.53	    0.22
White	Random Forest	          0.58	    0.28

🔍 Key Insights

🔴 Red wine dataset performed better than white
🌳 Random Forest outperformed Logistic Regression
⚖️ Strong class imbalance impacted performance
🎯 Models performed well on dominant classes (5 & 6)
❌ Minority classes (3, 4, 8, 9) had near-zero recall
🔄 High confusion between similar classes (5, 6, 7)

⚠️ Problem Identified

The models are biased toward majority classes due to class imbalance, leading to poor generalization for minority classes.

💡 Proposed Improvement

✔️ Apply class_weight="balanced"
→ Helps improve recall and F1-score for underrepresented classes

🧪 What This Project Demonstrates

End-to-end ML workflow
Model comparison & evaluation
Handling imbalanced datasets
Interpreting confusion matrix & F1-score
Translating results into business insights

🛠️ Tech Stack
Python 🐍
Pandas
NumPy
Scikit-learn

📌 Conclusion

Random Forest provides better predictive performance compared to Logistic Regression. However, both models struggle with class imbalance, highlighting the need for better data balancing or model tuning techniques to achieve reliable predictions across all classes.
