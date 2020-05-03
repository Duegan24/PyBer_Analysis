# PyBer Analysis Report

## Background and Results

### Purpose
Pyber is actively growing with drivers in many locations providing rides to many different kinds of customers.  To better understand where that growth is occuring and to understand the impact from seasonality, it was important to take a closer look at the data.  The primary focus was on segmenting the market into the type of city, Urban, Suburban or Rural, and then to evaluate how the type of city impacted the total fares and how the fares changed over time for each type.  

## Resources
- Data Source:  city_data.csv, ride_data.csv
- Software:  Python 3.7.7, Jupyter Notebook 6.0.3

What can be said about the summary DataFrame and multiple-line graph with respect to the ride-sharing data among the different city types? Include images of the summary DataFrame table and the multiple-line graph in these results.

### Technical Analysis
There were several steps to achieve the analysis; however, overall, it necessary to combine the ride informaiton with the city clasifications to be able to properly group the rides by city type.  A summary table performing an overview of the 2019 data was compiled so it could be determined the totals for rides, drivers, and fares.  In addition, it was possible to evaluate the average fares per ride and average fares per driver.  From this analysis it can be seen that while the average fares both per driver and per ride and higher for rural cities, the total amount of fares is ten-times larger for urban cities and five-times larger for suburban cities.

|  | Total Rides | Total Drivers | Total Fares | Average Fares per Ride | Average Fares per Driver |
| --- | --- | --- | --- | --- | --- |
|Rural | 125 | 78 | $4,327.93 | $34.62 | $55.49 |
|Suburban | 625 | 490 | $19,356.33 | $30.97 | $39.50 |
|Urban | 1,625 | 2,405 | $39,854.38 | $24.53 | $16.57 |

Once the summary data was collected the next step was to evaluate how the fares changed over time.  To perform that analysis, it was necessary to organize the data in a pivot table where the data was indexed by date and each column was sumarized by city type.  To remove the small fluctuations from day-to-day the datetime data was further consolidated so the information was summarized by weeks.  After that it was possible to effectively evaluate the results over time.


### Results
In the below multi-line graph, it can be seen that the fares do have some fluctiation over time; however, there does not appear to be a consistent pattern at differnt times during the month.  In addition, at no point do the total fares for each city type change order of which brings in the most fares.  Consistently urban cities have about double the amount of total fares by $USD than suburban cities, and suburban cities bring in almost five times the amount that rural cities do.  

!["PyBer Fares over time by City Type"](https://github.com/Duegan24/PyBer_Analysis/blob/master/Analysis/Fig8.png)

### Summary
By analyzing the data both from a standpoint of total results and based on changes over time, it was possible to evaluate the impact that the type of city has on number of drivers, number of rides, and total amount of fares.

## Challenges Encountered and Overcome

### Challenges and Difficulties Encountered
During this analysis, the primary challenges encountered centered around graphing.  The programming was a consistent progression from material that has already been learned.  I am very familiar with proforming data analysis and there were no issues centered around that aspect of the project.

* Programming
In this project there were some new concepts centered around changing the index, so it was a datatime field.  This required some research; however, there were numerous examples in Stack Overflow and so this challenge was easily overcome.

* Data analysis
The data provided for this project was already clean.  If that had not been the case, some of the largest challenges would have been finding acceptable ways to resolve the challenges.

* Graphing, etc
The largest challenge I had Working through the object-oriented plotting of the multi-line graph.  The biggest issue as I had trouble finding ways to set the size of the figure, initially I kept creating a second plot.  I Googled the problem; however, it was necessary to review multiple responses in Stack Overflow before I could find one where it was clear how to set the figure size and other attributes of the plot.

### Technical Analyses Used

## Recommendations and Next Steps
As seen in the technical analysis section of this document, it can be observed that rural cities have the fewest number of drivers and riders while having the highest average fares.  This could indicate that there is a potentially underserved market, that the miles driven per trip are longer, that the fare costs are elevated because of percieved value, or a combination of these three or other considerations.  With the current dataset it is difficult to determine what action should be taken and further analysis would be valuable to narrow down cause for the disparities.  Without additional data, it would be recommended to focus on the rural markets and evaluate what impact adding additonal drivers to those cities would have. 

For the next step, I believe it would be important to build a dataset that includes miles driven during the trip and when the trip started and ended.  It would also be useful to collect a dataset that includes a time stamp for when the ride was requested and whether the ride was completed or not, with the reason that the trips were not filled.  From those two additional datasets we can perform additional analysis as outlined below.

### Recommendations for Future Analysis

### Additional Analysis 1

* Description of Approach
Based on the dataset that includes the miles driven during each trip, it will be possible to assess the fare per mile driven for each city type.  This will have the ability to normalize the data in respect to distances.  This is applicable even for urban cities, some urban cities has a high population density, like New York, where it is reasonable to expect that rides will be relatively short in comparison to a city like Houston, where the population density is relatively low and ride distances are likely to be longer.

In addition, cities that have a significant amount of traffic congestion would affect the duration of the ride, which could also be impacting the fare amount.  Traffic congestions is not purely a conditon on urban cities and so should be taken into account when determining what steps to take. 

* Technical Steps
Once the dataset is collected it would be possible to perform a similar analysis to what has been performed earlier in this document, where a summary is made of the data; however, the primary focus will be to evaluate the datasets based on population density by city type (which can be extracted from census data).  Traffic congestion can be measured in a number of differet ways per the Federal Highway Administration (https://ops.fhwa.dot.gov/congestion_report/chapter2.htm) and as such could be a further extension of this analysis if stratgies need to be evluated based on specific cities vs. by city type.

### Additional Analysis 2

* Description of Approach
Based on the data set which would include the time stap of when a ride was requested and whether the ride was completed, including a reason in the case of a trip not filled.  We can use the data to assess whether there are an adequate number of drivers to meet the demand for each city type.  The time stamp data when coupled with the ride dataset requested in the additional analysis 1 would permit us to evaluate how long it takes for a ride to be filled.  Additionally, by evaluating the number and reason for rides that are not completed we can evaluate how many times a ride was not completed because of inadequate number drivers or excessively long wait times.  

By knowing the amount of wait times along with the number of rides canceled because of excessive wait times, we can determine the optimal number of drivers for a given area with a targeted amount of wait time.  In this way, we can see if rural areas are underserved and we can determine if urban areas are overserved.

* Technical Steps
The steps to perform this analysis would involve calculating the wait time for each ride completed, by city type. Calculate the number of rides canceled because of excessive wait times or inadequate number of drivers per city type and then cross plotting that informion for each city, color coding the cross plot with the city type.  In that way we can see if there are patterns to the relationship between city type, wait times, and in adequate drivers.

This data set could be used for further applications and more detailed analysis.  These options could be further evaluated once the additional data is collected and the inital analysis performed above is performed.
