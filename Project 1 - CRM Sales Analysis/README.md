# CRM Sales Analysis

## 🚀 Project Overview

This project focuses analysing air traffic across the US from 2000 to 2009. It presents key insights into passenger traffic, flight occupancy, route popularity and state-wise aire travel distribution. It helps stakeholders understand travel demand, airport performance, and flight patterns over the years.

## [Report](https://github.com/Trevor20/SQL-PowerBI-Portfolio/tree/main/projects/Project2-AirportAnalysis/report)

## 🎯 Objectives 

- Analyse Won deals and win rate over time.
- Assess top reasons the deals are lost.
- Check Sales performance across sales representatives and teams

## 📖 Dataset

The dateset in this project contains information about sales opportunities. The dataset includes information like lead source, sales representative, deal pipeline, reason for losing the deal,etc.

## 📂 Dataset Structure

The Dataset contains the following in 1 table

### 1. Sales_Data
| Column         | Description                                                             |
|----------------|-------------------------------------------------------------------------|
| Opportunity Id | Unique Id                                                               |
| Created Date   | Date the Opportunity was found                                          |
| Sales Rep      | Name of the person who was handling the sales opportunity               |
| Sales Team     | Team the sales rep was part of                                          |
| Lead Source    | Where did they get the opportunity from?                                |
| Deal Amount    | Value of the opportunity                                                |
| Stage          | Pipeline of the opportunity                                             |
| Close Date     | Date the opportunity was completed. Blank indicates the deal is ongoing |
| Loss Reason    | Reason the opportunity was lost                                         |

## 🔍 Key Business Questions Answered

1. What was the total value of opportunities over the past 2 years?
2. How many of those where closed-won deals, and whats the win rate?
3. How did the sales rep fair relative to each other?
4. What were the top reasons for losing the deal?
5. What is the won deals and win rate change over time?

## ➡️ Project Approach

### 1. Data Cleaning and Transformation on original data
1. On inspection, only the date columns were not in the correct data type. The date columns had time, which was unnecessary. Hence, changed the created date and closed date columns to short date data type. Rest of the data was clean.
2. Transformed the data by adding the following columns -
   - Open/Closed - Indicates if the deal is opened or closed
   - Time to close - Difference beteeen closed and open date, if closed date is not empty
   - EoM Created - End of month (EoM) date of date the opportunity was found.
   - Date Inc - TRUE/FALSE indicating whether the specified date falls within the dates the user indicated
   - Team Inc - TRUE/FALSE based on whether the user wants to check for the specific team
   - Rep Inc - TRUE/FALSE based on whether the user wants to check for the specific sales representative
   - Stage Inc - TRUE/FALSE based on whether the user wants to check for the specific stage of the pipeline
   - Source Inc - TRUE/FALSE based on whether the user wants to check for the specific Source
   - Master Inc - Multiplies all values in the prio created Inc Columns. Used this column to ensure only data that the user wants is choosen

### 2. Creation of Helper Worksheets 
The following worksheets were created for efficient selection of data based on user preferences
1. Dashboard Metrics - The main KPIs were created and formated on this page. The KPIs were transported to the main dashboard using the camera tool.
2. Index - To ensure efficient Xlookup by referencing Index instead of big values
3. Rank Rollup - Tables needed to make dashboard graphs were created in this worksheet
4. Data Rollup - Data needed by the user was transfered to this worksheet using the FILTER function and Master Inc Column


### 3. Data Visualatization on the Dashboard Worksheet
Created the following main sections of the dashboard to gather insights
1. Overview - Summary of relevant KPIs like total win bookings, total won deals, average time to close and pipeline value
2. Time-series analysis - tracks how win bookings and win rate changes with time
3. Top loss reasons - graph that indicate the main reasons the deals were lost
4. Sales Rep performance tracking - indicates how sales representatives are performing in the time period

## 🏆 Final Insights
- Emma was the best sales rep in the last 2 years.
- Only 33% of the closed deals were won.
- Price and timing were the main reasons for losing a deal.
- The win deals exibit approximately a cyclic pattern, with peaks typically happening around the midpoint of each half year.
- The win rate seem cyclic over time as well, with peaks happening every 4 months. 

