# UK-TRAIN-RIDES-ANALYSIS
An excel file showing train ticket data for National Rail in the UK, from Jan to Apr 2024, including details on the type of ticket, the date &amp; time for each journey, the departure &amp; arrival stations, the ticket price, and more. The goal is to derive actionable insights and provide recommendations to optimize overall operational effectiveness.

[<img width="1251" height="587" alt="DASHBOARD" src=](https://github.com/user-attachments/assets/da76c74f-365d-44c1-abe1-0693ca515d68)

### Table of Contents
- Project Overview
- Project Scope
- Project Objectives
- Expected Outcome
- Document Purpose
- Use Case
- Data Source
- Data Cleaning and preprocessing
- Data Analysis
- Data Visualization
- Recommendation
- Conclusion

### Project Overview
This project involved analyzing mock train ticket data for the National Rail in the UK from January to April 2024. The dataset included details on ticket types, journey dates and times, departure and arrival stations, ticket prices, and more. The aim of this project is to create an exploratory dashboard to help identify popular routes, peak travel times, analyze revenue from different ticket types and classes, and diagnose on-time performance and contributing factors. The insights generated aim to support management decisions in scheduling, promotions, and service optimization.

### Project Scope
This project focuses on analyzing historical ticket sales data to identify revenue trends and patterns, while examining passenger demographics, ticket types, and payment methods. It also aims to identify underperforming routes, ticket classes, and time periods, providing actionable recommendations to enhance revenue and improve overall service efficiency.

### Project Objectives
The objectives of this project are to:

-	Analyze railway transaction data to identify trends and patterns.
-	Evaluate the performance of different ticket types, payment methods, and routes.
-	Identify peak and off-peak travel times to optimize scheduling.
-	Provide actionable recommendations to increase revenue and operational efficiency.
-	Develop interactive dashboards for monitoring and decision-making.

### Expected Outcomes
The analysis aims to provide actionable insights including:

-	Daily Travelers Count
-	Identification Of Peak hours
-	Average delay time
-	Identification of Top Routes
-	Seasonality In Sales
-	Revenue Analysis
-	Recommendations on service optimization and promotional strategies.

### Document Purpose
This report provides a comprehensive analysis of railway ticketing data, presenting key insights and trends in ticket sales and revenue. It highlights operational inefficiencies and underperforming areas, offers actionable recommendations to support decision-making and strategic planning, and serves as a reference document for stakeholders and management.

Use Case
Stakeholders Benefiting from the Analysis
1. Railway Management and Executives
   
•	***Decision-Making Support:*** Provides insights into ticket sales trends, route performance, and travel patterns to guide strategic planning.

•***Revenue Optimization:*** Identifies high-demand routes and underperforming routes, enabling targeted promotions and pricing strategies.

2. Operations and Scheduling Teams
   
•***Schedule Optimization:*** Helps plan train schedules effectively by identifying peak and off-peak travel times.
•	***Resource Allocation:*** Supports better allocation of staff and train resources to reduce delays and improve service reliability.

3. Marketing and Sales Teams
   
•	***Targeted Campaigns:*** Enables the creation of promotions and loyalty programs based on passenger behavior, ticket type, and travel times.
•	***Revenue Growth:*** Helps increase ticket sales for off-peak hours and underperforming routes through data-driven campaigns.

4. Finance and Revenue Teams
   
•***Revenue Tracking:*** Provides insights into revenue trends by route, ticket type, and payment method for better forecasting.
•***Pricing Strategies:*** Supports pricing adjustments to maximize revenue and optimize train utilization.

5. Customer Service Teams
   
•***Passenger Satisfaction:*** Identifies routes or times with frequent delays or refunds, allowing teams to proactively address issues and improve service.

This comprehensive analysis equips all stakeholders with actionable insights to enhance operational efficiency, increase revenue, and improve passenger experience


### Data Source
The dataset used for project is sourced from [Maven analytics website](https://app.mavenanalytics.io/datasets?search=train) designed specifically for practice purpose. It is presented in an Excel file with 540,411 rows and 18 columns respectively. The dataset includes key attributes essential for a comprehensive analysis such as;

Field Description
-	Transaction ID: Unique identifier for an individual train ticket purchase
-	Date of Purchase:	Date the ticket was purchased
-	Time of Purchase:	Time the ticket was purchased
-	Purchase Type: Whether the ticket was purchased online or directly at a train station
-	Payment Method: 	Payment method used to purchase the ticket (Contactles, Credit Card, or Debit Card)
-	Railcard: Whether the passenger is a National Railcard holder (Adult, Senior, or Disabled) or not (None).  Railcard holders get 1/3 off their ticket purchases.
-	Ticket Class: Seat class for the ticket (Standard or First)
-	Ticket Type: When you bought or can use the ticket. Advance tickets are 1/2 off and must be purchased at least a day prior to departure. Off-Peak tickets are 1/4 off and must be used outside of peak hours (weekdays between 6-8am and 4-6pm). Anytime tickets are full price and can be bought and used at any time during the day.
-	Price: Final cost of the ticket
-	Departure Station: Station to board the train
-	Arrival Destination: Station to exit the train
-	Date of Journey: Date the train departed
-	Departure Time: Time the train departed
-	Arrival Time: Time the train was scheduled to arrive at its destination (can be on the day after departure)
-	Actual Arrival Time: Time the train arrived at its destination (can be on the day after departure)
-	Journey Status: Whether the train was on time, delayed, or cancelled
-	Reason for Delay:	Reason for the delay or cancellation
-	Refund Request: Whether the passenger requested a refund after a delay or cancellation

### Data Cleaning and Preprocessing

Having clean data for analysis is essential because it ensures that the insights are accurate, reliable, and free from errors. Clean data makes the analysis process smoother, helping researchers, analysts, and decision-makers draw meaningful conclusions and make informed decisions based on trustworthy information. After carefully reviewing the dataset for quality and suitability including checks for errors, inconsistencies, missing values, and duplicates, I found that the dataset is well-structured and consistent. The only area requiring adjustment was the ‘Reason for Delay Column’. Instead of leaving blanks, I replaced missing values with Not Applicable to ensure completeness and avoid gaps that could disrupt analysis.
The dataset follows a standard format and uses consistent naming conventions. All required fields are present and properly filled in. The values are accurate, and each column contains the appropriate data type. Most importantly, there are no duplicate records. Based on this detailed review, the dataset is well-prepared and ready for analysis, ensuring that any insights gained will be accurate, reliable, and trustworthy.

***ADDITION OF NEW COLUMNS***

Several new columns were created to improve the dataset and allow for deeper analysis of journey performance and customer behaviour. These include:

- ***Year:*** Extracted from the journey date, this column supports time-based trend analysis across different years.
- ***Month:***  This column enables the examination of journey patterns and revenue trends by month.
- ***Day:***  Captures the specific day of the week to identify peak daily sales/revenue.
- ***Route:***  Created by combining the departure and arrival stations, this column helps with route-based performance and revenue analysis.
- ***Delay Time:***  Calculated as the difference between the actual arrival time and scheduled arrival time, this column is essential for delay analysis and performance assessment.
  
These added fields support the evaluation of travel behaviour, seasonality, customer patterns, and operational efficiency. They also enable deeper insights into performance across time periods, regions, and travel routes.
By expanding and enriching the dataset with these new columns, I have created a more detailed foundation for dashboard development and data storytelling, ensuring more precise analysis and stronger insights.

### DATA ANALYSIS AND INSIGHTS

The primary aim of this analysis is to derive valuable insights from UK Train Rides data by conducting a comprehensive examination of key business indicators. This analysis focuses on several critical objectives. Firstly, it aims to identify how many train rides occurred and how revenue was generated across different routes, enabling an understanding of operational efficiency and route performance. Secondly, the analysis seeks to determine the primary causes of train delays and the level of punctuality achieved, helping to assess service reliability. Thirdly, it aims to analyze customer ticket preferences, including ticket type, ticket class, Railcard usage, and payment method choices. Finally, this analysis seeks to determine peak travel hours and understand how customer behaviour varies across different periods of the day.

***Key benefits include:***
- Operational Efficiency: Helps allocate resources and staffing to peak travel periods.
  
- Customer Insights: Identifies behavioural patterns, preferred ticket types, and Railcard usage.
  
- Financial Planning: Supports route profitability planning and revenue improvement strategies.
  
- Strategic Decision-Making: Informs pricing, route scheduling, delay intervention, and marketing campaigns.
  
- Customer Experience: Enhances punctuality management, ticketing options, and payment flexibility.
  
  As a result, this analysis provides insights addressing the following questions:
  
**1. How many train rides do we have, and how much revenue was generated?**

The total number of train rides recorded in the data is 31,653 generating a total revenue of £741,921.
This demonstrates a strong commercial performance and confirms widespread rail usage across multiple routes in the UK. With thousands of rides completed, the dataset reflects a reliable customer demand base for rail transportation services.

[<img width="897" height="76" alt="KPIS" src=](https://github.com/user-attachments/assets/bdae40ed-b8b0-4ac7-9be4-072fd01448ab) 


**2. What are the peak travel times?**
The objective of this question is to identify the periods of the day during which the rail system experiences the highest travel activity. To achieve this, the hour field was placed in the row section of the pivot table and the count of rides was calculated and visualised in a bar chart.
From the analysis:
•	6AM – 8AM recorded the highest travel volume.
•	The evening period around 4 PM to 6 PM maintained strong activity.
This indicates that demand is highest during morning and evening periods, likely due to work, school schedules, and leisure travel 
patterns.

[<img width="1254" height="142" alt="Peak Travel Times" src=](https://github.com/user-attachments/assets/935e0a37-c743-4e4e-bd2e-389c7bebe422)


**3. What is the daily sales revenue?**
The objective of this question is to idemtify how revenue changes acrooss each day of the week,helping to identify sales pattern, demand behaviour, and effective operational planning.

From the analysis:

- Wednesday generated the highest revenue ( £111,177 )
This suggests increased movement mid-week, possibly linked to business travel or commuting cycles.

- Saturday recorded the lowest revenue ( £95,940 )
This indicates lower weekend travel activity, likely due to reduced work-related movement.

- Sunday also remained below average ( £100,052 )
Showing quieter travel demand at the start of the week.

- Revenue increased sharply from Sunday to Wednesday, decreased on Thursday, recovered on Friday, and fell on Saturday.

[<img width="522" height="135" alt=Daily Sales Trend" src=](https://github.com/user-attachments/assets/d2b0ae30-497a-4486-a67c-ba75b0b6e3bb) 


**4. What are the main factors contributing to train delays?**
The purpose of this analysis is to understand why delays occur and how they affect operational efficiency. Using the reason for delay field, trains were grouped and counted to show the most common causes.
From the analysis:

-	Weather conditions recorded the highest delay count.

-	Technical issues and signal failures also contributed significantly.

-	Other causes included staff shortage and train faults, though at lower levels.

- This indicates that delays are driven primarily by infrastructure and environmental factors.

[<img width="267" height="339" alt="Main Contributing Factors" src=](https://github.com/user-attachments/assets/369ec9f1-1bc1-458d-acb3-bc88c6b8d048)


**5. Which routes generated the most revenue?**
Revenue by route was evaluated to determine which travel paths are most profitable. Using a pivot chart, the route field was placed in the rows section while revenue was summed.
From the analysis:

Top routes include:
-	London Euston → Manchester Piccadilly

-	Birmingham New Street → London Euston

-	Manchester Piccadilly → London Euston

Underperforming routes generated significantly lower revenue, likely due to shorter distance, lower ticket cost, or reduced customer demand.

This shows that the business relies heavily on major city-to-city routes for earnings.

[<img width="439" height="342" alt="Revenue By Route" src=](https://github.com/user-attachments/assets/2c6f3610-00a6-4d7d-88d0-3463b0369f9c)


**6. Which ticket types and classes are most preferred?

Customer ticket preferences were analyzed using ticket type and class fields.
**Ticket Type Analysis:

-	Advance tickets generated the highest share of revenue at 31.01%.

-	Off-peak tickets followed closely at 27.21%.

[<img width="275" height="153" alt="Revenue By Ticket Types" src=](https://github.com/user-attachments/assets/597707ca-b42a-43d1-bae6-67160baebc4c)


**Ticket Class Analysis:
-	Standard class contributed 79.89% of total revenue.
-	First class contributed 20.11%.
This shows that most customers prioritize value and affordability.

[<img width="249" height="157" alt="Revenue By Ticket Class" src=](https://github.com/user-attachments/assets/ff8c43ae-fc73-40ef-8465-76e816a5a80b)

**7. How did Railcards contribute to revenue?**
   
Railcard analysis helps determine customer profile segments and pricing advantages.

From the dashboard:

-	Adults produced the highest percentage of revenue.
-	
-	Disabled and Senior Railcards contributed steady revenue levels.
-	
This reflects a diverse customer base with strong utilization of discount schemes.

[<img width="279" height="177" alt="Revenue By Railcard" src=](https://github.com/user-attachments/assets/dda6f199-a61f-41c2-bf92-d1cb7001729b)


**8. What payment methods do customers prefer?**
Payment method data reveals transaction habits and technology usage levels.

From the analysis:

-	Credit cards accounted for most revenue transactions.
  
-	Contactless were also widely used.
  
-	Debit cards were the smallest share.
  
This shows that most customers still prefer direct card payments, providing opportunities to grow digital ticketing.

[<img width="248" height="180" alt="Revenue By Payment Method" src=](https://github.com/user-attachments/assets/a783e2b7-c274-44aa-8bed-9a5289b067ea)


###Recommendations
Based on the analysis above, several strategic recommendations are proposed:
-	Prioritize staffing and customer support during peak hours, particularly between 6 AM – 6 PM, to handle the highest passenger volume.
  
-	Increase staff and train capacity 6AM – 6 PM to maintain service quality.
  
-	Reduce operating frequency early mornings and late nights to optimize cost

-	Prepare for increased travel activity on busiest routes such as London → Manchester and Birmingham → London.
  
-	Use pricing strategies, marketing, and scheduling adjustments to boost ridership. For consistently low-value routes, review timetable efficiency and service frequency to reduce unnecessary operating costs.
  
-	Plan preventive maintenance before peak periods.
  
-	Increase inspection and maintenance frequency to reduce technical and signal delays.

-	Improve weather monitoring systems to anticipate weather-related disruption.

-	Strengthen staffing arrangements to prevent shortage-related delays.

-	Continue promoting Advance and Off-Peak tickets, as they are most profitable and widely used.

-	Advertise Standard class travel benefits since it attracts the highest volume of customers.

-	Introduce digital booking incentives to increase online payment adoption

-	Evaluate weaker revenue routes to determine whether to adjust train frequency, timing, or marketing strategy.

-	Promote Railcard options to encourage loyalty and repeat purchases.

-	Increase marketing efforts and consider introducing new railcard types to attract more passengers.

-	Improve real-time information updates for delayed services

-	Regularly adjust train schedules based on travel patterns and gather passenger feedback to improve services.

###Conclusion	
This analysis provides a comprehensive understanding of railway ticket sales, passenger behavior, and operational performance. The insights generated identify high- and low-performing routes, peak travel times, and revenue drivers. Implementing the recommended strategies can improve revenue, optimize operations, and enhance customer experience. The interactive dashboards provide management with a practical tool for continuous monitoring and data-driven decision-making. Thank you for reading

I am interested in a Data Analyst role where I can showcase my skills, turn raw data into insights, continue to learn, an organization I can grow with,where my work will make an imoact to the organization
You can reach me on oluwatoyosiadesetan@gmail.com

THANK YOU!



