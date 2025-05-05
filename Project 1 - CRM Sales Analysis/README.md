# CRM Sales Analysis

## 🚀 Project Overview

This project analyzes CRM sales opportunity data to help stakeholders understand sales performance and deal outcomes. It focuses on tracking performance of sales representatives, win rates over time, and uncovering key reasons for deal losses. The goal is to generate actionable insights that improve sales strategies and team effectiveness.

📊 Built using advanced Excel techniques including dynamic filtering, helper sheets, calculated fields, and camera tool integration for an interactive dashboard experience. 

## [Report](https://github.com/Trevor20/Excel-Portfolio/blob/main/Project%201%20-%20CRM%20Sales%20Analysis/Sales%20Dashboard%20Screenshot.png)

## 🎯 Objectives 

- Track won deals and win rate over time.
- Assess top reasons for deal losses.
- Assess performance across sales representatives and teams

## 📖 Dataset

The dataset includes information on individual sales opportunities like lead source, sales representative/team, deal pipeline, loss reasons, etc.

## 🧰 Tools Used

- Microsoft Excel - For data cleaning, transformation, and interactive dashboard design.
- Excel Tables - To structure data and enable automatic expansion with new entries.
- Excel Functions - XLOOPUP, FILTER, SORT, IF, EOMONTH, SEQUENCE and logical operations.
- Named Ranges & Helper Sheets - To support dynamic filtering.
- Camera Tool - For embedding KPI visuals into the main dashboard.

## 📂 Dataset Structure

The Dataset contains the following in 1 table

### 1. Sales_Data
| Column         | Description                                                             |
|----------------|-------------------------------------------------------------------------|
| Opportunity Id | Unique Id for each sales deal                                           |
| Created Date   | Date the Opportunity was found                                          |
| Sales Rep      | Sales representative assigned to the deal                               |
| Sales Team     | Team the sales rep was part of                                          |
| Lead Source    | Origin of the sales opportunity                                         |
| Deal Amount    | Value of the opportunity                                                |
| Stage          | Pipeline of the opportunity                                             |
| Close Date     | Date the opportunity was completed. Blank indicates the deal is ongoing |
| Loss Reason    | Reason the opportunity was lost (if applicable                          |

## 🔍 Key Business Questions Answered

1. What is the total value of sales opportunities over the past 2 years?
2. What proportion of deals were successfully closed (win rate)?
3. How did the sales rep perform relative to each other?
4. What are the most common reasons for losing deals?
5. How do won deals and win rates trend over time?

## ➡️ Project Approach

### 1. Data Cleaning and Transformation on original data
1. Converted Created Date and Close Date to short date format(removed time). Rest of the data was clean.
2. Converted data into Excel Table to ensure dashboard updates with changes in data. 
3. Transformed the data by adding the following columns -
   - Open/Closed - Indicates if the deal is opened or closed
   - Time to close - Difference between closed and open date, if closed date is not empty
   - EoM Created - End of month (EoM) date of date the opportunity was found.
   - Date Inc - TRUE/FALSE indicating whether the specified date falls within the dates the user indicated
   - Team Inc - TRUE/FALSE based on whether the user wants to check for the specific team
   - Rep Inc - TRUE/FALSE based on whether the user wants to check for the specific sales representative
   - Stage Inc - TRUE/FALSE based on whether the user wants to check for the specific stage of the pipeline
   - Source Inc - TRUE/FALSE based on whether the user wants to check for the specific Source
   - Master Inc - Multiplies all values in the prior created Inc Columns. Used this column to ensure only data that the user wants is chosen

### 2. Creation of Helper Worksheets 
The following worksheets were created for efficient selection of data based on user preferences
1. Dashboard Metrics - The main KPIs were created and formatted on this page. The KPIs were transported to the main dashboard using the camera tool.
2. Index - Lookup helper to simplify formulas using XLOOKUP.
3. Rank Rollup - Tables needed to make dashboard graphs were created in this worksheet
4. Data Rollup - Dynamic dataset filtering using the FILTER() + Master Inc logic


### 3. Data Visualization on the Dashboard Worksheet
Created the following main sections of the dashboard to gather insights
1. Overview - Summary of relevant KPIs like total win bookings, total won deals, average time to close and pipeline value
2. Time-series analysis - tracks how win bookings and win rate changes with time
3. Top loss reasons - graph that indicate the main reasons for losing deals
4. Sales Rep performance tracking - indicates how each sales representative is performing over time

## 🏆 Final Insights
- 👜 Emma was the top-performing sales representative over the past 2 years.
- 🧮 Only 33% of the closed deals were won, highlighting room for conversion improvement.
- ❌ The top loss reasons were Pricing and Bad Timing.
- 📉 Win deals exhibit a cyclic pattern, with peaks typically happening around mid-year and dropping toward year-end
- 📆 Win rate exhibited 4-month cycles, suggesting a seasonal or campaign-driven effect. 

