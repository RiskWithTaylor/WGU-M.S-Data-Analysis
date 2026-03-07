# 📊 Data Preparation and Exploration – Employee Turnover Dataset

## 👨‍💻 Author
**Taylor Wilkerson**  
B.S. IT Management – Western Governors University  

**Areas of Interest**
- Data Analytics
- Financial Technology
- Risk Analytics

---

# 📌 Project Overview

This project focuses on **data profiling, preparation, and cleaning** of an employee turnover dataset used by a multinational technology company.

Employee turnover is a major operational cost for organizations. Replacing an employee can cost **6–9 months of the employee’s salary**, making workforce analytics critical for improving retention strategies.

The objective of this project was to:

- Profile the dataset structure
- Identify data quality issues
- Implement Python-based data cleaning techniques
- Prepare the dataset for future analytics and modeling

---

# 📂 Dataset Overview

| Metric | Value |
|------|------|
| Records | 10,199 |
| Variables | 16 |
| Dataset Type | Workforce / HR dataset |

The dataset contains employee demographic, employment, and compensation information used to analyze turnover patterns.

---

# 🧠 Skills Demonstrated

- Data Profiling
- Data Cleaning
- Data Quality Assessment
- Python Data Analysis
- Pandas Data Manipulation
- Outlier Detection
- Data Normalization
- Data Preparation for Analytics

---

# 🔧 Tools and Technologies

| Tool | Purpose |
|-----|-----|
| Python | Data analysis |
| Pandas | Data manipulation |
| NumPy | Numerical analysis |
| JupyterLab | Development environment |
| Excel | Dataset storage |

---

# 📊 Data Profiling Process

The dataset was first inspected using Python and pandas to understand its structure.

```python
import pandas as pd

df = pd.read_excel("Employee Turnover Dataset.xlsx")

print("Rows:", df.shape[0])
print("Columns:", df.shape[1])
print(df.columns.tolist())
```
This inspection confirmed the number of records and variables in the dataset.

Sample values were also inspected to understand real entries across each column.
```python
for col in df.columns:
    print(col, ":", df[col].dropna().unique()[:3])
```
This helped identify representative values for each variable.
- 

# ⚠️ Data Quality Issues Identified

Five common data quality issues were identified during the inspection process.
- - -
## Duplicate Records

Duplicate employee records were detected.

- 99 duplicate rows were identified

- Duplicate *EmployeeNumber* values confirmed repeated employee entries

Duplicate records can distort analytics by artificially inflating counts and trends.

---
# Missing Values

##  Missing values were concentrated in a few variables.

| Variable                     | Missing Values |
| ---------------------------- | -------------- |
| TextMessageOptIn             | 2,266          |
| AnnualProfessionalDevHrs     | 1,969          |
| NumCompaniesPreviouslyWorked | 665            |

Total missing cells across the dataset: 4,900
---

# Inconsistent Categorical Values

## Several categorical variables had inconsistent formatting.

## Example:

```
InformationTechnology
Information Technology
Information_Technology
```
---
# This issue occurred in variables such as:

- JobRoleArea

- PaycheckMethod

## Inconsistent labels can split a single category into multiple groups.
---
# Formatting Errors

## Text formatting inconsistencies were detected such as:

```
DirectDeposit
Direct Deposit
Direct_Deposit
```
### These inconsistencies can affect grouping and summary statistics.

# Extreme Outliers

## Outliers were detected in several numeric fields.

| Variable                | Issue              |
| ----------------------- | ------------------ |
| AnnualSalary            | 544 outliers       |
| DrivingCommuterDistance | 245 outliers       |
| Salary ≤ 0              | 57 invalid entries |

### Extreme values can significantly distort statistical analysis.
---

## 🧹 Data Cleaning Techniques

### Several Python-based techniques were used to correct the identified issues.
---

# Removing Duplicate Records

## Duplicate rows were removed using:

```python

df = df.drop_duplicates()
```
### This ensured each employee record remained unique.

---
# Handling Missing Values

## Two strategies were implemented.

| Data Type   | Method                 |
| ----------- | ---------------------- |
| Numerical   | Median imputation      |
| Categorical | Replace with "Unknown" |

### Median imputation was chosen because it is robust to extreme values.
---

# Standardizing Categorical Data

## Categorical values were normalized by:

- Removing whitespace

- Replacing underscores with spaces

- Converting text to lowercase

- Mapping variations to canonical labels

Example transformation:

```
Information_Technology → Information Technology
```
--- 

# Fixing Invalid Numeric Values

## Invalid salary values (< = 0) were replaced with missing values before imputation.
--- 

# Outlier Treatment

## Outliers were detected using the Interquartile Range (IQR) method.

## Values outside the bounds:

```
Q1 − 1.5 × IQR
Q3 + 1.5 × IQR
```
### were capped to reduce their influence on the dataset.

----

# 📈 Advantages of the Cleaning Approach
## Data Preservation

Instead of removing records, imputation and outlier capping preserved all 10,199 records, maintaining statistical power.

## Improved Category Consistency

 Standardizing categorical labels ensures:

- accurate grouping

- correct frequency counts

- improved modeling performance

---

# ⚠️ Limitations

## Median Imputation

Replacing missing values with the median may mask meaningful patterns in missing data.

## Outlier Capping

Extreme but legitimate values may be compressed, potentially reducing insight into rare cases.
- - - 

# 🚀 Future Improvements

## Potential improvements to the project include:

- predictive turnover modeling

- machine learning classification

- workforce analytics dashboards

- anomaly detection techniques

- deeper feature engineering

- - - 

# ⭐ Key Takeaway

## Data preparation and exploration are essential steps in the analytics process.
## Clean and well-structured data allows organizations to perform reliable analysis, build predictive models, and make informed business decisions.
