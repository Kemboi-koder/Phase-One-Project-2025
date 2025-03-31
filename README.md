Final Project Submission

    Student name: Kemboi Bett

    Student pace: Full-Time Remote

    Instructor name: Diana Mongina

## Introduction

It is said that flying is among the safest and fastest ways to travel despite the number of aviation accidents that have occurred throughout the years. The aviation industry is a lucrative and fast growing sector in transport. That being mentioned, my project aims to use aviation data to identify the risk factors that contribute to accidents and how they relate to specific public and private aircraft carriers to make informed decisions on which aircraft models are best suited for a company trying to venture into the industry.

## Project overview

In this project using NTSB Aviation data(1962- 2023), the aim is to identify which aircraft carriers are less likely to cause fatal accidents in order to purchase these aircraft to venture into the business. The data will be first reviewed to farmiliarise with the indexes and columns.Next it will be checked for missing values and all unecessary datasets cleared.Computation is done where needed and finally we perfom analysisi with visualizations and provide recommendations and insights.


# 1. BUSINESS UNDERSTANDING
   
In order to diversify its portfolio, Green Collar Solutions Ltd. Is expanding into new ventures specifically the Aviation industry. The aim of this project is to find out which commercial and public aircrafts are suitable for purchase when entering this venture. The targets include:

    Which aircrafts have the records for the least accidents
    Which aircrafts are resilient to harsh weather conditions/ are equipped to handle emergencies well.
    What risk factors are associated with other aircrafts

   ## Parameters for success
   
Being able to provide insights into the cause of aircraft accidents for aircrafts and which ones are safe for purchase. Ability to clean data. Ability to make relevant correlations

First import the relevant Python libraries. This includes numpy, pandas, matplotlyb.pyplot and searbon

Load the data and print out an overview of the columns using the  pd.read_csv method

Get an overview of the dataset using: df.info, df.head, df.tail, df.shape, etc.

# 2. DATA PREPARATION

It involves using various methods to manipulate the raw data to prepare it for analysis. The steps carried out in this phase were:

## Dropping missing values

Find the percentage of missing values in the columns
Remove columns with a high percentage of missing values and are irrelevant to the study
check the rows to see if there are still missing values

## Drop irrelevant columns.

From the data, we can still see that there are still some missing data. Furthermore, some columns contain data that are not relevant to the study. We identify relevant columns that can help in the project analysis and drop the rest.
In our case the relevant columns here are namely: 'Make', 'Model', 'Injury.Severity',' Event.Date', 'Number.of.Engines', 'Total.Fatal.Injuries', 'Total.Serious.Injuries', 'Total.Minor.Injuries', 'Total.Uninjured', 'Broad.phase.of.flight', 'Weather.Condition', 'Aircraft.damage', 'Purpose.of.flight'

Now we find the total sum of missing values in the <relevant_columns>. After we find the sum of missing values, we can execute two operations namely; fill in missing values and or drop missing values.

## Fill in the missing data

Identify columns with continuous data and fill the missing values with the median. Find the continuous data types using
df.info()
The continuous data columns are: 'Number.of.Engines', 'Total.Fatal.Injuries', 'Total.Serious.Injuries', 'Total.Minor.Injuries', 'Total.Uninjured'
Fill the continuous data columns  their median using .fillna(medians)
Check for missing values in the rows of the remaining columns
Drop missing data from the remaining columns
Check if there are any remaining missing values

## Implement changes to the file

Save the changes onto the CSV file and create a copy of the file that will be used for creating visualizations.
Upload changes onto the csv using df.to_csv('Cleaned_Aviation_Data.csv',index = False) 
Create a copy of the clean dataset using df.copy()

# 3. MODELLING

Now that our data is ready we can proceed to create visual models that will help in evaluation. Here we make use of visual python libraries called Matplotlib and Seaborn which are essential for creating visual analysis. Here we will look for any aspect of correlation between the remaining variables and see if there is any correlation and to what extent the correlation occurs.

### Import the relevant libraries
import matplotlib.pyplot as plt
import seaborn as sns
%matplotlib inline
## Use the following visualizations

Plot a time series of the number of accidents over time 

Plot the bar chart for the top 15 Aircraft type with the most accident occurrences

Plot the bar chart for the bottom 15 Aircraft type with the least accident occurrences

Plot combined bar graph showing relationship between Aircraft types and severity of injuries after accident.

Plot heatmap that shows the relationship between aircraft damage and purpose of flight










