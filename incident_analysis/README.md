# Incident Analysis

## 🎯 Objective
Analyze NYC public school safety data in **Google Sheets** to understand incident patterns, identify borough-level trends, and detect possible data anomalies.

---

## 🧩 Tasks
- Upload and clean the CSV dataset in Google Sheets  
- Clean column names:
  - Convert to lowercase  
  - Replace spaces with underscores (`_`)  
  - Remove special characters  
- Explore and answer:
  - How many total rows are there?  
  - How many unique schools are listed?  
  - What is the most frequent incident type?  
  - What % of incidents occurred in the Bronx?  
- Identify 1–2 interesting findings or anomalies.

---

## 🧠 Process
All steps were performed directly in **Google Sheets**:

1. **Data Cleaning**
   - Standardized column names with text functions (`LOWER`, `SUBSTITUTE`, `REGEXREPLACE`).  
   - Filled missing borough values manually where possible, based on identical building codes or addresses.
   - Replaced values to keep data standardized.
   - Verified all numeric columns were recognized as numbers and handled blank cells as zeros for accurate calculations.  

2. **Exploration**
   - Created a helper column summing all incident types per school.  
   - Used `SUMIF` to total incidents per borough.  
   - Calculated the percentage of incidents in the Bronx.  
   - Built a pivot table to compare borough-level totals and incident types.  

---

## 📊 Key Findings
- **Total Rows:** 6,309  
- **Most Frequent Incident Type:** *NoCrim N* with 11,772 total incidents.  
- **Bronx share:** 28.30% in the original dataset (before cleaning).  
- Some schools reported **zero incidents**, while one reached **130 incidents**, showing wide variation.  
- **Brooklyn** had the largest overall number of incidents (~30%).  
- Some records shared the same building code but had different DBNs — representing multiple schools within the same facility.  
- Missing DBNs were marked; empty borough values were filled when other identifiers clearly indicated location.

---

## 🧰 Tools & Functions Used
- **Google Sheets**
  - `LOWER`, `SUBSTITUTE`, `REGEXREPLACE`, `SUMIF`, `COUNTUNIQUE`, `COUNTA`, `IF`
  - Pivot tables for aggregation

---

## 💬 Summary
This analysis provided a clear overview of incident distribution across NYC schools and boroughs using **Google Sheets only**.  
By cleaning, validating, and enriching the dataset manually, data quality was improved while maintaining all relevant records for forward analysis.
