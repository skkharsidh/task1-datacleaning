# task1-datacleaning


## Objective
Clean and prepare a raw dataset (Titanic) so it is ready for machine learning.

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, scikit-learn (Google Colab)

## Steps Performed
1. **Explored the data:** checked data types and missing values with `info()` and `isnull().sum()`.
2. **Handled missing values:**
   - `Age` (177 missing) filled with the median
   - `Embarked` (2 missing) filled with the mode
   - `Cabin` (687 missing) dropped because most values were missing
   - `PassengerId`, `Name` and `Ticket` dropped as they are not useful for ML
3. **Encoded categorical features:**
   - `Sex` label encoded (male = 0, female = 1)
   - `Embarked` one-hot encoded
4. **Visualized and removed outliers:** boxplots of `Age` and `Fare`, outliers removed with the IQR method (891 rows before, 718 after, 173 removed)
5. **Standardized numeric features:** `Age` and `Fare` scaled with `StandardScaler` (mean about 0, std about 1)

## Files
- `Titanic-Dataset.csv`: original raw dataset
- `task1_data_cleaning.ipynb`: full code notebook
- `cleaned_data.csv`: final cleaned dataset
- `boxplots_before.png`: outliers before removal
- `boxplots_after.png`: boxplots after removal

## What I Learned
Data cleaning, handling null values, encoding categorical variables, outlier removal and feature scaling.
