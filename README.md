# Regression-assignment
Regression models on California Housing dataset

#  California Housing Regression Project

##  Objective
Apply multiple regression techniques on the **California Housing dataset** to predict median house values and compare model performance.

---

##  Dataset
- Source: `sklearn.datasets.fetch_california_housing`
- Features: Demographic and geographic attributes of California districts
- Target: Median house value (`MedHouseVal`)

---

##  Preprocessing
1. Loaded dataset into a **pandas DataFrame**.
2. Checked for missing values → none found (handled with mean imputation if present).
3. Applied **StandardScaler** to normalize features.

**Why?**
- Scaling ensures fair comparison across models, especially SVR and Gradient Boosting.
- Clean data prevents training errors.

---

##  Models Implemented
- **Linear Regression** → baseline linear fit
- **Decision Tree Regressor** → rule-based splits, captures non-linearity
- **Random Forest Regressor** → ensemble of trees, reduces overfitting
- **Gradient Boosting Regressor** → sequential boosting, strong predictive power
- **Support Vector Regressor (SVR)** → margin-based regression, sensitive to scaling

---

## 🔹 Evaluation Metrics
- **Mean Squared Error (MSE)** → penalizes large errors
- **Mean Absolute Error (MAE)** → average magnitude of errors
- **R² Score** → proportion of variance explained

---

## 📊 Results

| Model              | MSE  | MAE  | R²   |
|---------------------|------|------|------|
| Linear Regression   | 0.55 | 0.53 | 0.57 |
| Decision Tree       | 0.49 | 0.45 | 0.62 |
| Random Forest       | 0.25 | 0.32 | 0.80 |
| Gradient Boosting   | 0.29 | 0.37 | 0.77 |
| SVR                 | 0.35 | 0.39 | 0.72 |

---

###  Best Performing Model
**Random Forest Regressor**  
- Lowest MSE (0.25) and MAE (0.32)  
- Highest R² (0.80)  
- Justification: Ensemble averaging reduces overfitting and captures complex patterns effectively.

###  Worst Performing Model
**Linear Regression**  
- Highest errors (MSE 0.55, MAE 0.53)  
- Lowest R² (0.57)  
- Reasoning: A simple linear fit cannot capture the non-linear relationships in housing data.



---
##  Conclusion
- Among all tested models, **Random Forest Regressor** achieved the best performance with the lowest error values (MSE = 0.25, MAE = 0.32) and the highest R² score (0.80).  
  ➝ This shows that ensemble methods like Random Forest are highly effective at capturing complex patterns in housing data while reducing overfitting.

- The **Linear Regression model** performed the worst, with the highest error values (MSE = 0.55, MAE = 0.53) and the lowest R² score (0.57).  
  ➝ This indicates that a simple linear fit is insufficient for modeling the non-linear relationships present in the dataset.

- Overall, ensemble methods (Random Forest, Gradient Boosting) consistently outperformed simpler models, highlighting the importance of using advanced techniques for real-world regression tasks.
.


