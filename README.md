# Challenge_5

## Background

I just joined Pymaceuticals, Inc., as a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, I've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team has tasked me with generating all of the tables and figures needed for the technical report of the clinical study. They have also asked me for a top-level summary of the study results.

## Files

I downloaded the following files to help me get started:


## Instructions
This task is broken down into the following tasks:

Preparing the data.

Generating summary statistics.

Creating bar charts and pie charts.

Calculating quartiles, find outliers, and create a box plot.

Creating a line plot and a scatter plot.

Calculating correlation and regression.

Submitting my final analysis.

## Preparing the Data

I ran the provided package dependency and data imports, and then merge the mouse_metadata and study_results DataFrames into a single DataFrame.

Displayed the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Displayed the data associated with that mouse ID, and then created a new DataFrame (called combined_data_df) where this data was removed.  I used this cleaned DataFrame for the remaining steps.

1. To display the updated number of unique mice IDs.

2. Generate Summary Statistics

3. Create a DataFrame of summary statistics. 

My summary statistics include:

1. A row for each drug regimen. These regimen names were contained in the index column.

2. A column for each of the following statistics: mean, median, variance, standard deviation, and SEM of the tumor volume.

## Thereafter I Created Bar Charts and Pie Charts

- Generated two bar charts. Both charts were identical and showed the total total number of rows (Mouse ID/Timepoints) for each drug regimen throughout the study.

a. Created the first bar chart with the Pandas DataFrame.plot() method.

b. Created the second bar chart with Matplotlib's pyplot methods.

- Generated two pie charts. Both charts were identical and showed the distribution of female versus male mice in the study.

a. Created the first pie chart with the Pandas DataFrame.plot() method.

b. Created the second pie chart with Matplotlib's pyplot methods.

## Calculated Quartiles, Find Outliers, and Create a Box Plot

Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculated the quartiles and IQR, and determined if there were any potential outliers across all four treatment regimens. Using the following substeps:

I created a grouped DataFrame that shows the last (greatest) time point for each mouse. Merged this grouped DataFrame with the original cleaned DataFrame.

Created a list that holds the treatment names as well as a second, empty list to hold the tumor volume data.

Looped through each drug in the treatment list, located the rows in the merged DataFrame that correspond to each treatment. Appended the resulting final tumor volumes for each drug to the empty list.

Determined outliers by using the upper and lower bounds, and then print the results.

Using Matplotlib, I generated a box plot that shows the distribution of the final tumor volume for all the mice in each treatment group. Highlighted any potential outliers in the plot by changing their color and style.



Created a Line Plot and a Scatter Plot
Selected a single mouse that was treated with Capomulin, and generate a line plot of tumor volume versus time point for that mouse.

Generated a scatter plot of mouse weight versus average observed tumor volume for the entire Capomulin treatment regimen.

Calculated Correlation and Regression
Calculated the correlation coefficient and linear regression model between mouse weight and average observed tumor volume for the entire Capomulin treatment regimen.

Ploted the linear regression model on top of the previous scatter plot.

## Requirements
Prepare the Data (20 points)
The datasets are merged into a single DataFrame. (6 points)
The number of mice are shown from the merged DataFrame. (2 points)
Each duplicate mice is found based on the Mouse ID and Timepoint. (6 points)
A clean DataFrame is created with the dropped duplicate mice. (4 points)
The number of mice are shown from the clean DataFrame. (2 points)
Generate Summary Statistics (15 points)
The mean of the tumor volume for each regimen is calculated using groupby. (2 points)
The media of the tumor volume for each regimen is calculated using groupby. (2 points)
The variance of the tumor volume for each regimen is calculated using groupby. (2 points)
The standard deviation of the tumor volume for each regimen is calculated using groupby. (2 points)
The SEM of the tumor volume for each regimen is calculated using groupby. (2 points)
A new DataFrame is created with using the summary statistics. (5 points)
Create Bar Charts and Pie Charts (15 points)
A bar plot showing the total number of timepoints for all mice tested for each drug regimen using Pandas is generated. (4.5 points)
A bar plot showing the total number of timepoints for all mice tested for each drug regimen using pyplot is generated. (4.5 points)
A pie plot showing the distribution of female versus male mice using Pandas is generated. (3 points)
A pie plot showing the distribution of female versus male mice using pyplot is generated. (3 points)
Calculate Quartiles, Find Outliers, and Create a Box Plot (30 points)
A DatFrame that has the last timepoint for each mouse ID is created using groupby. (5 points)
The index of the DataFrame is reset. (2 points)
Retrieve the maximum timepoint for each mouse. (2 points)
The four treatment groups, Capomulin, Ramicane, Infubinol, and Ceftamin, are put in a list. (3 points)
An empty list is created to fill with tumor volume data. (3 points)
A for loop is used to display the interquartile range (IQR) and the outliers for each treatment group (10 points)
A box plot is generated that shows the distribution of the final tumor volume for all the mice in each treatment group. (5 points)
Create a Line Plot and a Scatter Plot (10 points)
A line plot is generated that shows the tumor volume vs. time point for one mouse treated with Capomulin. (5 points)
A scatter plot is generated that shows average tumor volume vs. mouse weight for the Capomulin regimen. (5 points)
Calculate Correlation and Regression (10 points)
The correlation coefficient and linear regression model are calculated for mouse weight and average tumor volume for the Capomulin regimen. (10 points)
Grading
This assignment will be evaluated against the requirements and assigned a grade according to the following table:


References
I leaverage the Xpert Learning Assistant for debugging

Find my high level summary in word document 