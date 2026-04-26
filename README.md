# Rapido-sales-Analysis
1. Project Overview
This project focuses on analyzing Rapido ride data to understand city performance, fare trends, and ride demand over time.
 The analysis was performed using Excel for data preparation and Power BI for data visualization and dashboard creation.
The goal of the project is to transform raw ride data into meaningful business insights that support better decision-making.    
   
2. Project Objectives
The main objectives of this project are:
Analyze city-wise ride performance
Study fare and revenue distribution
Analyze ride demand over time
Create interactive dashboards for business users

  3. Tools and Technologies
 Microsoft Power BI Desktop
 DAX ( Data Analysis Expression )
 Data Modeling using star schema
 Excel / Database as data source
        



  4. Data Model 
The dashboard follows a star schema consisting of one fact into several dimension tables.
Fact Table :  Contains transaction data such as city , customer name , driver id , fare INR, Payment method 

City wise Dim :  Includes Pickup location, Drop location , Ride duration .

Fare Dim : Contains , Ride distance , Ride duration , Payment Method .

Time Dim:  Includes , Rider ID , Ride Date , Ride Time.

  5. Key Measures
Total Revenue = SUM(Rides[Fare])
Avg Fare = AVERAGE(Rides[Fare])
Revenue per Ride = DIVIDE([Total Revenue], [Completed Rides], 0)
Total Distance = SUM(Rides[Distance_km])
Avg Distance = AVERAGE(Rides[Distance_km])
Active Riders = DISTINCTCOUNT(Rides[RiderID])
Avg Revenue per Day =DIVIDE([Total Revenue],DISTINCTCOUNT(Rides[Date]), 0)
Month Name = FORMAT(Rides[Date], "MMMM")
Revenue per Km =DIVIDE([Total Revenue], [Total Distance], 0)
Total Trips = DISTINCTCOUNT(Trips[TripID])
Total Fare = SUM(Trips[Fare])
Total Duration (Min) = SUM(Trips[DurationMinutes])
6. Key Visualizations
The following visuals were created in Power BI:
KPI Cards:
Total Trips
Total Fare
Average Fare
Total Duration
Bar Chart:
City-wise total fare
Line Chart:
Daily/Monthly trip trends
Map Visualization:
Ride distribution across cities
Scatter Plot:
Distance vs Fare relationship 
7. Conclusion
The analysis of Rapido bike taxi data provides meaningful insights into customer behavior, revenue patterns, and operational efficiency. These insights can help improve pricing strategies, optimize driver allocation, and enhance business growth.
