
# Housing EDA

## Objective
The goal of this project was to explore the housing dataset, perform data preprocessing, visualize important patterns, and build a regression model to predict house prices. The task also included interpreting model coefficients and plotting a regression line.

## Dataset
Name: Housing Dataset  
Size: 545 rows × 13 columns after preprocessing  
Target Variable: price  
Source: Provided in task materials  

---

## Steps Performed

### 1. Data Exploration
- Checked dataset shape, column names, data types, and null values.
- Displayed summary statistics (mean, median, std, min, max).
- Separated numerical and categorical columns.
- Dropped any ID-like columns.
- Converted categorical columns to category type for consistency.

### 2. Data Preprocessing
- Converted categorical variables into numerical using pd.get_dummies().
- Split the dataset into training (80%) and testing (20%) sets.
- Scaled all numerical features using StandardScaler.

### 3. Outlier Removal (Unique Approach)
- Applied IQR method in a loop for each feature in the training set.
- Removed extreme outliers only from the training set to avoid data leakage.
- Reduced training data from 436 rows to 118 rows after outlier removal.

### 4. Model Training - Linear Regression
- Trained a Linear Regression model on the cleaned training set.
- Evaluated the model on the test set using:
  - MAE (Mean Absolute Error)
  - RMSE (Root Mean Squared Error)
  - R² Score
- Performed 5-fold Cross-Validation to check model stability.

### 5. Feature Importance
- Plotted absolute coefficients from the Linear Regression model to identify the most influential features.
- Interpreted the sign and magnitude of each coefficient to understand positive or negative relationships with price.

### 6. Regression Line Plot
- Plotted a regression line for area vs. price to visually represent the relationship.
- Provided interpretation for each feature's coefficient:
  - Positive coefficient: Price increases as the feature increases.
  - Negative coefficient: Price decreases as the feature increases.
  - Near zero: No significant relationship.

---

## Tools and Libraries
- Python  
- Pandas, NumPy – Data manipulation  
- Matplotlib, Seaborn – Data visualization  
- Scikit-learn – Scaling, Encoding, Modeling, and Evaluation

---

## Key Insights
- area had the strongest positive impact on price.
- furnishingstatus_unfurnished had a notable negative impact on price.
- Several binary categorical variables had coefficients close to zero, indicating minimal effect.
- Outlier removal significantly reduced dataset size but helped in cleaner model training.

---
   git clone <repo_link>

