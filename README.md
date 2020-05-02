# PyBer Analysis Report

## Background and Results

### Purpose
Pyber is actively growing with drivers in many locations providing rides to many different kinds of customers.  To better understand where that growth is occuring and to understand the impact from seasonality, it was important to take a closer look at the data.  The primary focus was on segmenting the market into the type of city, Urban, Suburban or Rural, and then to evaluate how the type of city impacted the total fares and how the fares changed over time for each type.  

## Resources
- Data Source:  city_data.csv, ride_data.csv
- Software:  Python 3.7.7, Jupyter Notebook 6.0.3

What can be said about the summary DataFrame and multiple-line graph with respect to the ride-sharing data among the different city types? Include images of the summary DataFrame table and the multiple-line graph in these results.


### Technical Analysis
There were a number of steps to achieve the analysis; however, overall it necessary to combine the ride informaiton with the city clasifications to be able to properly group the rides by city type.  A summary table performing an overview of the 2019 data was compiled so it could be determined the totals for rides, drivers and fares.  In addition, it was possible to evaluate the average fares per ride and average fares per driver.  From this analysis it can be seen that while the average fares both per driver and per ride and higher for rural cities, the total amount of fares is ten-times larger for urban cities and five-times larger for suburban cities.


|  | Total Rides | Total Drivers | Total Fares | Average Fares per Ride | Average Fares per Driver |
| --- | --- | --- | --- | --- | --- |
|Rural | 125 | 78 | $4,327.93 | $34.62 | $55.49 |
|Suburban | 625 | 490 | $19,356.33 | $30.97 | $39.50 |
|Urban | 1,625 | 2,405 | $39,854.38 | $24.53 | $16.57 |


Once the summary data was collected the next step was to evaluate how the fares changed over time.  To perform that analysis it was necessary to organize the data in a pivot table where the data was indexed by date and each column was sumarized by city type.  To remove the small fluctuations from day-to-day the datetime data was further consolidated so the information was summarized by weeks.  After that it was possible to effectively evaluate the results over time.



### Results
In the below multi-line graph, it can be seen that the fares do have some fluctiation over time; however, there does not appear to be a consistent pattern at differnt times during the month.  In addition, at no point do the total fares for each city type change order of which brings in the most fares.  Consistently urban cities have about double the amount of total fares by $USD than suburban cities, and suburban cities bring in almost five times the amount that rural cities do.  


!["PyBer Fares over time by City Type"](https://github.com/Duegan24/PyBer_Analysis/blob/master/Analysis/Fig8.png)

### Summary

By analyzing the data both from a standpoint of total results and based on changes over time, it was possible to evaluate the impact that the type of city has on number of drivers, number of rides, and total amount of fares.

## Challenges Encountered and Overcome

### Challenges and Difficulties Encountered

During this analysis the primary challenges encountered centered around graphing.  The programming was a consistent progression from material that has already been learned.  I am very familiar with proforming data analysis and there were no issues centered around that aspect of the project.

* Programming
In this project there were some new concepts centered around changing the index so it was a datatime field.  This required some research; however, there were numerous examples in Stack Overflow and so this challenge was easily overcome.

* Data analysis
The data provided for this project was already clean.  If that had not been the case, some of the largest challenges would have been finding acceptable ways to resolve the challenges.

* Graphing, etc
Working through the object oriented plotting of the multi-line graph.  The biggest issue as I had trouble finding ways to set the  size of the figure, initially I kept creating a second plot.  I Googled the problem; however, it was necessary to review multiple responses before I could find one where it was clear how to set the figure size.

### Technical Analyses Used

## Recommendations and Next Steps

### Recommendations for Future Analysis

### Additional Analysis 1

* Description of Approach

* Technical Steps

### Additional Analysis 2

* Description of Approach

* Technical Steps
