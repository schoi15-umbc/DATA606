# Air Quality Analysis
![1600px-Air_pollution_banner_Smog_in_Warsaw](https://user-images.githubusercontent.com/70929605/125210145-d520b280-e26b-11eb-99fd-f3829fc825e3.jpg)


<pre>

Phase 1 :  <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%201/Phase1.pptx>Power Point</a> / <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%201/Phase1_EDA.ipynb>EDA</a> / <a href=https://youtu.be/ZOv6Nv96m2o>Youtube</a>
Phase 2 :  <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%2002/Phase02.pptx>Power Point</a> / <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%2002/phase2%20.ipynb>EDA and Model Construction</a> / <a href=https://youtu.be/dhbzJ0WItI4>Youtube</a>
Phase 3: <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%2003/Phase03.pptx>Power Point</a> / Youtube</a>
Executive Code  : <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Phase%2003/606_executive_notebook%20.ipynb>Executive Notebook </a> </a>
Executive Power Point:  <a href=https://github.com/schoi15-umbc/DATA606/blob/main/Final_PPT.pptx>Presentation</a>
Executive Video: <a href=https://youtu.be/LF2vlsPykoQ>Youtube</a>

</pre>

## Introduction
Saving and protecting our environment is a key topic these days. Every issue of pollution is important and essential in our ecosystem. Out of many factors, air is essential to life and the quality of air can highly effect our health. Every year, millions of Americans suffer from adverse health impacts liked to air pollution, an d tens of thousands have their lives cut short. This project focuses on air pollution with the retrieved air data. 

*So what is Air data?*

The United States Environmental Protection Agency (EPA) provides access to air quality data (primarily from Air quality system (AQS) database) collected at outdoor monitors across the United Sates, Puerto Rico, and the U.S Virgin Islands. The data can be used to view, create visuals and graphical displays, investigate monitor locations, and so on. It is accessible to the public and can be downloaded by hourly, daily, and annual concentration data, AQI data, and speciated particle pollution data.

*How does the four criteria gases air pollution impact us?*

#### Ozone
-Coughing and pain when taking a deep breath

-Lung and throat irritation

-Wheezing and trouble breathing during exercise or outdoor activities

-Can effect everyone, but specifically people with asthma or other lung diseases, older adults, babies and children
(https://www.cdc.gov/air/ozone.html)

#### Carbon monoxide
-Breathing air with a high concentration of CO reduces the amount of oxygen that can be transported in the blood stream to critical organs like the heart and brain.

- Can cause dizziness, confusion, unconsciousness and death.

- Very high levels of CO are not likely to occur outdoors. However, when CO levels are elevated outdoors, they can be of particular concern for people with some types of heart disease.

(https://www.epa.gov/co-pollution/basic-information-about-carbon-monoxide-co-outdoor-air-pollution)

#### Nitrogen dioxide  

- Increased inflammation of the airways 

- Worsened cough and wheezing

- Reduced lung function

- Increased asthma attacks

- Greater likelihood of emergency department and hospital admissions.

(https://www.lung.org/clean-air/outdoors/what-makes-air-unhealthy/nitrogen-dioxide)

#### Sulfur dioxide

- Irritates the skin and mucous membranes of the eyes, nose, throat, and lungs. 

- Can cause inflammation and irritation of the respiratory system.

- Pain when taking a deep breath, coughing, throat irritation, and breathing difficulties. High concentrations of SO2 can affect lung function, worsen asthma attacks, and worsen existing heart disease in sensitive groups. 
-
(https://www.nps.gov/subjects/air/humanhealth-sulfur.htm)

*Literature Review*

•European ozone measurements examined through a cluster analysis (CA) of 4 years of 3-hourly ozone data from 1492 European surface monitoring stations in the Airbase database

•Propose the use of air quality index and the development of advanced data processing, analysis, and visualization techniques based on the AI-based k-clustering method, based in China.

•Novel hybrid learning method, carried out to forecast urban air quality index (AQI). Wavelet packet decomposition (WPD) was firstly performed to decompose the original AQI data into lower-frequency subseries. (China)

1.Cluster analysis of European surface ozone observations for evaluation of MACC reanalysis data
Authors: Olga Lyapina, Martin G. Schultz, and Andreas Hens

2. K-Clustering Methods for Investigating Social-Environmental and Natural-Environmental Features Based on Air Quality Index
Authors: Victor Chang; Pin Ni; Yuming L

3. A clustering-based ensemble approach with improved pigeon-inspired optimization and extreme learning machine for air quality prediction
Author: Feng Jiang a,, Jiaqi He a, Tianhai Tian b



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
The images on the bottom shows the 29 columns within the dataset, along with the description for each. 
Out of the 29 elements, the ones that will be used in our project are Features:
- State code
- County code
- Observation Count
- Observation Percent
- Arithmetic mean
- AQI
- 1st Max Value

![1](https://user-images.githubusercontent.com/70929605/125210368-6b090d00-e26d-11eb-83c8-15453d13af0f.jpg)
![2](https://user-images.githubusercontent.com/70929605/125210372-70665780-e26d-11eb-8ecc-3a4c31835acb.jpg)

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

## EDA
The chart below shows the distribution for each criteria gas. Although it is not detailed, it shows a quick overview of how the AQI is distributed. 
![Screen Shot 2021-07-28 at 11 01 32 PM](https://user-images.githubusercontent.com/70929605/127575550-4068fb6d-63a6-4902-ab93-de7c4b919072.png)

### Box Plot for Each State's AQI Per Criteria Gas
Each plot visually shows all the state's distribution of numerical data and skewness through displaying the data quartiles (or percentiles) and averages, along with the outliers. Because there are many states, it is hard to see the state's name; two additional charts were generated to show the 10 states with the highest, and the lowest AQI. Also, some noticeable factors are stated. 

#### 1. Ozone 
![ozone_state_aqi](https://user-images.githubusercontent.com/70929605/127575627-34025308-37c4-47cb-8667-d36a4ab565b0.png)

Arizona has high AQI with highest and the most outliers. This shows that the AQI in the state seems to be very inconsistent.
On the other hand, Alaska and Hawaii has a low AQI with no outlier. The AQI for ozone seems to be consistent.

Highest : Arizona, Colorado, New Mexico, Utah 
Lowest: Hawaii, Washington, Oregon, Alaska

#### 2. Carbon Monoxide 
![co_state_aqi](https://user-images.githubusercontent.com/70929605/127575694-5015ac79-158a-4e3e-ae1a-4605cbc56f0a.png)

Oregon is the only state that has very high AQI with the outliers.

Highest: Georgia, Arizona, Alaska, California
Lowest: South Carolina, Wyoming, Mississippi, Nebraska 

#### 3. Nitrogen Dioxide 
![no2_state_aqi](https://user-images.githubusercontent.com/70929605/127575739-6f2fa05a-6b7b-4a55-bd36-4b83866314c6.png)

Nevada has a high AQI with no outliers. This indicates that the AQI is very consistent.
Highest: Nevada, Idaho, Arizona, Georgia
Lowest: Montana, Wyoming, New Hampshire, North Dakota 

#### 4. Sulfur Dioxide
![so2_state_aqi](https://user-images.githubusercontent.com/70929605/127575784-9ed13273-53db-4576-8be1-859989d0f46a.png)

Overall, most of the states have many outliers which suggests that sulfur dioxide AQI is inconsistent.
Alaska has highest AQI with some low outliers.
Hawaii, Texas, and Virginia has low AQI but very high outlier.
Highest: Alaska, West Virginia, Alabama, Illinois
Lowest: Wyoming, New Mexico, New Jersey, New Hampshire

## Implementation (Model)
#### K-Means Clustering 

In order to find the best analyzation for our dataset, the K-Means clustering model was ran to see how many clusters, and where the clusters were. The four data sets (four types of criteria gases) were ran separately, with the elements that had an AQI over the limit of a good-moderate pollution rate (In other words, the clusters showed the states/regions that had air pollution for each type of gas). 
In order to find the number of clusters, the elbow method was used and generated. Below shows the generated model for the elbow method.

![Screen Shot 2021-07-29 at 6 57 21 PM](https://user-images.githubusercontent.com/70929605/127575877-1e40fef5-0cea-43fd-8166-cf31240083af.png)
![Screen Shot 2021-07-29 at 6 57 25 PM](https://user-images.githubusercontent.com/70929605/127575882-99a466a6-19bf-4ac6-978e-8cbd62629d81.png)
![Screen Shot 2021-07-29 at 6 57 30 PM](https://user-images.githubusercontent.com/70929605/127575892-a9ce1d8a-fd49-45c1-8eb7-3dc6002bfe1e.png)
![Screen Shot 2021-07-29 at 6 57 34 PM](https://user-images.githubusercontent.com/70929605/127575908-19f98b25-9870-4bbb-aea5-720701bdffca.png)

Number of K: Ozone- 3, Carbon Monoxide- 4, Nitrogen Dioxide- 3, Sulfur Dioxide- 4

Blow shows the result of clustering for the four types of criteria gases

Setting boundary of the dataset to at least ’moderately polluted’

Ozone:  AQI > 100

Carbon Monoxide:  AQI > 10

Nitrogen Dioxide: AQI > 80

Sulfur Dioxide:  AGI > 80


#### Ozone


![image](https://user-images.githubusercontent.com/70929605/129127582-efa2c6ad-160b-4423-9bf8-4afa2f749bf5.png)

#### Sulfur Dioxide 

![image](https://user-images.githubusercontent.com/70929605/129127606-77623452-f658-4818-a4f2-2936b68f59b8.png)

#### Carbon Monoxide

![image](https://user-images.githubusercontent.com/70929605/129127620-336e7611-90be-4b39-a9f6-e70831a0402c.png)


#### Nitrogen Dioxide 

![image](https://user-images.githubusercontent.com/70929605/129127641-79323093-9683-4ae7-88a7-b57175f76655.png)


## Findings / Suggestions

- Sulfur Dioxide’s air pollution is the most severe out of the 4 gases

- Carbon Monoxide’s air pollution is the least sever out of the 4 gases 

- Central States have the best AQI overall

- The clusters seem to be generated by regions (West, Central, East)

1. Ozone

- Limiting driving 

- Maintain vehicles/tools well

- Try to use tools without motors.

2. Carbon Monoxide

- Regular inspections, maintenance

- Proper storage in house 

3. Nitrogen Dioxide

- Manage and Reduce Emissions

- Conserve energy, Less driving

 
4. Sulfur Dioxide

- Set regulations by State

## Moving Forward..

- Find more details for the clusters. 

- Find a detailed dataset that has the indicators for pollution.

- Generate clusters using time (See when the pollution is more severe).

- Think of other analysis/ machine learning that I can do with the dataset. 

