This folder contains all **SQL scripts** used for data cleaning, transformation, and analysis in the **Hospital Patient Flow & Medical Services Analytics** project.

📂 **Files Included:**

**1. Data Cleaning & Importing Queries**

This document includes SQL queries used to prepare raw datasets for analysis:

**Data Integration**

Combined partitioned datasets (D1–D5, P1–P5, T1–T5) using UNION ALL to create unified tables:
  DOCTOR_PROFILES
  PATIENT_ADMISSIONS
  TREATMENT_RECORDS
  
**Data Standardization**

Corrected inconsistent DOCTOR_ID formats (e.g., D01001 → D1001) to ensure consistency across tables
Date Formatting & Conversion
Converted string-based date columns into proper DATE format using STR_TO_DATE
Standardized:
  ADMISSION_DATE
  DISCHARGE_DATE
  TREATMENT_DATE
  
**Data Cleaning**

Removed duplicate/irrelevant columns (e.g., redundant DEPARTMENT column)
Eliminated invalid records (e.g., patients with AGE = 0)

**Feature Engineering**

Created derived column:
AGE_GROUP (e.g., 20–29, 30–39) for demographic analysis

**2. Analytical SQL Queries:**

This document contains SQL queries developed to answer key business problems:

  1. Department-wise admissions and treatment cost analysis
  2. Doctor performance evaluation using joins
  3. Moving averages and ranking using window functions
  4. Treatment cost distribution using percentiles and median
  5. Patient risk segmentation using CASE statements
  6. Identification of high-performing doctors using subqueries
  7. Year-over-year treatment trend analysis
  8. Patient readmission and retention analysis

**⚙️ Tools Used**

MySQL Workbench
SQL (Joins, Aggregations, Window Functions, Subqueries, Data Cleaning)

**📌 Note**

The cleaned and transformed datasets created using these queries were used for downstream analysis and visualization in Power BI, enabling insights into hospital efficiency, patient outcomes, and operational performance.
