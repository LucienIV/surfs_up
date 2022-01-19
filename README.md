# surfs_up

## Overview
### Purpose of Analysis
The purpose of this analysis is to gather temperature data for the months of June and December in Oahu and utilize the data to determine the sustainability of a surf and ice cream shop in the area year-round.

## Results
### Key Points
The summary statistics for the months of June and December are respectively as follows:

![image](https://user-images.githubusercontent.com/92831138/150194049-7c17724c-6d93-4b98-aec9-f1fe2199c4ac.png)
![image](https://user-images.githubusercontent.com/92831138/150194066-507e17bd-2e8f-4947-b419-bbc4c1bb2376.png)
- The biggest takeaway from the results of the analysis is that there is very little difference in the mean temperature for the two months analyzed. The two values are within four degrees of each other.
- The month of December had a lower minimum temperature than June. While June had a lowest recorded temperature of 64 degrees, December had a lowest recorded temperature of 56 degrees.
- Interestingly, the highest recorded temperatures for each month were almost exactly the same. June and December had a highest recorded temperature of 85 and 83 degrees respectively.

## Summary
### Summary of Results
The results of the analysis would indicate that the proposed business is indeed sustainable year-round. Even in December, generally considered one of the coldest months of the year, the temperature did not drop below 56 degrees in any of the years observed. As this is still 20 degrees above freezing, the temperature of the region should prove no obstacle to the development of a business built around warm weather. Other considerations could be examined by further queries. For example, modifying the query for each month to be `session.query(Measurement.date, Measurement.prcp).filter(Measurement.date.like('%-06-%'))`, changing the filter dependent on months being analyzed, would allow for analysis of the precipitation in a given timeframe to determine if there are any worrying trends. Even if temperatures stay warm, overly rainy periods of time could also impact the proposed business. Additionally, as the dataset has information for which weather stations collected each measurement, one could set a filter on the basis of station in the query with a method like `filter(Measurement.station == _______)` with the blank space being the desired station to limit the search to a singular station and maybe fine tune the results based on a certain region of Oahu.
