# School Directory Exploration

## 🎯 Objective
The goal of this analysis was to explore the NYC high school directory dataset using **Pandas** in a Jupyter Notebook.  
The task focused on cleaning, filtering, grouping, and visualizing the data to uncover patterns across different boroughs, particularly regarding the number of schools, student distribution, and grade spans.

---

## 🧩 Tasks

1. Load the dataset using pandas  
2. Clean the column names (lowercase, replace spaces with `_`, remove special characters)  
3. Filter the dataset to include only schools located in **Brooklyn**  
4. Answer:
   - How many total unique schools are in Brooklyn?  
   - How many schools in Brooklyn offer Grade 9 entry?  
5. Group and summarize:
   - Count of schools per borough  
   - Average number of students per borough  
   - Summary statistics of `grade_span_max` by borough  
6. Visualize:
   - Bar chart showing number of schools per borough  
7. Write 2–3 insights based on findings

---

## 🧠 Process

### 1. **Data Cleaning**
- Column names were standardized using `str.lower()`, `str.replace()`, and regex to remove special characters.  
- Borough names were normalized to lowercase for consistent filtering.  
- `grade_span_min` and `grade_span_max` columns were converted to numeric types to enable range-based comparisons.  

### 2. **Exploration**
- Filtered data to include only Brooklyn schools.  
- Counted total unique schools using `.nunique()` on the `dbn` column (the unique school identifier).  
- Identified Brooklyn schools offering Grade 9 entry by checking if **9 lies within each school’s grade range** (`grade_span_min <= 9 <= grade_span_max`).  
- Grouped by borough to calculate:
  - Number of unique schools per borough  
  - Average number of students per borough  
  - Descriptive statistics for `grade_span_max`  

### 3. **Visualization**
- Created a **bar chart** showing the number of schools per borough.  
- Added axis labels, titles, and rotation for better readability.

---

## 📊 Key Findings

- **Staten Island** has the **highest average number of students (1,847.5)**, even though it only has 10 schools.  
- **The Bronx** has the **second-highest number of schools (118)** but the **lowest average number of students (490.4)**, suggesting smaller school sizes.  
- All schools in **Staten Island** offer education up to **Grade 12**, while other boroughs have more diverse grade spans (some ending earlier).  
- **Brooklyn** has the largest number of unique schools overall, indicating a more extensive and varied education network.

---

## 🧰 Tools & Features Used

- **Python**
- **Pandas** for data cleaning, grouping, and summarization  
- **Matplotlib** for visualization  
- **Jupyter Notebook** for analysis and presentation  

---

## 💬 Summary
This exercise provided hands-on experience in data cleaning, filtering, and exploratory data analysis using Pandas.  
It highlighted how grouping and descriptive statistics can uncover differences across boroughs, such as school sizes and grade coverage.  
The visualization helped clearly compare boroughs, reinforcing the value of combining data analysis with simple but effective visual storytelling.
