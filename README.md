# Road-Accident-Dashboard-PowerBI
![image](https://github.com/user-attachments/assets/cc3a1329-40ea-4789-b612-939cd3fccadb)
## Table of Content
• [Introduction](#introduction)  
• [Dashboard Requirements](#dashboard-requirements)  
• [Installation / Usage](#installation--usage)  
• [DAX Formulas Used in Measures](#dax-formulas-used-in-measures)  
• [Bug / Feature Request](#bug--feature-request)  
• [Authors](#authors)  

## Introduction
•This project focuses on developing a Power BI Dashboard to analyze and generate insights from road accident data in the United Kingdom. 

•The dataset is available at the following link: [Road Accident Data (UK)](https://docs.google.com/spreadsheets/d/18gHMTeKObXTYW9-dTpC3Ix8cUassEVnv/edit?usp=sharing&ouid=112300673406057049645&rtpof=true&sd=true).

## Dashboard Requirements
•Primary KPIs - Total Casualties by Accident Severity (Fatal, Serious, Slight) for the Current Year and YoY Growth

•Monthly Trend showing comparison of Casualties for Current Year and Previous Year

•Current Year Casualties by Area/Location & Day/Night

•Casualties by Urban vs. Rural Areas 

•Weather Condition (All, Rain, Fog, Snow, Clear, etc.)

•Road Surface Condition (All, Dry, Wet, Icy, etc.)

•Weekly accident frequency
## Installation / Usage
•Install Power BI Desktop from the [Official Power BI Download Site](https://www.microsoft.com/en-us/download/details.aspx?id=58494).

•Download data files from link given in Introduction

•Download this repository to your local machine

•Open Dashboard report file (Road Accidents Dashboard.pbix) in Power BI Desktop, to access the dashboard's interactivity
## DAX Formulas Used in Measures
1. Average Speed Limit Calculation  
   • AvgSpeedLimit = AVERAGE(Table1[Speed_limit])  

2. Accident Severity Counts  
   • Fatal = CALCULATE(COUNT('Table1'[Accident_Severity]), 'Table1'[Accident_Severity] = "Fatal")  
   • Serious = CALCULATE(COUNT('Table1'[Accident_Severity]), 'Table1'[Accident_Severity] = "Serious")  
   • Slight = CALCULATE(COUNT('Table1'[Accident_Severity]), 'Table1'[Accident_Severity] = "Slight")  

3. Date Formatting  
   • Short number = FORMAT('Table1'[Accident Date], "mmm")  

4.Accident & Vehicle Counts
   • Total Accidents by Day = COUNTROWS('Table1')
   • Total Vehicles = COUNTROWS('Table1')

