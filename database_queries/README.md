# Database Queries

## 🎯 Objective
The goal of this task was to connect to a PostgreSQL database using **SQLAlchemy** and **Pandas**, query the NYC school-related tables, and perform data analysis directly from SQL within a Jupyter Notebook.  
The main objectives were to practice database querying, joining tables, and identifying insights from the school data, especially regarding English Language Learners (ELL) and Special Needs students.

---

## 🧩 Tasks

1. Connect to the PostgreSQL database using credentials provided for the training environment.  
2. Use `pandas.read_sql()` to run SQL queries directly from Python.  
3. Answer the following questions:

   - **Q1:** How many unique schools are there in each borough?  
   - **Q2:** What is the average percentage of English Language Learners (ELL) per borough?  
   - **Q3:** Which are the top 3 schools in each borough with the highest percentage of Special Education students (*sped_percent*)?

4. Summarize and interpret the results in Markdown.

---

## 🧠 Process

### 1. **Database Connection**
- The connection was established using **SQLAlchemy** with the PostgreSQL driver `psycopg2`.  
- Connection details were stored as variables and combined into an engine string.  
- Queries were executed using `pandas.read_sql()` for smooth integration with DataFrames.

### 2. **Data Exploration**
- Each question was answered using SQL queries written directly in the notebook.  
- Borough-level aggregations were done with `GROUP BY`.  
- To avoid counting duplicate schools, **`COUNT(DISTINCT dbn)`** was used instead of `COUNT(*)`.  
- Joins were applied between `school_directory` and `school_demographics` tables when borough information was needed.

### 3. **Dealing with Missing Values**
- During the ELL and Special Needs analyses, it was found that the *school_demographics* table only contains data for **Manhattan**, while all other boroughs have missing values.  
- The attempt to use **number_programs** as a proxy for ELL coverage was discarded, since that column includes all academic programs, not only ELL-related ones.

---

## 📊 Key Findings

- **Q1:** The query was adjusted to count **unique schools** per borough using `COUNT(DISTINCT dbn)`.  
- **Q2 & Q3:** Both analyses returned results only for **Manhattan**, revealing significant data gaps in the *school_demographics* table.  
- This indicates that the dataset is **incomplete or poorly maintained** for certain metrics such as `ell_percent` and `sped_percent`.  
- Therefore, borough-level comparisons are **not reliable**, and even the Manhattan results should be treated with caution due to possible underreporting.

---

## 💬 Insights

- The *school_demographics* table lacks consistency, as it only reports values for one borough.  
- The missing data suggests that further analysis would require **alternative data sources** or a **data enrichment step**.  
- It also shows how crucial data validation is before drawing conclusions in an analytical project.  
- Using *high_school_directory* as a complementary source could provide better borough coverage for future analysis.

---

## 🧰 Tools & Features Used

- **PostgreSQL**
- **SQLAlchemy** and **psycopg2** for database connection  
- **Pandas** for executing SQL and manipulating results  
- **Jupyter Notebook** for combining queries, outputs, and interpretations  

---

## 💬 Summary
This task demonstrated how to connect Python to a relational database and execute SQL queries within a Jupyter environment.  
It emphasized not only querying and aggregation but also the importance of **data quality awareness**.  
Even though some results were incomplete due to missing data, identifying and explaining these limitations shows strong analytical thinking and real-world problem-solving skills.
