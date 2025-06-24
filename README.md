# Student Grade Prediction
This project was undertaken as a part of the curriculum for 6th semester of B.Sc. Computer Science, Statistics and Mathematics under the Department of Mathematics, University Institute of Science, Chandigarh University. Conducted an end-to-end analysis using **Python** and **regression modeling** to predict academic performance for **B.Sc. students** (Computer Science, Statistics, and Mathematics).  
The goal was to surface patterns that could guide early academic intervention and improve learning outcomes.

---

## Data Overview

Data was collected anonymously from **51 students** in Chandigarh University’s 5th semester of B.Sc. Computer Science, Statistics and Mathematics, ensuring privacy and minimizing response bias.

The study considered:
- Living Arrangements  
- High School Education 
- Attendance  
- Self-reported engagement levels  

In order to assess the predictors of **CGPA**.

---

## Data Engineering & Feature Creation

- Captured **14+ features** including location, gender, education board, attendance, and focus scores (1–10 scale).  
- Applied **Binary Encoding** for categorical variables.  
- Introduced derived features like **Living Category** to capture lifestyle impact.  
- Eliminated low-correlation features (threshold: **0.12**) to prevent noise and overfitting.

---

## Key Insights

- **Living Arrangement**:  
  Day Scholars had the highest average CGPA, followed by Hostel/PG, then Flat residents.

- **Board Impact**:  
  Students from **State Boards** slightly outperformed **ICSE** and **CBSE** counterparts.

- **Focus vs. Attendance**:  
  Focus scores were stronger predictors than raw attendance, indicating **quality over quantity**.

- **Gender**:  
  No statistically significant difference in academic performance across genders.

---

## Model Performance

| Rank | Model                     | MAE     | RMSE     | RMSE (CV) | MSE      | R² Score |
|------|---------------------------|---------|----------|-----------|----------|----------|
| 1    | Lasso                     | 0.09256 | 0.11175  | 0.38895   | 0.01249  | **0.91236** |
| 2    | GradientBoostingRegressor| 0.16603 | 0.17807  | 0.27110   | 0.03171  | **0.77748** |
| 3    | RandomForestRegressor    | 0.17583 | 0.18923  | 0.35048   | 0.03581  | **0.74870** |
| 4    | BayesianRidge            | 0.17023 | 0.20693  | 0.26359   | 0.04282  | **0.69952** |
| 5    | DecisionTreeRegressor    | 0.18333 | 0.22128  | 0.48374   | 0.04897  | **0.65637** |
| 6    | Ridge                    | 0.23978 | 0.26998  | 0.26426   | 0.07289  | **0.48849** |
| 7    | LinearRegression         | 0.24738 | 0.27533  | 1.60375   | 0.07581  | **0.46803** |


- **Lasso’s regularization** improved model interpretability and minimized multicollinearity due to its inherent ability to penalise the absolute magnitudes of the coefficients.
- Still captured over **91% variance**.
- **Cross-validation** confirmed robustness with low error margins.

---

## Applications and Insights

- **Academic Risk Monitoring**:  
  Helps identify at-risk students, enabling educators to properly allocate resources to them and help them achieve better scored by the time of the final exam.

- **Targeted Support**:  
  Enables resource prioritization based on risk profiles (e.g., flat residents with low focus).

- **Curriculum Adaptation**:  
  Insights on education board performance can guide teaching strategies to identify gaps in self learning methodologies and pre-requisite knowledge.

- **Engagement Design**:  
  Emphasizes interactive learning that retains student attention and interest on the subject, over strict attendance mandates.

---
