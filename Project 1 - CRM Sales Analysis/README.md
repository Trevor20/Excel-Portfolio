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
   a. Open/Closed - Indicates if the deal is opened or closed
   b. Time to close - Difference beteeen closed and open date, if closed date is not empty
   
   

### 1. Data Visualatization Using Power BI
Created the following main sections of the dashboard to gather insights
1. Overview - Summary of relevant KPIs like total passengers, longest route, % unoccupied seats per flight, flight distance per route, etc
2. Time-series analysis - tracks how passenger traffic evolved over the years
3. Airport popularity - graphs that highlight the busiest airports an popular flight routes
4. Market trends - Donut chart that indicates the most common purpose of travel
5. Region wise analysis - Heatmap that indicates top states in the US that have the most passenger traffic (incoming and outgoing)

## 🏆 Final Insights
- Emma was the best sales rep in the last 2 years.
- Only 33% of the closed deals were won.
- Price and timing were the main reasons for losing a deal.
- The win deals exibit approximately a cyclic pattern, with peaks typically happening around the midpoint of each half year.
- The win rate seem cyclic over time as well, with peak heppening every 4 months. 

