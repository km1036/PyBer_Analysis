# PyBer_Analysis

## Overview of the PyBer Analysis

An exploratory analysis was performed for PyBer, a Python-based ride-sharing app company, on data to showcase relationships between type of city, number of riders and drivers, percentage of total fares, riders, and drivers by type of city. Analyses and visualizations were created as informative and collective methods to help executives at PyBer decide how to improve access to ride-sharing services and determine affordability for underserved neighborhoods. 

The original datasets used to develop the code are city_data.csv and ride_data.csv. The programming language used was Python which was enabled in Jupyter Notebook. Pandas, SciPy, and NumPy libraries were used as tools to perform statistical analyses. Matplotlib library was used to create data visualizations such as multiple-line charts from DataFrames in our code. 

## Results

To perform the PyBer Analysis, data was merged from city_data.csv and ride_data.csv to reduce the complexity of data extraction from such large datasets. The data was then combed through for an errors or missing data prior to performing any statistical calculations. 

To obtain the Summary DataFrame code, pictured below, five key metrics were calculated: total riders, total amount of fares, total drivers, average fare per ride for each city type, and average fare per driver for each city type. The cities in the dataset were categorized either into rural, suburban, or urban. The goal of the analysis is to determine the relationship between these key metrics and the city type. The dataframe, "pyber_summary_df", contains key-pairs of various metric calculations and the column name.

<img src="https://github.com/katmarcin/PyBer_Analysis/blob/27f8262af7aedfdbed2aadbb2f2d22178d62d135/analysis/summary%20dataframe.png" width="580" height="200" />

The table for the Summary DataFrame is visualized below when "pyber_summary_df" DataFrame is executed. 

We can determine from the table the following:

* Urban rides make up more than 5 times the number of rural rides and almost 3 times that of surbuban total rides. 
* Urban cities have more than 30 times the number of drivers in rural cities and five times that of suburban cities. 
* Total fares in urban cities are ten times that of rural cities and almost twice the amount of total fares in suburban cities.
* Average Fare Per Ride in rural cities is about $10 dollars more than urban cities and almost $4 dollars more than suburban cities.
* Average Fare Per Driver is 3 times that of rural cities and about a third more than the Average Fare Per Driver in suburban cities.

<img 
src="https://github.com/katmarcin/PyBer_Analysis/blob/27f8262af7aedfdbed2aadbb2f2d22178d62d135/analysis/summary.png" width="580" height="200" />

As a final project, the CEO at PyBer requested a multiple-line chart to compare the relationship between total fare by city type with the timeframe of January 1st, 2019 to April 28th, 2019. In order to do this, a new DataFrame was created with the 'groupby()' function to establish the "date" and "type" columns as the indexes. The 'sum()' method was used to obtain the total fare amount for each date. The index was then reset to allow for the 'pivot()' function to be used to create a table with an established index, column, and value set. 'Loc()' method was used to acquire data from the desired data range. The index was reset one last time prior to using the 'resample()' function to organize our data neatly into weekly bins. Aftering summing the total weekly fares, the data was plotted using the object-oriented interface with a Matplotlib "fivethirtyeight" graph style code. The final result, "Total Fare by City Type," is visualized below. 

<img src="https://github.com/katmarcin/PyBer_Analysis/blob/27f8262af7aedfdbed2aadbb2f2d22178d62d135/analysis/PyBer_fare_summary.png">
 
The PyBer analysis allows us to visualize very significant differences in ride-sharing data among the different city types. It is clear that as an area becomes more urbanized, the average total fare increases consistently across the date range. The month has no effect on the average total fare when cross-comparing the city types as a whole. The highest average total fare for rural cities in the date range was about $500 dollars, for the month of April. For suburban cities, the highest average total fare was about $1450 which was seen in February. That same average was approximately $2500 for urban cities which peaked both at the end of February and beginning of March. By comparing this data, we can deduce urban city total fares could be five times greater than their rural counterparts, while suburban cities remain a stagnant average between these two city types. What all three city types do share is two specific patterns where average total fare rises. This is seen when comparing the end-point averages of two date ranges, January-February and March-April. 

## Summary 


Based on the results from the Summary Dataframe, one can conclude that the 'Average Fare Per Ride' for rural cities may pose a deterrant for riders in that particular city type. Higher fares, and therefore higher demand, may drive rural residents to use means of transportation other than ride-sharing such as a buse or train. This would not be beneficial for the PyBer itself if its aim is to increase affordability for underserved communities, assuming rural cities have less capital average. In order to improve accessibility to ride-sharing services in this city type, it would be beneficial for PyBer to expand on ride-pooling services within the ride-sharing app. When a ride-sharing app provides an option for people to pool rides with up to 4 other riders, the average fare per ride decreases which improves accessibility. The cost for increasing the variety and the number of cars that would be able to provide this service, for instance deploying cars that can service more than 4 passengers simultaneously, would leverage out with the increase in ridership. Most importantly, rural riders would be more satisified with this increase in accessibility. This suggests rural riders are more likely to recommend the PyBer app over others.

Second, to address the very large average fare increases towards the end of February and early March, it would be in the best interest of PyBer to deploy more drivers in those months to decrease the demand and increase the supply of drivers. This would be beneficial for customers all across the city types because affordability churns more ridership. Customers are less likely to use public transportation if they know PyBer will guarantee an affordable on-demand ride. In doing so, customers are more likely to be satisfied with PyBer's service which would be beneficial for the company within the ride-sharing market. The more customers that are happier with PyBer, the more they will choose this app over another ride-sharing app.

Lastly, to really examine, understand, and address disparities among the city types with regard to ridership, it would be beneficial to employ another analysis for each particular city type that would loop in the average number of commuters within each city. People who rely on means other than their own personal car to work make up a critical group of potential riders. If the original PyBer dataset can be modified in the future to include a category for average number of commuters per each city, we can develop three new Summary DataFrames to display average commuter count per city for easy visualization. In doing so, we can determine and provide which particular cities need more access or supply to ride-sharing services for commuters. And when this is done, the demand shifts from buses, trains, and subways to PyBer, the affordable, accessible, and successful ride-sharing app.
