# Exploratory Data Analysis: Titanic Survival
## Overview

This project performs an end-to-end Exploratory Data Analysis (EDA) on the
Titanic passenger dataset to understand which factors influenced survival. It
is written as a Google Colab notebook (Titanic_EDA_Project.ipynb) and follows a
structured workflow from data loading to insights.

## Objectives

- Inspect the structure and quality of the dataset
- Handle missing values and duplicates
- Explore individual features (univariate analysis)
- Study relationships between features and survival (bivariate analysis)
- Engineer new features such as family size and age groups
- Summarize key insights about survival patterns

## Dataset

The Titanic dataset is loaded directly through the seaborn library
(sns.load_dataset("titanic")), so no manual download is needed. It contains
891 passengers with details such as class, gender, age, fare, family
relations and port of embarkation.

## Tools and Libraries

- Python 3
- Pandas and NumPy (data handling)
- Matplotlib and Seaborn (visualization)
- Google Colab (execution environment)

## Project Workflow

1. Setup and imports
2. Load the data
3. Data overview (info, summary statistics)
4. Data quality check (missing values map, duplicates)
5. Data cleaning
   - Drop the deck column (about 77% missing)
   - Fill age using the median of each class and gender group
   - Fill embarked and embark_town with the most frequent value
   - Remove duplicate rows and redundant columns
6. Univariate analysis (survival, class, gender, age, fare)
7. Bivariate analysis (survival by gender, class, port, age)
8. Correlation analysis (heatmap)
9. Feature engineering
   - family_size, is_alone
   - age_group (Child, Teen, Young Adult, Adult, Senior)
   - fare_band (Low, Medium, High, Very High)
10. Summary tables (survival rate by class and gender)
11. Key insights and conclusion

## How to Run

1. Open https://colab.research.google.com
2. Go to File > Upload notebook and select Titanic_EDA_Project.ipynb
3. Click Runtime > Run all
4. View the charts and outputs under each section

To run locally instead:

pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Titanic_EDA_Project.ipynb

## Key Findings

- Gender was the strongest factor: women survived at a much higher rate
  than men.
- First-class passengers survived more often than third-class passengers.
- Children had a higher survival rate than other age groups.
- Passengers in small families (2 to 4 people) survived more often than
  those travelling alone or in very large families.
- Higher fares correlated with survival, largely because fare is linked to
  passenger class.

## Future Work

- Build a predictive model (Logistic Regression, Random Forest) using the
  engineered features
- Run statistical tests (chi-square, t-test) to confirm the patterns
- Repeat the workflow on other datasets such as customer churn or retail sales

## Author

Meesala Mohan Surya Sai

Intern ID: CITS9842
