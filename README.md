# Titanic-Dataset EDA

This repository contains an exploratory data analysis (EDA) performed on the Titanic dataset. The analysis aims to uncover insights into the survival patterns of passengers by examining demographic and socio-economic factors.

## Overview
The dataset consists of 891 records and 12 variables. The analysis focuses on understanding how passenger characteristics such as age, gender, class, and family size impacted survival outcomes on the Titanic.

## Data Overview
**Dataset Size:** 891 rows x 12 columns
**Integer Columns:** PassengerId, SibSp (number of siblings/spouses), Parch (number of parents/children), Age, Fare
**Categorical Columns:** Name, Sex, Ticket, Cabin, Embarked, Survived (0 = died, 1 = survived), Pclass (1, 2, 3)

## Data Cleaning and Preprocessing
**Missing Values:**
Age: 177 missing values (~20%). These were handled via imputation (using the mean or median) or by removing rows.
Cabin: 687 missing values (~77%). Due to the high rate of missing data, the Cabin column was removed.
**Outliers:**
Age: 66 outliers identified, with most ages concentrated between 25 and 40, though the distribution is right-skewed.
SibSp & Parch: Outliers present with most passengers having 0 or 1 family member.
Fare: 116 outliers were detected. The distribution is bimodal, indicating a majority of 3rd class fares with a few high values corresponding to 1st class.

## Exploratory Data Analysis
**Histograms:**
Age: Distribution is right-skewed with a peak around 25-30 years.
SibSp & Parch: Both show exponential distributions with most values in the range of 0-1.
Fare: The bimodal distribution reflects the differences between travel classes.
**Bar Charts:**
Pclass: Majority of passengers were in 3rd class.
Sex: Approximately 60% of the passengers were male and 40% were female.
Embarked: Most passengers boarded at Southampton.
Survival: There were more non-survivors than survivors overall.
**Correlation Analysis:**
Age shows a weak positive correlation with PassengerId and Fare, but a weak negative correlation with SibSp and Parch.
SibSp and Parch are moderately positively correlated (0.41).
Fare also exhibits weak positive correlations with Age, SibSp, and Parch.
**Hypothesis Testing**
Survival by Age: Non-survivors tend to peak around age 30.
Survival by Gender: Females showed higher survival rates compared to males.
Survival by Class:
1st Class: Higher survival rates.
2nd Class: A balanced outcome with a slight edge toward survivors.
3rd Class: A higher proportion of non-survivors.
## Conclusion
The analysis reveals that survival on the Titanic was influenced by factors such as gender, travel class, age, and family size. Females and 1st class passengers had a better chance of survival, while males and 3rd class passengers were less likely to survive. These insights emphasize the importance of data cleaning and proper handling of missing values and outliers to ensure accurate predictive modeling.

## Repository Structure
README.md: This file.
Data/: Contains the dataset in CSV format
Src/: Jupyter notebooks detailing the EDA process.
Docs/: Scripts used for data cleaning and visualization.
Results/: Output visualizations and statistical analysis results.
