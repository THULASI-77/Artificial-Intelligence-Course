# Flight Delays Analysis (Day 21 Project)

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

