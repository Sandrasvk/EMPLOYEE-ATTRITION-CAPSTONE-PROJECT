🚀 Employee Attrition Analytics: Predictive Modeling & Optimization
📌 Project Overview
This project focuses on predicting employee attrition using the IBM HR Analytics dataset. By leveraging advanced Machine Learning techniques, I developed a pipeline to identify high-risk employees, enabling data-driven retention strategies.

🛠️ Technical Workflow
1. Data Preprocessing & Cleaning
Removed non-contributing features (EmployeeCount, StandardHours, etc.).
Performed One Hot Encoding and Scaling to prepare categorical and numerical data for high-performance algorithms.

2. Multi-Algorithm Exploration
I implemented and compared several sophisticated models to find the most reliable predictor:

Logistic Regression: Established a baseline for linear separability.

Support Vector Machine (SVM): Optimized via GridSearchCV (C=0.95, kernel='sigmoid'), achieving a high training score of 87.7%.

AdaBoost Classifier: Demonstrated the highest raw accuracy of 88%.

Random Forest Classifier: Selected as the final production model.

3. Dimensionality Reduction (PCA)
To handle feature complexity, I applied Principal Component Analysis (PCA). This ensured the model focused on the most significant variance in the dataset, reducing the risk of overfitting and improving computational efficiency.

4. Rigorous Optimization (Grid Search & CV)
I utilized GridSearchCV with 5-Fold Cross-Validation across all major models. This guaranteed that the "Best Parameters" were chosen based on consistent performance across different data subsets, not just a single lucky split.

⚖️ Final Model Selection: Why Random Forest?
While SVM and AdaBoost showed high accuracy (87.7% and 88% respectively), I finalized the Random Forest model (Accuracy: 85%, CV Score: 87%) for the following reasons:

Stability & Generalization: Unlike AdaBoost (which can overfit on noise) or SVM (which can be sensitive to parameter shifts), Random Forest is a "Bagging" ensemble. It averages multiple decision trees, providing a more stable and generalized prediction for noisy HR data.

Robustness with PCA: Random Forest handles PCA-transformed features exceptionally well, maintaining a high Cross-Validation Score of ~87%.

The "Sweet Spot": Through Grid Search, I optimized the model to 49 estimators, achieving a perfect balance between complexity and predictive power.

📊 Key Metrics
Final Model: Random Forest (n_estimators=49)

Cross-Validation Reliability: 87.2%

Final Test Accuracy: 85.0%

Tools,Libraries Used
Language - Python
Jupyter Notebook
Numpy,Pandas,Matplotlib,Seaborn,Scikitlearn
