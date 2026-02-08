# Analysing Employee Attrition using Excel 

## 🚀 Project Overview

This project analyzes employee attrition patterns using an HR dataset, with the goal of identifying key drivers behind employee turnover and translating them into actionable business insights.

The dashboard was built entirely in **Microsoft Excel** using **Power Query**, **Power Pivot**, **Pivot Tables**, and **DAX**, following a dimensional modeling approach (star schema).  

## [Report](https://github.com/Trevor20/Excel-Portfolio/blob/main/Project%203%20-%20HR%20Attrition%20Analysis/Attrition_Analysis.png)

## 🧠 Business Problem

Employee attrition is costly and time consuming, especially when it disproportionately affects specific roles, experience levels, or departments.  

The organization wants to understand:
- Which employee segments are most likely to leave
- Whether tenure, satisfaction, compensation, or commute distance influence attrition
- Where targeted retention strategies would have the highest impact

## 🎯 Objectives 

1. Analyze overall attrition rate and key employee segments driving turnover
2. Identify patterns across tenure, department, job level, salary slabs, and distance from office
3. Compare satisfaction levels of employees who stayed vs those who left
4. Build a clear, decision-ready dashboard for HR and leadership stakeholders

## 📖 Dataset

The dataset includes information on:
- Demographics - Age, gender, education, distance from office, designation
- Performance - For Employee and for employer 
- Company characteristics - Monthly compensation, years stayed with manager, department
- Attrition - Who stayed and who left

...and more

The data is provided in CSV format. The dataset has 1740 records.

## 🧰 Tools Used
- **Microsoft Excel**
  - Power Query - For ETL & data transformations
  - Power Pivot - For creating data model & star schema
  - Pivot Tables & Pivot Charts - For creating the dashboard graphs
  - DAX - For basic measures & KPIs
  - Camera Tool - For KPI cards
- **Data Source**
  - Public HR Attrition dataset from Kaggle

## 📂 Dataset Structure

A CSV table was connected and imported into Excel. It includes, among other fields, the following primary columns:

### 3. HR_Analytics
| Column                    | Description                                    |
|---------------------------|------------------------------------------------|
| EmpID                     | Unique Employee Id                             |
| Age                       | Employee age                                   |
| AgeGroup                  | Age group of the employee                      |
| Attrition                 | Whether the employee left (Yes/No)             |
| BusinessTravel            | Amount of travel needed for the job            |
| DailyRate(AED)            | Daily compensation for the employee            |
| Department                | Department the employee works in               |
| DistanceFromHome(KM)      | Distance from office to home                   |
| Education                 | Level of education of the employee             |
| EducationField            | Education field                                |
| EnvironmentSatisfaction   | Employee satisfaction of the work environment  |
| Gender                    | Employee Gender                                |
| JobInvolvement            | Level of involvment to the job                 |
| JobRole                   | Job Title                                      |
| JobSatisfaction           | How satisfied is the employee with the job     |
| MaritalStatus             | Marital status                                 |
| MonthlyIncome(AED)        | Monthly compensation                           |
| SalarySlab                | Salary slab of the employee                    |
| PerformanceRating         | Employees performance rating                   |
| RelationshipSatisfaction  | How satisfied is the employee with the manager |
| WorkLifeBalance           | Level of work life balance of the employee     |

## 🔍 Key Business Questions Answered

1. What is the overall attrition rate, and the median tenure of people who left?
2. Which job level and department contains the highest attrition?
3. How does attrition vary across different tenures?
4. How does satisfaction levels differ among those who staysed vs those who left?
5. Does attrition depend on salary slabs and years of experience of the employee?
6. Does attrition differ as distance from office increases?

## ➡️ Project Approach

### 1. Data Import
1. Imported the raw HR dataset using Excel's **Get Data**
2. Loaded the data into **Power Query** for transformation and modeling

### 2. Data Modelling & Transformation in Power Query
1. Started with a single fact table and intentionally **split it into 6 tables** to:
   - Increase modeling complexity
   - Improve clarity and analytical flexibility
2. Several columns (e.g., Education, Work-Life Balance, Performance Rating) were encoded as numeric values (1–5) without definitions. Created **dimension tables** to map these numeric codes to meaningful labels  
3. For **Satisfaction Rating**, multiple rating columns existed:
   - Created one shared Satisfaction dimension
   - Connected it to all three rating columns (1 active relationship + 2 inactive)
4. Loaded the cleaned tables into Power Pivot and built a **star schema**

### 3. Measures & Calculations in Power Pivot using DAX
1. Created basic DAX measures such as:
   - Overall attrition rate
   - Attrition by department
   - Maximum attrition across job levels
2. Focused on clarity and correctness rather than overly complex DAX

### 4. Dashboard Development in Excel
1. Built **Pivot Tables** from the data model
2. Created charts directly from Pivot Tables to ensure dynamic filtering
3. Used Excel’s **Camera Tool** to design KPI cards for:
   - Total employees
   - Attrition %
   - Median tenure of employees who left
   - Highest-attrition department and job level

## 🏆 Final Insights

### Employee Experience Drivers
- 👱 **Entry-level employees** experience nearly **2× higher attrition** compared to other job levels
- 📈 Employees who left reported **lower satisfaction scores** than those who stayed
- 🦾 Attrition is highest within the **first year**, and steadily declines with tenure

### Company Structure Drivers
- 🏗️ **R&D** shows the highest department-level attrition
- 🏢 Employees earning **<5k salary with low experience** show the highest churn
- 🛏️ Attrition rises significantly once commute distance exceeds **13 km**, suggesting travel fatigue as a key factor

## 🪪 Key Recommendations
- ⬆️ Strengthen **onboarding and mentorship** programs to improve first-year retention
- 💠 Address **expectation gaps** by incorporating exit interviews and external reviews (e.g., Glassdoor)
- 🚗 Consider **flexible work options or commute support** for employees with long travel distances
