---
title: "ExcelHelpLine Bootcamp: Web Scraping and Data Analysis Exercises"
date: 2024-08-01
draft: false
author: "John Adrian Adona"
tags:
  - "Python"
  - "Pandas"
  - "NumPy"
  - "Matplotlib"
  - "Web Scraping"
  - "BeautifulSoup"
image: /images/projects/python-excelhelpline/python-thumbnail.jpg
description: ""
toc: trues
mathjax: true
---

<div style="text-align: justify;">

Hello! A few months ago, I completed the Full Stack Data Analyst Bootcamp from ExcelHelpLine, where I gained hands-on experience with essential tools and software used by Data Analysts, featuring Excel, VBA, Power BI, SQL, and Python. In this article, I'd like to share and highlight some of the Python exercises I worked on during the course, showcasing the skills I've developed and how I've applied them in practical scenarios. Have a look around!

For more details about the rest of my Python exercises and other materials, you can check them out in my [GitHub repository](https://github.com/John-Adrian-Adona/ExcelHelpLine-Bootcamp-Python-Compilation).

</div>

<br>

___

<div style="text-align: justify;">

### Skills and Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Beautiful Soup

<br>

### Web Scraping Activity 

**Goal:**
  - Webscrape from this web page: [Worldometer - Philippines Population](https://www.worldometers.info/world-population/philippines-population/) 
  - Produce three CSV files from the three tables (Please enter provided link for more details)

*1. In the script below, I developed a function where it webscrapes all specified tables from a webpage by its CSS class, converting it to a pandas DataFrame.*

<div style="text-align: center;">
<img src="https://i.postimg.cc/sXKykw66/image.png" width="50%">
</div>

<br>

*2. Using the function, I webscrape the three tables of interest from the webpage where I export them as CSV files.*

<div style="text-align: center;">
<img src="https://i.postimg.cc/Pqqcx6j7/image.png" width="60%">
</div>
<br><br>

The images below show how web scrapped tables look like: 
- See webpage to validate original tables with the results ([Worldometer - Philippines Population](https://www.worldometers.info/world-population/philippines-population/)) 


<div style="text-align: center;">
<img src="https://i.postimg.cc/qMZfVVnF/image.png" width="90%">

Population of the Philippines (2024 and historical)

<img src="https://i.postimg.cc/hgdXs4gx/image.png" width="90%">

Philippines Population Forecast

<img src="https://i.postimg.cc/t405VBHT/image.png">

Main Cities by Population in the Philippines

</div>

<br><br>

### Data Analysis Exercises
**Goal:**
  - Perform the following tasks on the Customers and Orders CSV dataset

<div style="text-align: center;">

**IMAGES OF INPUT FILES USED**

<img src="https://i.postimg.cc/ZqnWsGGj/image.png" width="60%">

Customers CSV dataset

<img src="https://i.postimg.cc/nrpZg7sZ/image.png" width='30%'>

Orders CSV dataset
</div><br>

*1. **Data Cleaning and Preprocessing Task**: Clean both of the CSV files in Python.*

For this Python exercise, I performed the following clean up to showcase my python literacy:
- Replaced NaN in the Customer ID column of the Customer DataFrame with the value 6.
- Imputed missing values in the Points column of the Customer DataFrame with the mean.
- Removed rows with missing values from the Orders DataFrame.
- Converted the Order Date and Shipping Date columns in the Orders DataFrame to datetime format.
- Corrected the erroneous '7392.68a' entry in the Order_Total column to '7392.68'.

<div style="text-align: center;">
<img src="https://i.postimg.cc/zBsf39HD/image.png" width="60%">

Screenshot of the Python script - Data Cleaning and Preprocessing

<img src="https://i.postimg.cc/RFpvn23J/image.png" width="80%">

Preprocessed / Cleaned Customer DataFrame Result

<img src="https://i.postimg.cc/g0JzkYjb/image.png" width="40%">

Preprocessed / Cleaned Orders DataFrame Result

</div><br>

*2. **Calculate Average Shipping Duration**: What is the average shipping in terms of days?*

For this Python exercise, I performed the following steps:
- Merged the Customer and Orders DataFrames into a new DataFrame, conso_df.
- Imputed missing values in the State column of conso_df using the mode (most frequent value).
- Calculated the difference between Shipping Date and Order Date, storing the result in a new column, Order_To_Shipping.
- Computed the mean of the Order_To_Shipping column.

<div style="text-align: center;">
<img src="https://i.postimg.cc/T2FBg69G/image.png" width="60%">

Screenshot of the Python script - Average Shipping Duration Calculation

<img src="https://i.postimg.cc/nLsfcp7g/image.png" width="90%">

Screenshot of conso_df DataFrame

<img src="https://i.postimg.cc/bvS4fLfj/image.png">

The Average Shipping Duration in terms of Days

</div><br>

*3. **Identify Top Customers by Points and Revenue**: Top 3 Customers in terms of Points and Revenue.*

For this Python exercise, I performed the following steps:
- Sorted the conso_df DataFrame in descending order based on the Points column.
- Retrieved all rows from the conso_df DataFrame corresponding to the top 3 highest Points.

<div style="text-align: center;">
<img src="https://i.postimg.cc/cJ7pvM03/image.png" width='60%'>

Screenshot of the Python script - Top Customers 

<img src="https://i.postimg.cc/C0QTvBp1/image.png" width='90%'>

Screenshot of Top 3 Customers in terms of Points

<img src="https://i.postimg.cc/HjGz0Rtk/image.png" width='90%'>

Screenshot of Top 3 Customers in terms of Revenue

</div><br>

*4. **State Revenue Aggregation**: Top 5 state in terms of Revenue.*

For this Python exercise, I performed the following steps:
- Grouped the conso_df DataFrame by the State column and calculated the total revenue (Order_Total) for each state.
- Retrieved and displayed the top 5 states with the highest total revenue.

<div style="text-align: center;">
<img src="https://i.postimg.cc/q7HW0yJh/image.png" width='75%'>

Screenshot of the Python script - State Revenue Aggregation

<img src="https://i.postimg.cc/RCtDhLdZ/image.png">

Screenshot of Top 5 States in terms of Revenue

</div><br> 

*5. **Visualizing Data with Bar and Line Charts**: Create a bar char (Revenue by State) and line chart.*

For this Python exercise, I created the following charts:

- Bar Chart: Total Revenue per State
  - Grouped the data by State column to calculate total revenue
  - Generated a bar chart to visualize total revenue by state. 
  - Based on the bar chart, Florida has the lowest revenue while Connecticut has the highest revenue among the US States.

<div style="text-align: center;">
<img src="https://i.postimg.cc/50Gp1m2L/image.png" width='50%' style="margin-right:20px;">
<img src="https://i.postimg.cc/RZHj6NHc/image.png" width='40%'>

Script and Screenshot of my Bar Chart Output

</div><br>

- Line Chart: Total Daily Orders 
  - Grouped the data by Order_Date column to calculate total orders
  - Generated a line chart to visualize total order per day from June 1-14, 2024. 
  - Based on the line chart, June 7 has the highest order total while June 11 has the lowest order total recorded.
  
<div style="text-align: center;">
<img src="https://i.postimg.cc/jjrdLVLS/image.png" width='45%' style="margin-right:20px;">
<img src="https://i.postimg.cc/tg2Qy86f/image.png" width='50%'>

Script and Screenshot of my Line Chart Output

</div>