# Database Population

## 🎯 Objective
The goal of this task was to integrate a cleaned SAT results dataset into a PostgreSQL database using **SQLAlchemy** and **Pandas**.  
This process focused on connecting to the database, preparing the dataset for insertion, ensuring schema compatibility, and verifying data integrity after the load.

---

## 🧩 Tasks

1. Load the SAT results dataset using **Pandas**.  
2. Clean and standardize all column names to `snake_case`.  
3. Format the `school_name` column (title case, remove extra spaces).  
4. Remove duplicated rows and a typo column (`sat_critical_readng_avg_score`).  
5. Clean percentage values and convert them into decimal form.  
6. Convert all relevant columns to numeric data types.  
7. Detect outliers and validate score ranges for SAT sections.

---

## 🧠 Process

### 1. **Data Cleaning**
- Column names were transformed into `snake_case` using Pandas string methods.  
- Duplicates were removed based on the `dbn` column to ensure unique schools.  
- The duplicated typo column `SAT Critical Readng Avg. Score` was dropped.  
- Placeholder strings (`'s'`, `'N/A'`, `'None'`, empty cells) were replaced with `NaN`.  
- All numeric fields (including SAT scores and number of test takers) were converted to proper numeric types.  
- The column `pct_students_tested` was cleaned by removing the `%` symbol and converting it to a decimal (e.g., `78% → 0.78`).  
- Outliers were handled by filtering values outside the valid SAT score range (200–800).

### 2. **Feature Engineering**
- Added `avg_sat_score` for the average SAT performance per school.

### 3. **Database Connection**
- The connection was established using **SQLAlchemy** with a secure PostgreSQL URL:  

## 💬 Insights
- Cleaning and validation were necessary due to inconsistent raw data.
- Outlier detection showed how data entry errors can distort analyses if not corrected.
- After preprocessing, the dataset was standardized and suitable for integration into a PostgreSQL table.
- This task reinforced how crucial data quality checks are before the database population step.

⸻

## 🧰 Tools
- Python (Pandas, NumPy) for data cleaning, formatting, and validation
- Jupyter Notebook for documenting and executing the process
- SQLAlchemy for database connectivity setup

⸻

## 💬 Summary

This task focused on preparing a raw SAT dataset for integration into a relational database. \
The workflow included cleaning column names, removing duplicates, converting data types, and detecting invalid score ranges. 
