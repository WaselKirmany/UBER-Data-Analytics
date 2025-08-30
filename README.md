# UBER-Data-Analytics
NCR Ride-Hailing Service Analysis
Project Overview
This project performs a comprehensive analysis of a ride-hailing service's booking data in the National Capital Region (NCR). The goal is to uncover key insights into customer behavior, operational efficiency, and service quality. The analysis is conducted using two primary tools: Python for data cleaning and exploratory analysis, and Microsoft Power BI for creating a detailed, interactive business intelligence dashboard.

The dataset used is ncr_ride_bookings.csv, which contains 150,000 anonymized records of ride bookings, including details on timing, locations, vehicle types, fares, and ride statuses.

Key Questions Explored
This analysis aims to answer several critical business questions:

What are the peak hours and busiest days of the week for ride bookings?

Which pickup and drop-off locations are the most popular?

What are the primary reasons for ride cancellations by both customers and drivers?

How do key metrics like revenue, ride volume, and ratings vary by vehicle type?

What is the relationship between ride distance and the booking fare?

How do service quality metrics like driver and customer ratings trend over time?

Tools Used
Data Cleaning & Analysis: Python

Pandas: For data manipulation, cleaning, and preparation.

Matplotlib & Seaborn: For static data visualization and exploratory analysis.

Interactive Dashboarding: Microsoft Power BI

Power Query: For data transformation and cleaning.

DAX (Data Analysis Expressions): For creating calculated columns and advanced measures.

Part 1: Python Analysis (Data Cleaning & EDA)
The initial analysis was performed in a Python script to clean the raw data and generate key exploratory visualizations.

Data Cleaning Process
A Python script (analysis_script.py) was used to perform the following cleaning and preparation steps:

Loaded the Data: Imported the ncr_ride_bookings.csv into a Pandas DataFrame.

Standardized Headers: Trimmed leading/trailing whitespace from column names.

Cleaned String Data: Removed erroneous triple-quote characters from Booking ID and Customer ID fields.

Datetime Conversion: Combined the Date and Time columns into a single datetime object for time-series analysis.

Handled Missing Values: Imputed missing numerical data for completed rides using median values to ensure robust analysis.

Exploratory Visualizations (Matplotlib & Seaborn)
Several charts were generated to understand the data's distribution and trends:

Booking Trends: Line charts for hourly, daily, and monthly ride volumes to identify peak demand periods.

Location Analysis: Bar charts highlighting the Top 10 busiest pickup and drop-off locations.

Cancellation Analysis: Bar charts showing the most common reasons for cancellations by both drivers and customers.

Service Quality: Histograms displaying the distribution of driver and customer ratings.

Financial Analysis: A scatter plot with a regression line to analyze the correlation between Ride Distance and Booking Value.

Part 2: Power BI Interactive Dashboard
A comprehensive, multi-page interactive dashboard was built in Power BI to allow for dynamic exploration of the data.

Data Transformation (Power Query)
The same cleaning steps from the Python script were replicated in the Power Query Editor to ensure data integrity.

Data types were corrected for all columns.

DAX Calculations
Several DAX measures and calculated columns were created to enhance the dashboard's capabilities, including:

Total Bookings, Total Revenue, Average Fare: Core KPI measures.

Trip Duration: A calculated column ([Avg CTAT] - [Avg VTAT]) that computes the trip time only for completed rides using an IF condition.

Month Name & Month Number: Helper columns created to ensure correct chronological sorting of months in visuals.

Dashboard Pages
The report is structured into five distinct pages for a clear narrative:

Homepage: An executive summary with key KPI cards, a donut chart for booking statuses, and high-level trends for monthly revenue and top locations.

Bookings: A deep dive into demand patterns, with visuals for hourly and daily trends, and a map to show geographic hotspots.

Vehicle Type: A comparative analysis of different vehicle types across metrics like ride volume, total revenue, and average ratings.

Revenue: A financial overview, including revenue by payment method and a scatter plot analyzing the relationship between ride distance and fare.

Ratings: A service quality page focusing on the distribution of driver and customer ratings and their trends over time.

Design and Theming
The dashboard was designed for a professional look and feel by:

Implementing a custom, consistent color theme.

Creating a structured layout with a clear header.

Using shadows, borders, and rounded corners to make visuals pop.

Writing clear, descriptive titles for all charts and KPIs.

How to Use This Project
Python Script
Ensure you have Python installed.

Install the required libraries:

pip install pandas matplotlib seaborn

Place the ncr_ride_bookings.csv file in the same directory as the Python script.

Run the script to see the analysis and generate the charts.

Power BI Dashboard
Ensure you have Power BI Desktop installed.

Open the .pbix file.

The dashboard is fully interactive. Use the slicers and click on visuals to filter and explore the data.
