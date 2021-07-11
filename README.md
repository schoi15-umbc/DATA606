# Air Quality Analysis
![1600px-Air_pollution_banner_Smog_in_Warsaw](https://user-images.githubusercontent.com/70929605/125210145-d520b280-e26b-11eb-99fd-f3829fc825e3.jpg)


## Introduction
Saving and protecting our environment is a key topic these days. Every issue of pollution is important and essential in our ecosystem. Out of many factors, air is essential to life and the quality of air can highly effect our health. Every year, millions of Americans suffer from adverse health impacts liked to air pollution, an d tens of thousands have their lives cut short. This project focuses on air pollution with the retrieved air data. 

*So what is Air data?*

The United States Environmental Protection Agency (EPA) provides access to air quality data (primarily from Air quality system (AQS) database) collected at outdoor monitors across the United Sates, Puerto Rico, and the U.S Virgin Islands. The data can be used to view, create visuals and graphical displays, investigate monitor locations, and so on. It is accessible to the public and can be downloaded by hourly, daily, and annual concentration data, AQI data, and speciated particle pollution data.

<pre>
Phase 1 :  <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%201/Phase1.pptx>Power Point</a> / <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%201/Phase1_EDA.ipynb>EDA</a> / Youtube</a>
Phase 2 :  <a href=>Power Point</a> / <a href=>EDA and Model Construction</a> / Youtube</a>
Phase 3P: <a href=>Power Point</a> / <a href=>EDA</a>Execution and Interpretation	 / Youtube</a>
Executive Code  : <a href=>Executive Notebook </a> </a>

</pre>


## Data Set 

### Overview
The Data set is retrieved from [United States Environmental Protection Agency (EPA).](https://aqs.epa.gov/aqsweb/airdata/download_files.html#Daily)

EPA has annual datasets from 1980 - 2021 (as of 2021-05-18) categorized by concentration by monitor, Air Quality Index (AQI) by Core Based Statistical Areas (CBSA), and AQI by County. 
Each daily summary file contains data for every monitor (sampled parameter) in our database for each day. These files are separated by parameter (or parameter group) to make the sizes more manageable.
This file will contain a daily summary record that is:
1) The aggregate of all sub-daily measurements taken at the monitor.
2) The single sample value if the monitor takes a single, daily sample (e.g., there is only one sample with a 24-hour duration). In this case, the mean and max daily sample will have the same value.

The daily summary files contain (at least) one record for each monitor that reported data for the given day. There may be multiple records for the monitor if:
- There are calculated sample durations for the pollutant. For example, PM2.5 is sometimes reported as 1-hour samples and EPA calculates 24-hour averages.
- There are multiple standards for the pollutant (q.v. pollutant standards).
- There were exceptional events associated with some measurements that the monitoring agency has or may request be excluded from comparison to the standard.
(Information taken from [website](https://aqs.epa.gov/aqsweb/airdata/FileFormats.html)) 

### Data Elements
The images on the left shows the 29 columns within the dataset, along with the description for each. 
Out of the 29 elements, the ones that will be used in our project are Features:
- State code
- County code
- Observation Count
- Observation Percent
- Arithmetic mean
- AQI
- 1st Max Value

#### Target variable: AQI
### Unit of measure
Ozone, carbon monoxide: Parts per million

Nitrogen dioxide (NO2), Sulfur dioxide :Parts per billion

Daily Summary dataset for Ozone (44201) 2020 contains 391,923 Rows, 24 Columns, and is  3,127 KB. It contains numerical and categorical data.
Daily Summary dataset for Sulfur dioxide (SO2 (42401)) 2020 contains 324,817 Rows, 24 Columns, and is  4,357 KB. It contains numerical and categorical data.
Daily Summary dataset for Carbon Monoxide (CO (42101)) 2020 contains 178,789 Rows, 24 Columns, and is  1,784 KB. It contains numerical and categorical data.
Daily Summary dataset for Nitrogen dioxide (NO2 (42602)) 2020 contains 157,726 Rows, 24 Columns, and is   2,159 KBv. It contains numerical and categorical data.

## Hypothesis / Research Question(s)
1) How is air pollution different by state/county?
2) Which model will give us the most accurate analysis of categorizing into various clusters to see how the pollution is distributed geographically?
3) What are some solutions for the different clusters? 

Datasets for all four types of pollution (ozone, sulfur dioxide, carbon monoxide, and nitrogen dioxide) will be used to find answers to the research questions, along with comparing the AQI for the different types of pollution.
