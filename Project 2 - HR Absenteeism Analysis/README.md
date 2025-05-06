# Analysing Employee Absenteeism using Excel 

## 🚀 Project Overview

This project analyses workplace absenteeism using employee demographics, lifestyle choices and compensation data. Furthermore, the HR department is looking to promote a healthy workforce through incentive programs like a bonus. Specifically, they aim to identify healthy employees with low absenteeism for a health bonus and evaluate compensation adjustments for non-smokers.

Data was extracted and loaded using Excel Power Query Editor. Data cleaning and modelling was done using Excel Functions. Key trends and insights was visualized through a two-page Excel dashboard.

## [Report](https://github.com/Trevor20/Excel-Portfolio/blob/main/Project%202%20-%20HR%20Absenteeism%20Analysis/Absenteeism_Dashboard_Overview.png)

## 🧠 Business Problem

Employee absenteeism directly affects productivity and efficiency. The HR department wants to understand the major reasons of absenteeism and identify areas where intervention - through wellness programs and compensation changes - can reduce unplanned leave and encourage healthier employee behaviour.

## 🎯 Objectives 

1. HR wants the following information for their incentive programs
   - Provide a list of healthy individuals and low absenteeism for a health bonus program.
   - Calculate wage increase for non-smokers - budget $983,221
2. Develop an Excel dashboard to help HR understand key absenteeism patterns accross time, demographics and lifestyle
   - Absenteeism Overview - Key trends, Absenteeism Distribution and top reasons for being absent 
   - Absenteeism Factors - Analysis of how compensation, disciplinary failure and social lifestyle (Smoker, Drinker, BMI and no of degrees, pets and children) impact absenteeism.

## 📖 Dataset

The dataset includes information on:
- Demographics: Age, education, BMI, children, pets
- Compensation: Compensation per hour
- Lifestyle: Smoking, drinking habits
- Absenteeism: Reasons, number of hours, days of the week, and months

The data is anonymized and provided in CSV format. The dataset has 740 records.

## 🧰 Tools Used
- Microsoft Excel - For data transformation, and dashboard design.
- Power Query Editor - To merge data and data cleaning 
- Pivot Table - To group and summarize data.
- Excel Functions - VLOOPUP, FILTER, SORT, TEXT, UNIQUE.
- Helper Sheets - To support dynamic filtering.
- Camera Tool - For embedding KPI visuals into the main dashboard.

## 📂 Dataset Structure

The following three CSV tables were connected and imported into Excel

### 1. Compensation
| Column  | Description                    |
|---------|--------------------------------|
| Id      | Unique employee Id             |
| Comp/hr | Compensation per hour ($/hour) |


### 2. Absent_Data
| Column | Description             |
|--------|-------------------------|
| Number | Unique Reason Id        |
| Reason | Reason for being absent |


### 3. Absent_Data
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

## 🔍 Key Business Questions Answered

1. Who are the healthy individuals with low absenteeism eligible for a health bonus program?
2. Calculate wage increase for non-smokers. Budget is $983,221.
3. How does absenteeism vary accross weekdays and months?
4. What are the top reasons employees take leave?
5. Is there a correlatiion between age or compensation and absent hours?
6. Does lifestyle(Smoking, drinking, education, children, pets) influence absenteeism?
7. Does having a disciplinary failure impact hours absent?
8. Does BMI impact absenteeism?

## ➡️ Project Approach

### 1. Data Cleaning and Transformation using Excel Power Query Editor and Excel Functions
1. Imported and merged three CSV tables into a clean dataset.
2. Removed ambiguous and low-value columns.
3. Created BMI Category and Season columns using Index + VLOOKUP.

### 2. Creation of Helper Worksheets

The following worksheets were created for efficient selection of data based on user preferences

- Dashboard Metrics - The main KPIs were created and formatted on this page. The KPIs were transported to the main dashboard using the camera tool.
- Index - Lookup helper to simplify formulas using VLOOKUP.
- Calculation Engine - Tables needed to make dashboard graphs were created in this worksheet.

### 3. Dashboard Development in Excel
The dashboard has the following main Attributes
1. Page 1 - Absenteeism Overview
   - KPI - Summary of relevent KPIs like total employees, average time absent, % of smokers/drinkers, etc
   - Time-series analysis - tracks when employees take leaves
   - Employee demographics - Determines employee body factors (BMI, age) that tend to take more leaves
   - Top reasons - table that indicates primary absent causes
  
2. Page 2 - Absenteeism Factors
   - Work factors - graphs that indicate whether disciplinary failure and compensation/hr are related to absenteeism
   - Social factors - Provide insights into what social factors affect absenteeism
   - Health factors - Column charts that indicade whether BMI or smoker/drinker affect absenteeism 

## 🏆 Final Insights
- 📈 Non-Smokers are eligible for a wage increase of approx $1433.
- 📆 March sees the highest number of absentees; Thursdays the lowest.
- 🦾 Over 50% of employees taking leave are in the healthy BMI range.
- 🧔 Significant absent hours come from the 31-34 age group.
- 🦷 Medical and dental consultations make up majority of the leaves.
- 💰 There is a slight positive correlation between compensation/hour and absent hours
- 0️⃣ No one who had a disciplinary failure took leave
- 🍹 Employees who drink but do not smoke had the highest absent hours.

