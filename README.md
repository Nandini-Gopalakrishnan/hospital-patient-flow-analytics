🏥 **Hospital Patient Flow & Medical Services Analytics**

📌 **Project Overview:**

This project focuses on analyzing hospital operations to improve patient flow, optimize resource utilization, and enhance healthcare service delivery.

By integrating and analyzing multiple datasets, the project provides actionable insights into patient admissions, treatment outcomes, doctor performance, and billing efficiency.


🎯 **Problem Statement:**

The objective of this project is to analyze operational efficiency and patient care metrics across hospital departments.

Key focus areas include:

  1. Patient admission and discharge trends
  2. Treatment outcomes and recovery rates
  3. Doctor performance evaluation
  4. Resource utilization across departments

The goal is to identify bottlenecks, improve decision-making, and enhance overall hospital performance.


🏥 **Business Use Cases:**

  1. **Departmental Efficiency Optimization** - Analyze length of stay, treatment success rates, and patient flow bottlenecks
      
  2. **Doctor Performance Evaluation** - Identify top-performing doctors based on recovery rate, patient volume, and efficiency
    
  3. **Patient Segmentation** - Segment patients based on demographics, admission patterns, and risk levels


🧩 **Dataset Description:**

The project uses three datasets:

1. **patient_admissions.csv** – Contains patient IDs, admission/discharge dates, age, gender,
diagnosis, and department info.
2. **doctor_profiles.csv** – Includes doctor ID, specialization, experience, performance rating, and
assigned department.
3. **treatment_records.csv** – Tracks treatment ID, patient ID, doctor ID, treatment type, date,
success flag, and cost.


⚙️ **Tools & Technologies:**
  1. **Python (Pandas)** – Data partitioning to import easily in MySQL
  2. **MySQL** – Data Cleaning, Data integration, transformation, and advanced analytics
  3. **Power BI** – Data visualization and dashboard creation
  4. **Excel & PowerPoint** - Business Report creation, Insight Presentation


🔧 **Data Preparation:**
  1. Merged partitioned datasets using SQL (UNION ALL)
  2. Standardized inconsistent doctor_id formats
  3. Converted date fields into proper formats
  4. Removed invalid records and duplicates
  5. Created derived features such as Age Groups


📊 **SQL Analysis:**

📁 **SQL Files -** sql/analysis_queries.sql

Performed advanced SQL analysis including:

**A. Basic Aggregation**
- Calculate the number of admissions per department per month.
- Find the average treatment cost per department.

**B. Join Operations**
- Join admissions with doctors to identify top performing doctors by department.
- Join treatments with patient data to evaluate recovery rate by age group.

**C. Window Functions**
- Calculate moving average of daily admissions (7-day MA).
- Rank doctors by number of successful treatments per month.

**D. Percentiles and Median**
- Calculate 25th, 50th, and 75th percentile of treatment costs per treatment type.
- Find the median length of stay per department.

**E. Grouping and Case Statements**
- Group patients into 'High-Risk', 'Moderate-Risk', 'Low-Risk' based on comorbidity count.
- Find admission trends by weekday and weekend.

**F. Complex Joins and Subqueries**
- Find doctors whose patients had recovery rate above the departmental average.
- Identify patients who visited more than 3 departments in a year.

**G. Date Functions and YOY**
- Calculate year-over-year change in total treatments administered.
- Find the month with the highest treatment cost.

**H. Retention and Follow-up Analysis**
- Find patients readmitted within 30 days of discharge.
- Calculate average interval between admissions for chronic patients.


📈 **Power BI Dashboard:**

An interactive dashboard was created to visualize key metrics and insights.

📁 **File:** dashboards/Dashboard.pbix

📌 **Key Visualizations:**

    1. KPI Summary Metrics:
       Displays key indicators including Total Doctors, Total Patients Treated, Chronic Patients Count, and Readmission Rate (%)
    2. Patient Outcomes Analysis:
       Recovery rate segmented by age group and analysis of 30-day revisit frequency across age groups and gender
    3. Financial Performance Insights:
       Average treatment cost across departments and year-wise trend of total treatments to monitor growth patterns
    4. Doctor Performance & Treatment Effectiveness:
       Distribution of treatment types, average success rate by department, and department-wise count of top-performing doctors with successful treatments

📷 **Dashboard Preview:**



📊 **Reports & Insights:**

📁 reports/sql_results_insights.xlsx
→ Query-wise results with key insights

📁 reports/hospital-insights-presentation.pptx
→ Visual summary of findings with charts and business insights


🚀 **Business Impact:**
  1. Improved visibility into hospital operations
  2. Identification of inefficiencies and bottlenecks
  3. Data-driven decision-making for resource allocation
  4. Enhanced patient care and operational performance
