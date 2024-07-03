# Australian Road Accident Data Analysis (1989-2021)

## Introduction

### Background of the Study

This report delves into the Australian Road Accident data from 1989 to 2021, aiming to uncover significant patterns and trends that contribute to road fatalities. The analysis uses inferential statistics, data visualization, and comprehensive exploration to understand the main causes of crash incidents. The ultimate goal is to inform the creation of safety measures and policies to reduce road accidents and save lives.
## Tools Used
- Ms Power BI
- Ms Excel
- Ms Word (3 Reports)
- Ms Power Point

## Data Wrangling

### Data Loading

- The crash data, initially in CSV format, was loaded into Power BI where the data was cleaned, shaped, and transformed using the Power Query Editor. Transformations included standardizing state names, correcting age values, filling missing gender data, and creating new age-related columns.

### Data Cleaning & Transformation

- State: Standardized state names.
- Age: Corrected negative values to positive integers.
- Gender: Filled missing values with "No Data Available" (NDA).
- Columns with Blanks: Filled blanks in columns like Bus Involvement and Heavy Rigid Truck Involvement with NDA.
- Age Group: Dropped due to blank values and created new columns "Age Range" and "Age Categories".
- Crash ID Duplicates: Removed duplicates.
- Unspecified Gender: Replaced with NDA.
- Other Road User: Standardized values.

### Creating Measures

- Using DAX formulas, the following measures were created:
  - Total Crashes: COUNTROWS ('Crash_Data (2)')
  - Average Speed: AVERAGE ('Crash_Data (2)'[Speed Limit])
  - CY Accidents: TOTALYTD (COUNT ('Crash_Data (2)'[Crash ID]), 'Calendar'[Date])
  - PY Accidents: TOTALYTD (COUNT ('Crash_Data (2)'[Crash ID]), SAMEPERIODLASTYEAR('Calendar'[Date]))
  - YoY Accidents: ([CY Accidents] - [PY Accidents]) / [PY Accidents]

## Data Visualization

- Data visualization was conducted to accurately represent findings without distortion. Various charts and graphs were created:
  - Card Visuals: Showing the total number of crash incidents.
  - Pie Chart: Illustrating crashes by time of day.
  - Donut Chart: Gender distribution in crashes.
  - Column Chart: Crashes by state.
  - Bar Chart: Crashes by age group.
  - Waterfall Chart: Single vs multiple vehicle crashes.
  - Area Chart: Crashes by speed.
  - Line Chart: Crashes by time of day.
  - Stacked Column Chart: Crashes by age categories and range.
  - Decomposition Tree: Breakdown of crashes by various components.
  - Matrix: Crashes by time of day and gender.
  - Donut Chart: Crashes during the Christmas period.

## Data Dashboard/Reports

- Main Dashboard: Overview of crash incidents.
- Duration Analysis Dashboard: Analysis by time.
- Roads Dashboard: Crash analysis by road type.
- Demographics Dashboard: Demographic analysis of crash incidents.

## Descriptive Data Analysis

### Dataset Overview

- The dataset includes Australian Road Accident data from 1989 to 2021. The data, sourced from the Australian Road Death Database, is available on Kaggle in CSV format [here](link_to_data).

### Variables

- The dataset includes various variables such as Crash Id, State, Month, Year, Day of the Week, Time, Crash Type, Speed Limit, Road User, Gender, Age, Age Group, Holiday Periods, National Road Type, and others.

### Dashboard

- A comprehensive dashboard is provided for visualizing key insights from the data.
  ![Main Dashboard](https://github.com/RojeshDhakal/AustraliaRoadAccidentAnalysis/raw/main/Visualization%201/main%20dashboard.PNG)


### Descriptive Statistics for Quantitative Variables

- Speed Limit: Analysis includes descriptive statistics, boxplots, and histograms to provide insights into speed limits during crashes.
- Age: Analysis includes descriptive statistics, boxplots, and histograms to provide insights into the ages of individuals involved in crashes.
- Year: Analysis includes descriptive statistics to provide insights into crash occurrences over the years.

### Descriptive Statistics for Qualitative Variables

- Gender: Analysis includes distribution charts to highlight gender disparities in crash involvement.
- Month: Analysis includes line charts to show crash occurrences across different months.
- Time: Analysis includes line charts to show crash timings and highlight notable patterns.
- Age Group: Analysis includes distribution charts to show the total number of crashes by different age groups.
- Weekdays: Analysis includes bar charts to show crash distribution by day of the week.
- Day of Week: Analysis includes donut charts to show crash distribution during weekends and weekdays.
- Road User: Analysis includes charts to show crash involvement by different road users.
- Time of the Day: Analysis includes donut charts to show crash occurrences during different times of the day.
- Crash Types: Analysis includes pie charts to show crash distribution by different crash types.

## Diagnostic Analysis

### Bivariate Analysis

- Age Group & Gender: Analysis includes charts to show crash involvement by age group and gender.
- Gender & Speed: Analysis includes charts to show crash involvement by gender and speed.
- Gender & Crash Type: Analysis includes charts to show crash involvement by gender and crash type.
- Gender & Time of Day: Analysis includes charts to show crash involvement by gender during day and night.

### Multivariate Analysis

- Age Group, Crash Types & State: Analysis includes charts to show crash involvement by age group, crash type, and state.
- Age Group, Gender, and Crash Type: Analysis includes charts to show crash involvement by age group, gender, and crash type.
- Gender, Age Group, and Time of Day: Analysis includes charts to show crash involvement by gender, age group, and time of day.

## Business Questions

### Business Questions

- How can road safety laws and policies be improved to better address the needs of vulnerable groups like young adults and seniors?
- How can innovative strategies and campaigns be developed to effectively raise awareness and encourage safer road behaviors within these demographics?

### Business Questions using Descriptive Statistics

- How does the distribution of driving speeds vary across different age groups, and what trends in speed behaviors can be identified for road safety?
- How can new speed limits and safety guidelines be recommended by analyzing trends?
- What is the relationship between age and crash rates, and how can this data be leveraged to create targeted safety measures tailored to specific age groups?

## Hypothesis Testing

- Analysis between Speed and Age: Tests the correlation between age and crash speed.
- Analysis of Crash with Age: Tests the correlation between age and road accidents.
- Analysis of Crash with Speed Limit: Tests the association between speed limits and the frequency of road accidents.
- Analysis of Crash with Speed: Tests the trend of accident crashes over the years.

## Exploratory Data Analysis

- Exploratory Data Analysis (EDA) techniques are applied to further investigate patterns and trends in the data. Results are explained and interpreted with supporting evidence.

## Feature Selection

- The most important variables are selected and their impact is discussed.

## Conclusions

- Key findings and conclusions drawn from the analysis are presented in each individual report.

## References

- All references and sources used in the three report that is in my repo.
