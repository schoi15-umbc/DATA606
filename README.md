# Air Quality Analysis


## Introduction
Saving and protecting our environment is a key topic these days. Every issue of pollution is important and essential in our ecosystem. Out of many factors, air is essential to life and the quality of air can highly effect our health. Every year, millions of Americans suffer from adverse health impacts liked to air pollution, an d tens of thousands have their lives cut short. This project focuses on air pollution with the retrieved air data. 

*So what is Air data?*

The United States Environmental Protection Agency (EPA) provides access to air quality data (primarily from Air quality system (AQS) database) collected at outdoor monitors across the United Sates, Puerto Rico, and the U.S Virgin Islands. The data can be used to view, create visuals and graphical displays, investigate monitor locations, and so on. It is accessible to the public and can be downloaded by hourly, daily, and annual concentration data, AQI data, and speciated particle pollution data.


## Data Set Overview
The Data set is retrieved from United States Environmental Protection Agency (EPA).
EPA has annual datasets from 1980 - 2021 (as of 2021-05-18) categorized by concentration by monitor, Air Quality Index (AQI) by Core Based Statistical Areas (CBSA), and AQI by County. 
Each daily summary file contains data for every monitor (sampled parameter) in our database for each day. These files are separated by parameter (or parameter group) to make the sizes more manageable.
This file will contain a daily summary record that is:
1) The aggregate of all sub-daily measurements taken at the monitor.
2) The single sample value if the monitor takes a single, daily sample (e.g., there is only one sample with a 24-hour duration). In this case, the mean and max daily sample will have the same value.

The daily summary files contain (at least) one record for each monitor that reported data for the given day. There may be multiple records for the monitor if:
- There are calculated sample durations for the pollutant. For example, PM2.5 is sometimes reported as 1-hour samples and EPA calculates 24-hour averages.
- There are multiple standards for the pollutant (q.v. pollutant standards).
- There were exceptional events associated with some measurements that the monitoring agency has or may request be excluded from comparison to the standard.
(Information taken from website) 
