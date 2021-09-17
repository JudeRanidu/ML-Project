**Link to GitHub Repository: ** https://github.com/JudeRanidu/ML-Project

**DrivenData Username: ** moracse_170504n

**Index No: ** 170504N

---

## Exploratory Data Analysis

- A class imbalance in the response variable was identified
- Using describe() identified some numerical columns are having a lot of 0's
- Used pairplots to identify whether there are any correlations between the numerical columns
- Identified the columns that are having missing values
- Identified most of the features are categorical in the given dataset
- Through inspections identified some categorical columns are correlated (eg: payment & payment_type) since they have similar categories

---

## Data Preprocessing

- Filled missing values of permit (using forward filling) & funder (using a new category "unknown") columns
- Dropped other columns which have missing values since some had a high percentage of missing values and others had less effect on the predictions
- Categorical columns with low cardinality (less than 10 features) were one-hot encoded
- Categorical columns with high cardinality (more than 10 features) were label encoded
- The numerical columns were scaled using Standard Normalization since original values were in different ranges
- The response variable was label encoded
- The 0's and negative values of construction_year, population & gps_height columns were imputed using the mean/median of the remaining observations of those columms

---

## Feature Engineering & Selection

- Created new column year_recorded using the date_recorded
- Selected a set of categorical columns by dropping correlated categorical cloumns through the inspections in EDA (for example keep source and remove source_type & source_class since they are correlated)
- Features having less impact on predictions due to nature of the feature (eg: recorded_by, num_private) & features which are some what unique to each observation (eg: id, wpt_name) were dropped

---

## Model Selection & Training

- Random Forest Classifier was used as the model
- Hyperparameter Optimization was done using Grid Search and identified the best parameters (n_estimators = 500, max_depth = 20, random_state = 1)

---

## Score and Rank

![Alt text](https://github.com/JudeRanidu/ML-Project/blob/main/Proof/score%20%26%20rank.jpeg)

---

## List of Submissions

![Alt text](https://github.com/JudeRanidu/ML-Project/blob/main/Proof/submission%20list.jpeg)
