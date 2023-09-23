# Hurricane Tracking and Trending Project

# Table of Contents
- [Overview](#overview)
  - [Data](#data)
  - [NOAA csv files](#noaa-csv-files)
  - [Time Period](#data-time-period)
  - [Installation](#installation)
- [Introduction](#introduction)
- [Data Cleaning and Discussion](#Data-Cleaning-and-Discussion)
- [Time Series Analysis](#Time-Series-Analysis)
- [Wind Speed and Air Pressure Correlation](#Wind-Speed-and-Air-Pressure-Correlation)
- [Hurricane Tracking](#Hurricane-Tracking)
- [Thematic Mapping](#Thematic-Mapping)
- [Contributing](#Contributing)

## Overview

We would like to track historical hurricane paths and find countries that are prone to hurricanes. We would also like to find patterns and trends regarding the speed, atmospheric pressure and seasonality of hurricanes over time.

### Data: 
National Oceanic and Atmospheric Administration

### NOAA csv files
https://www.ncei.noaa.gov/data/international-best-track-archive-for-climate-stewardship-ibtracs/v04r00/access/csv/

### Time Period:
1922 - 2022

### Installation:
- Kaleido
- Pandas
- Plotly
- Matplotlib
- geo.py

## Introduction

Hurricanes, as a natural phenomenon, can be a powerful and destructive force on Earth. For this project, our group used Tropical Storm data from the International Best Track Archive for Climate Stewardship (IBTrACS), a project of the World Meteorological Organization(WMO), and accessed through the National Oceanic and Atmospheric Administration(NOAA) database. This data was used to analyze trends and patterns as well as to find areas prone to hurricanes. We looked at specific hurricane characteristics such as air pressure and wind speed to determine whether hurricanes are becoming more intense. Finally, we will use hurricane point data to determine if hurricane frequency is increasing over time.

We set out to answer the following questions. 

- Are hurricanes increasing in frequency  and intensity over time?
- Are there any trends or patterns of wind speed and air pressure in regards to hurricanes in the North Atlantic Basin?
- What can we learn from tracking hurricanes?
- What countries surrounding the west Pacific basin were most susceptible to hurricanes and by how much?

## Data Cleaning and Discussion

The data available through the NOAA was extensive, encompassing all oceanic basins that experience Tropical Storms, going back in some cases as far as 1842. We chose to work with the last 100 years of data, from 1922-2022, from three most impacted basins. We assigned one to each group member as follows:

Western Pacific Ocean - Ron Briggs
Northern Atlantic Ocean  - Leif Munroe
North Indian Ocean - Ghislain Nyirumuheto

The Dataset for the North Atlantic Basin was the most complete, with the greatest amount of data captured for Wind Speed(knots) and Air Pressure(mb) over our chosen 100 year time frame. This allowed for more statistical analysis to be done, and with greater accuracy. 

## Time Series Analysis

Are hurricanes increasing in frequency  and intensity over time?

To answer the first question, we created a set of time series maps showing the location of each hurricane every 3 hours based on latitude and longitude, providing a high level snapshot of hurricane occurrences in each basin over time. Based on the increased dot density and the growing area of hurricane coverage, we can conclude that hurricanes are generally increasing in frequency between 1922 and 2021 in the West Pacific Basin.

To answer the question of frequency in more statistical detail, time series graphs were created to show the number of storms occurring each year. 
These “Number of Storms per Year” graphs of the North Atlantic Basin show an overall increase in the total number of storms occurring in that region between 1922-2022. The same data plotted in scatter format allows us to quantify this observation, showing a moderate positive correlation with an r-value of 0.491. This confirms the qualitative observations suggesting that the number of storms is increasing over time. 

![Hurricanes (1922-1931)](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Pacific/Fig_1922_1931.png?raw=true)

![Hurricanes (2012-2021)](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Pacific/Fig_2012_2021.png?raw=true)

## Wind Speed and Air Pressure Correlation

Are there any trends or patterns of wind speed and air pressure in regards to hurricanes in the North Atlantic Basin?

To answer this question, the Wind Speed and Air Pressure data for the North Atlantic Basin was graphed to determine trends in the data. First the two sets of values were plotted against one another the “Wind Speed vs Air Pressure” graph, showing a strong negative correlation between the two. The graph shows that lower air pressure results in higher wind speeds, which correlates to a higher categorization on the Saffir-Simpson Scale, or in other words a more intense storm. 

![Wind Speed Vs Air Pressure](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Atlantic/windvair.png?raw=true)

Next we plotted the change in both variables over time, averaged by year. The  “Wind Speed Change over Time” graph shows that there is a strong negative correlation between average wind speed and year with an r-value of -0.714. In other words, the average wind speed is declining over time. The “Air Pressure Change over Time” graph shows a corresponding increase in average air pressure over 100 years, with a moderate positive correlation and r-value of 0.664. 

![Wind Speed Change over Time](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Atlantic/windspeed.png?raw=true)

![Air Pressure Change over Time](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Atlantic/airpressure.png?raw=true)

To investigate the question of intensity in more detail, the data was grouped based on the Saffir-Simpson Hurricane Scale, which categorizes storm intensity based on wind speed,  ranging from Tropical Storm (>64 knots) to Category 5 Hurricane (<137 knots). A series of pie charts “Storm Categories for Decade x” were created to show the percent of total storms in each category for each decade. A stacked bar graph “Storm Categories by Decade” shows the same data for all decades on one chart. In both formats, it’s clear that the percent of Tropical Storms has been increasing over time, from just 27% of total storms in the 1920’s to just over 79% of the total in the 2010’s. Taken together with the “Wind Speed Change over Time” and the “Air Pressure Change over Time” graphs, this could suggest that the average intensity of all storms across a given year is decreasing at least in part because of an increasing number of these less intense Tropical Storms.

![Storm Categories by decade](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Atlantic/storm_categories.png?raw=true)

Finally we plotted “Max Wind Speed per Year”, which shows a weak positive correlation based on an r-value of 0.321. This suggests that there is an increase in intensity at the top end of the intensity spectrum. 
All together, this snapshot of the North Atlantic basin over the last 100 years points to an increase in the number of storm events, particularly Tropical Storms, over time. It suggests that the most intense storms may be increasing in intensity, but more analysis is needed to understand these relationships. 

![Max Wind Speed](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Atlantic/storm_categories.png?raw=true)

## Hurricane Tracking

What are the longest hurricanes by time in a given year?

In order to answer this question, two polyline maps of the 10 longest hurricane paths were created.  These were all located in the West Pacific Basin and the selected years were 1952 and 2022.  The maps of hurricanes paths are shown below:

![Hurricanes Paths (1952)](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Pacific/Tracks_1952.png?raw=true)

![Hurricanes Paths (2022)](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Pacific/Tracks_2022.png?raw=true)

The resulting maps clearly shows what the longest hurricanes are. The data was presented in a map rather than a list because the map shows more context, such as the path of the hurricane.  You can also see which countries are affected by each hurricane.

What can we learn from tracking hurricanes?

Broadly speaking, we can make several conclusions based on reading these maps. First, we can see that powerful hurricanes that do not make landfall may not cause significant destruction.  We can also identify trends.  We can see from the maps that hurricanes tend to track towards higher latitudes.  Also, path analysis shows the unpredictability of hurricanes.  For example, we can see that hurricane Hinnamnor radically changes direction in the Philippine Sea. Finally, we can see how landfall locations reveal areas most prone to destructive impacts.

## Thematic Mapping

What countries are most susceptible to hurricanes and by how much?

Based on information from the NOAA, we learned that land masses can be affected by hurricanes as far as 111.12km from shore. We calculated all the hurricane points found within this radius.  After, we totalled the count for each country and then created choropleth maps to show the 10 most susceptible countries in 1952 and 2022.

![Proximity Counts of Hurricanes (1952)](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Pacific/Countries_1952.png?raw=true)

![Proximity Counts of Hurricanes (2022)](https://github.com/rkb81/Hurricane-Tracking-Project/blob/main/North_Pacific/Countries_2022.png?raw=true)

In summary, we can see that that China and the Philippines are the two hardest hit countries in the Western Pacific basin in 1952 and 2022 respectively. Additionally, we can see that as we move farther west from the Pacific Ocean, we see that countries are less susceptible to hurricanes (such as Laos and Myanmar).

## Contributing

- Ron Briggs
- Leif Munroe
- Ghislain Nyirumuheto

