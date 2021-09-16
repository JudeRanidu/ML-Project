## Exploratory Data Analysis

- A class imbalance in the resposible variable was identified
- Using describe() identified some numerical columns are having a lot of 0's
- Used pairplots to identify whether there are correlations between the numerical columns
- Identified the columns that are having missing values
- Identified most of the features are categorical in the given dataset
- Through inspections identified some categorical columns are correlated (eg: payment & payment_type) since they have similar categories

---

## Data Preprocessing

- Dropped the columns which have missing values since some had a high percentage of missing values and others had less effect on the predictions
- The selected categorical columns were one-hot encoded
- The numerical columns were scaled using Standard Normalization since original values were in different ranges
- The response variable was label encoded
- The 0's and negative values of construction_year & gps_height columns were imputed using the mean of remaining observations

---

## Feature Engineering & Selection

- Created new column year_recorded using the date_recorded
- Selected a set of categorical columns by dropping correlated categorical cloumns through the inspections in EDA
- Categorical columns with High Cardinality were dropped
- Features having less impact on predictions (due to nature of the feature) & features which are some what unique to each observation (eg: id, wpt_name) were dropped

---

## Score and Rank (as of 15-09-2021)

- Random Forest Classifier was used as the model
- Hyperparameter Optimization was done using Grid Search and identified n_estimators as 500 and max_depth as 20

---

## Score and Rank (as of 15-09-2021)

![Alt text](./Proof/score & rank as of 15-09-2021.jpeg)

---

## List of Submissions

![Alt text](./Proof/submission list.jpeg)