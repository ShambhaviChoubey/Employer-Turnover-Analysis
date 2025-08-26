markdown
# HR Analytics & Employee Turnover Analysis

## 📊 Project Overview
Comprehensive analysis of company HR data to uncover insights about employee demographics, distribution, and turnover patterns. Final deliverable is an interactive Power BI dashboard for strategic HR decision-making.

## 📁 Data Source
- `Human Resources.csv` - Raw employee dataset

## 🛠 Tools Used
- **SQL** - Data cleaning and analysis
- **Power BI** - Data visualization

## 🧹 Data Cleaning
sql
-- Sample cleaning code
UPDATE hr 
SET termdate = CASE 
    WHEN termdate IS NULL OR termdate = '' THEN NULL 
    ELSE STR_TO_DATE(termdate, '%Y-%m-%d %H:%i:%s UTC') 
END;

ALTER TABLE hr ADD COLUMN age INT;
UPDATE hr SET age = TIMESTAMPDIFF(YEAR, birthdate, CURDATE());


## 🔍 Key Analysis Questions
1. Gender breakdown of employees
2. Race/ethnicity distribution
3. Age demographics
4. HQ vs remote workers
5. Average tenure of terminated employees
6. Departmental gender distribution
7. Job title distribution
8. Department turnover rates
9. State-wise employee distribution
10. Hiring/termination trends over time

## 📈 Dashboard Features
- Employee distribution metrics
- Demographic visualizations
- Turnover analysis
- Departmental insights
- Interactive filters

## 📋 Key Findings
- Male employees outnumber female employees
- White employees represent largest racial group
- 25-34 age group is largest cohort
- Marketing has highest turnover rate
- Ohio has highest employee concentration
- Positive net employee growth trend

## ⚠ Limitations
- Excluded records with negative ages
- Only employees 18+ considered
- Future termination dates excluded from analysis

## 🚀 Implementation
1. Import CSV to SQL database
2. Execute cleaning queries
3. Run analysis queries
4. Connect Power BI to database
5. Build visualizations

## 📂 Project Files
- `Human Resources.csv` - Raw data
- `Question+Data cleaning.sql` - SQL cleaning script
- `HR Data Questions.sql` - Analysis queries
- `HR Employee Report.pbix` - Power BI dashboard
- `HR analytics.pdf` - Dashboard preview
- `ICONS.rar` - Visual assets
