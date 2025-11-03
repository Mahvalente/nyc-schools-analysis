# 🗽 NYC Schools Analysis

This project was created during a data analytics internship, with a focus on data cleaning, exploratory analysis, and database management.  
It explores different datasets related to New York City public schools, aiming to uncover insights about student demographics, safety incidents, and school performance through both Python and SQL.

---

## Project Overview

The project is divided into four main parts:

1. **Incident Analysis** – Exploring school safety data and identifying borough-level patterns.  
2. **School Directory Exploration** – Examining demographic and enrollment data for NYC schools.  
3. **Database Queries** – Running SQL queries through Python to extract and analyze specific insights.  
4. **Database Population** – Cleaning data and preparing it for upload into a PostgreSQL database.

---

## Key Skills & Tools

- **Languages:** Python, SQL  
- **Libraries:** pandas, matplotlib, sqlalchemy, psycopg2  
- **Techniques:** Data Cleaning, EDA, Data Aggregation, SQL Integration  
- **Tools:** Jupyter Notebook, GitHub  

---

## Main Insights

### Incident Analysis  
- The **majority of reported incidents** were categorized as *No Crime* or *Other*, which may reflect either underreporting or classification inconsistencies.  
- **Brooklyn** accounted for roughly **30% of all incidents**, the highest share across boroughs.  
- Some schools reported **over 200 incidents**, while others reported none — indicating large disparities in reporting behavior or school environment.  
- By examining borough-level patterns, it became clear that **school size and local context** may influence the number of incidents.

### School Directory Exploration  
- **Staten Island** had the highest *average number of students per school* (≈ 1847), despite having far fewer schools than Brooklyn or the Bronx.  
- **Bronx** schools had the lowest average enrollment but one of the **highest densities of schools**, suggesting smaller institutions distributed across neighborhoods.  
- The dataset contained **missing and inconsistent values** (e.g., enrollment data or grade spans), which required targeted cleaning and type correction before aggregation.  
- Exploratory statistics and visualizations helped confirm that borough-level educational resources are **unevenly distributed**.

### Database Queries (PostgreSQL)
- Using PostgreSQL queries, we were able to join and analyze datasets efficiently — for example, linking **demographic** and **incident data** to explore potential relationships.  
- We identified that some boroughs with **higher student populations** did not necessarily have proportionally more incidents, suggesting that **school culture or local policies** may play a role.  
- Aggregate queries highlighted differences in **ELL (English Language Learner)** program distribution and **special needs support** across boroughs, though incomplete data limited full precision.

### Database Population  
- The cleaning process included removing invalid scores (e.g., negative SAT values), converting percentages to decimals, and standardizing column names.  
- Final cleaned data was uploaded into a PostgreSQL database for reproducibility and further querying.  
- Data validation ensured that all numerical and categorical columns aligned with expected formats.

---

## Repository Structure

📁 nyc-schools-analysis/ \
├── incident_analysis/ \
│   └── README.md \
│   └── data/ \
|       └── placeholder \
├── school_directory_exploration/ \
│   └── day2_analysis.ipynb \
│   └── visuals/ \
│   └── README.md \
├── database_queries/ \
│   └── day3_sql_analysis.ipynb \
│   └── README.md \
├── database_population/ \
|   └── data/ \
|       └── sat-results.csv \
|       └── cleaned_sat-results.csv \
│   └── sat_modeling.ipynb \
│   └── README.md \
├── requirements.txt \
└── README.md           










✨ Author: Marcella Valente Ralser
