# Excel.MT.Tourism
 
## Quick Links:
### Data: Raw data located in main repository

## Introduction
This project focuses on geo data that tracks the movement patterns and travel behavior of visitors to different locations within the state of Montana. Your company provides data-driven insights to help destination marketers, travel brands, and organizations understand visitor behavior, measure the impact of marketing efforts, and make informed decisions to optimize return on ad spending.  

## Objective
As a remote analyst specializing in location-based analytics for the travel and tourism industry, our goal is to deliver actionable insights to county-level clients in the U.S. to enhance their tourism marketing strategies and maximize ad spend returns. 

## Tools used in Analysis
- Data Cleaning & Analysis: Microsoft Excel 
- Visualization: Tableau Public
- Presentation: Power Point 

### Ask Phase:
To address the business task of understanding visitors travel trends, lets ask some questions to guide our analysis:

- High-Volume Origin Locations
- Score-based system by origin market for volume and length of stay 
- Weekday vs. weekend visitation trends
- Top average stay durations per origin market
- Top average stay durations per arrival market
- In-state vs. out-of-state visitation trends
  
### Prepare Phase:
- The dataset used for this project focuses on visitaion trends for January 2018, and January and February of 2019.
- The original dataset contains 7 columns with 7,435 rows related to visitation trends into the state of Montana. 
- Each column provides limited information about each visit, including:
    - Arrival Date, Origin_City, Arrival_County, Arrivals_Volume, Avg_Distance_to_Arrival_Miles, Avg_length_of_stay_county_minutes, Avg_length_of_stay_MT_minutes

### Process Phase:
#### Data Cleaning and Transformation in Excel:

During the process phase, the data cleaning steps were carried out in Microsoft Excel. The following actions were performed: 
- **Validating Column Values:** 44 files removed where Origin_City = Arrival_County
- **Removing Data:** Stays less than 4 hours (277), and trips less than 50 miles (16), were removed.
- **Creating Score-Based System:** The Column "Combined_Score" was added to provide a balanced emphasis on volume of visitors and duration of stay. The following formulas were used: (E2 - MIN($E$2:$E$7390)) / (MAX($E$2:$E$7390) - MIN($E$2:$E$7390)) to normalize arrival volume. (J2 - MIN($J$2:$J$7390)) / (MAX($J$2:$J$7390) - MIN($J$2:$J$7390)) to normalize length of stay in MT. Then the two columns were aded to create the Combined Score Value. 
- **Adding the Sum_Arrivals_by_City Column:** A new column named "Sum_Arrivals_by_City" was added to include the sum of arrivals by each city. The formula SUM(IF(C2=C:C,E:E)) was used.
- **Adding the Sum_Arrivals_by_County Column:** A new column named "Sum_Arrivals_by_County" was added to to include the sum of arrivals by each county. The formula SUM(IF(D2=D:D,E:E)) was used.
- **Adding the Avg_length_of_stay_per_county_days Column:** A new column named "Avg_length_of_stay_per_county_days" was added to to include the average length of stay per visitor in each county. The formula AVERAGE(IF(D2=D:D,I:I))/1440 was used.
- **Adding the Avg_length_of_stay_MT_days Column:** A new column named "Avg_length_of_stay_MT_days" was added to include the average length of stay per visitor in each county. The formula AVERAGE(IF(D2=D:D,K:K))/1440 was used.
- **Adding Arrival_Day** A new column named "Arrival_Day" was added to convert mm/dd/yyyy format to weekday format. The formula used WEEKDAY(A2,2) was used along with find and replace for the digits with the day of the week. 
- **Changing Minutes to Days:** Changed Avg_length_of_stay_county_minutes and Avg_length_of_stay_MT_minutes to days with the following formula, G2/1440. 
- **Sorting the Table:** The table was sorted in ascending order based on the Origin_City column to ensure data consistency.
By cleaning data in Excel, the dataset was refined, inconsistencies were addressed, and the average length of stay information was formatted appropriately for subsequent analysis.


### Analyze Phase:
During the Analyze phase, our objective is to explore the dataset thoroughly, revealing valuable insights and addressing significant discoveries pertaining to the distinct travel patterns of visitors to Montana. Our primary emphasis lies in comprehending their travel behavior and trends, with the ultimate goal of informing marketing strategies aimed at maximizing the clients return on ad spending. To tackle the critical findings, a series of analyses were conducted using Microsoft Excel. 

#### 1. 80% of Arrival Volume originating from 14 cities 

![image](https://github.com/Nick-Sierra/Nick-Sierra.Excel.MT.Tourism/assets/149681943/c8ac6074-c8d4-4b1f-8d01-dc78a6e2bdba)

#### 2. Proportion of Arrivals by Day of the Week

![image](https://github.com/Nick-Sierra/Nick-Sierra.Excel.MT.Tourism/assets/149681943/6591e9e0-bc72-4377-b013-759734159b67)

#### 3. Length of Stay by Arrival Day of the Week

![image](https://github.com/Nick-Sierra/Nick-Sierra.Excel.MT.Tourism/assets/149681943/b92a3d15-c3ea-4e21-90fd-24aacddf3f37)

#### 4. Top 10 Origin Markets by Length of Stay

![image](https://github.com/Nick-Sierra/Nick-Sierra.Excel.MT.Tourism/assets/149681943/2e6bedd7-eb97-4ca5-bef4-8db4f1ec26ea)

#### 5. Top 10 Out of State Visitation 

![image](https://github.com/Nick-Sierra/Nick-Sierra.Excel.MT.Tourism/assets/149681943/49447f3c-aa7f-4f5a-9c7a-dd15918a11ad)


### Share Phase:
In the Share phase, we showcase the insights and discoveries obtained through the examination of the tourism data using Tableau Public, a robust data visualization tool. The analysis uncovered a multitude of significant findings, including:

#### 1. 80% of Arrival Volume originating from 14 cities 



#### 2. Proportion of Arrivals by Day of the Week


#### 3. Length of Stay by Arrival Day of the Week



#### 4.Top 10 Origin Markets by Length of Stay


#### 5. Top 10 out of state visitation


### Act Phase:
#### Key Takeaways: 
Based on my analysis, we've uncovered some valuable insights:

- **In state visitation:** In state visitation accounts for 46% of arrivals
- **Out of state visitation:** Out of state visitors spend on average 1.09 more days in MT. 


#### Strategies to increase visitation trends 

- **Targeted **
