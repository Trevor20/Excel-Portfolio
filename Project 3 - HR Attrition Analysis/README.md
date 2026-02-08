# In Progress - Analysing Employee Attrition using Excel 

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
- Company characteristics - Monthly & overtime compensation, years stayed with manager
- Attrition: Who stayed, who left and when they left
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

## 📂 Dataset Structure - In Progress

The following CSV tables were connected and imported into Excel

### 3. HR_Analytics
| Column                          | Description                                   |
|---------------------------------|-----------------------------------------------|
| Id                              | Unique Employee Id                            |
| Reason for absence              | Reason Id                                     |
| Month of Absence                | Month the employee was absent                 |
| Day of the week                 | Day the employee was absent                   |
| Seasons                         | Source had no info, data is ambiguous         |
| Transportation expense          | Cost to travel from home to office            |
| Distance From residence to work | Distance to work                              |
| Service time                    | Source had no info, data is ambiguous         |
| Age                             | Age of employee                               |
| Work load average/day           | Source had no info, data is ambiguous         |
| Hit target                      | Source had no info, data is ambiguous         |
| Disciplinary failure            | Whether employee had performance issues (0/1) |
| Education                       | No of education degrees                       |
| Son                             | No of Children                                |
| Social Drinker                  | Whether the employee drinks (1/0)             |
| Social Smoker                   | Whether the employee smokes (1/0)             |
| Pet                             | No of pets                                    |
| Weight                          | Employee weight                               |
| Height                          | Employee height                               |
| Body mass index                 | Division of weight by height. Also called BMI |
| Absenteeism time in hours       | Total hours the employee was absent           |

## 🔍 Key Business Questions Answered - In Progress

1. Who are the healthy individuals with low absenteeism eligible for a health bonus program?
2. Calculate wage increase for non-smokers. Budget is $983,221.
3. How does absenteeism vary accross weekdays and months?
4. What are the top reasons employees take leave?
5. Is there a correlatiion between age or compensation and absent hours?
6. Does lifestyle(Smoking, drinking, education, children, pets) influence absenteeism?
7. Does having a disciplinary failure impact hours absent?
8. Does BMI impact absenteeism?

## ➡️ Project Approach

### 1. Data Import
1. Imported the raw HR dataset using Excel's **Get Data**
2. Loaded the data into **Power Query** for transformation and modeling

### 2. Data Modelling & Transformation in Power Query
1. Started with a single fact table and intentionally **split it into 6 tables** to:
   - Increase modeling complexity
   - Improve clarity and analytical flexibility
2. Several columns (e.g., Education, Work-Life Balance, Performance Rating) were encoded as numeric values (1–5) without definitions. Created **dimension tables** to map these numeric codes to meaningful labels  
3. For **Performance Rating**, multiple rating columns existed:
   - Created one shared Performance dimension
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
