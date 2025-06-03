readme_content = """
# Insurance Charges Prediction

This project aims to predict medical insurance charges based on personal attributes using various regression models. The dataset contains insurance customer data including age, sex, BMI, number of children, smoking status, and region.

---

## Dataset

- Source: `insurance.csv`
- Features:
  - `age`: Age of the insured person
  - `sex`: Gender (male/female)
  - `bmi`: Body Mass Index
  - `children`: Number of children/dependents
  - `smoker`: Smoking status (yes/no)
  - `region`: Residential area in the US (southwest, southeast, northwest, northeast)
  - `charges`: Medical insurance charges (target variable)

---

## Steps Performed

1. **Data Loading & Exploration**
   - Loaded data using `pandas`.
   - Checked data info, summary statistics, null values, and duplicates.
   - Dropped the `region` column (categorical but dropped in this analysis).

2. **Data Cleaning**
   - Removed duplicate rows.
   - Verified no missing values.

3. **Data Visualization**
   - Pairplot for numeric features.
   - Correlation heatmap to identify relationships between variables.

4. **Encoding Categorical Variables**
   - Converted categorical columns (`sex`, `smoker`) to numeric using `LabelEncoder`.

5. **Data Splitting & Scaling**
   - Split data into training (80%) and testing (20%) sets.
   - Applied standard scaling on feature data.

6. **Model Training & Evaluation**
   - Trained multiple regression models:
     - Linear Regression
     - K-Nearest Neighbors Regressor
     - Decision Tree Regressor
     - Random Forest Regressor
     - AdaBoost Regressor
     - Gradient Boosting Regressor
   - Evaluated models using R² (coefficient of determination) metric.
   - Gradient Boosting Regressor achieved the highest R² score (~0.85).

7. **Result Visualization**
   - Compared actual vs predicted charges with a scatter plot.

---

## Usage

1. Ensure you have the necessary libraries installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
