# Project 1

# Flight Delays Analysis 

**Prepared by:** [Thulasi.P]  
**Course/Program:** Project B — Flight Delays  

---

## Overview

This project analyzes flight performance and delay metrics by merging operational flight data with an airline lookup table. The pipeline audits raw data, cleans recorded sentinels and invalid records, evaluates airline and route performance, and investigates the relationship between flight distance and delays.

---

## Project Structure & Six-Step Workflow

1. **Step 1 — Load & Look:** Load datasets (`flights.csv` and `airlines.csv`), inspect initial shapes, data types, and first few rows.
2. **Step 2 — Audit:** Identify missing values (`isna()`), invalid numeric sentinel values (`describe()`), text casing/whitespace discrepancies (`value_counts()`), exact/key duplicates, and unmapped airline lookup keys.
3. **Step 3 — Clean:** Standardize text formatting, deduplicate records, filter out invalid rows (zero-passenger flights), and replace numerical error sentinels (`-999`) with `NaN`.
4. **Step 4 — Combine:** Perform a left join on airline codes to attach airline names without altering total row counts.
5. **Step 5 — Explore:** Analyze punctuality by airline, evaluate route delays with sample-size thresholds, measure distance-delay correlations, and evaluate extreme delays.
6. **Step 6 — Write Up & Findings:** Summarize business findings using the **What / So What / Caveat** framework and document cleaning decisions.

---

## Key Questions Answered

* **Usable Flights:** Total flights retained after filtering invalid logs (`passengers == 0`) and removing duplicate records.
* **Most Punctual Airline:** Evaluated using **On-Time Performance (OTP %)** (delays $\le$ 15 minutes) and **Median Delay** to prevent extreme outliers/storms from distorting rankings.
* **Worst Delay Routes:** Evaluated on routes with a minimum sample size ($N \ge 30$) to prevent single-flight anomalies from skewing results.
* **Distance vs. Delay:** Correlation analysis measuring whether longer flight distances tend to have higher arrival delays.
* **Extreme Delays:** Assessment of severe operational delay outliers versus recording failures.

---

## Visualizations Included

* **Chart 1:** Airline On-Time Performance (OTP %)
* **Chart 2:** Top 10 Worst Delayed Routes (Min 30 Flights)
* **Chart 3:** Scatter Plot of Flight Distance vs. Arrival Delay
* **Chart 4:** Delay Duration Frequency Distribution

---
# Project 2


# Heart Disease Prediction Using Logistic Regression

## Project Overview

This project uses **Machine Learning and Logistic Regression** to predict the 10-year risk of coronary heart disease (CHD) based on patient health information.

The model analyzes medical attributes such as age, gender, blood pressure, cholesterol, smoking habits, diabetes, and other health-related factors to estimate the probability of developing coronary heart disease within ten years.

## Objectives

- Understand and analyze the heart disease dataset.
- Perform data cleaning and preprocessing.
- Handle missing values and duplicate records.
- Explore important features using data visualization.
- Train a Logistic Regression classification model.
- Evaluate model performance using classification metrics.
- Predict the probability of heart disease for new records.

## Dataset Information

**Dataset:** Heart Disease Prediction Using Logistic Regression

**Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/dileep070/heart-disease-prediction-using-logistic-regression)

- Total records: 4,238
- Total columns: 16
- Target variable: `TenYearCHD`

### Features Used

| Feature | Description |
|---|---|
| male | Gender |
| age | Age of the patient |
| education | Education level |
| currentSmoker | Current smoking status |
| cigsPerDay | Cigarettes smoked per day |
| BPMeds | Blood pressure medication |
| prevalentStroke | Previous stroke history |
| prevalentHyp | Hypertension status |
| diabetes | Diabetes status |
| totChol | Total cholesterol |
| sysBP | Systolic blood pressure |
| diaBP | Diastolic blood pressure |
| BMI | Body Mass Index |
| heartRate | Heart rate |
| glucose | Glucose level |

**Target variable:**
- `TenYearCHD = 1`: CHD event within ten years.
- `TenYearCHD = 0`: No recorded CHD event within ten years.

## Technologies Used

- Python
- Google Colab
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Project Workflow

1. Import the required Python libraries.
2. Upload

