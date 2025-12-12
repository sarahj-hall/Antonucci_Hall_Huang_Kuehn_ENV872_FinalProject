# Antonucci_Hall_Huang_Kuehn_ENV872_FinalProject
ENV 872 Course Project for A. Antonucci, S. Hall, C. Huang, and I. Kuehn

# <Repository Title>

## Summary

This repository contains code and data for the investigators' Duke Nicholas School of the Environment ENVIRON872 Environmental Data Exploration Final Course Project in the Fall of 2025. The data used for analysis was event-correlated power outage data from the Pacific Northwest National Laboratory (PNNL). Temporal trends in the frequency, seasonality, and severity of power outages were analyzed for California, Florida, Pennsylvania, and Texas from 2015 to 2023.

## Investigators

Addisen Antonucci, Sarah Hall, Carina Huang, and Isabelle Kuehn

## Keywords

power outages, trend, time series analysis, power-system, black-out, reliability

## Database Information

The dataset was downloaded from the Open Energy Data Initiative (OEDI), and the outage data set version 2 was accessed 11/15/2025. This dataset is located in the Data/Raw folder. Processed data was wrangled in RStudio and written into Data/Processed folder in the repository.  

Data citation: 
She, B., Adetola, V., & Yun, J. (2024). Event-correlated Outage Dataset in America. Open Energy Data Initiative (OEDI). Pacific Northwest National Laboratory. https://data.openei.org/submissions/6458


## Folder structure, file formats, and naming conventions 
Folders in this repository include: Code, Output, Data/Raw, and Data/Processed. 

- '~/Code' folder the .Rmd files used to complete the data wrangling, exploration, and analysis for this report.
  - Naming according to state and content of analyis
- '~Data/Raw' folder contains the original data sets (all csv files)
  - Naming of files is original to the dataset source
- '~Data/Processed' contains the wrangled data. All data was downloaded and processed into csv format. 
  - Naming according to state and correpsonds to respective dataset
- '~/' contains the REAMME file and final report .rmd and .pdf files 

## Metadata

<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 

note to self: might not need to include all this if we don't use it?, also check class types 
In the Raw data folder, there are four different types of files for the years 2014 to 2023 (replace year in title with proper year):

1. eagle_outages_year_group.csv

Column Name    | Description                                                   | Class         | Units
-------------: | :----------------------------------------------------------- | ------------- | -------------
state         |State where outage occurred                                   | factor  | NA
year          | Year when outage occurred                                    | integer  | NA
month  | Month when outage occurred (0 is yearly summary)| integer | NA
outage_count  | Total number of outages | integer | NA
max_outage_duration  | Maximum duration of any single outage in the period | number | hours
customer_weighted_hours  | Total customer-weighted hours, calculated by multiplying the number of affected customers by the outage duration | number | NA

2. eagle_outages_year_merged.csv

Column Name    | Description                                                   | Class         | Units
-------------: | :----------------------------------------------------------- | ------------- | -------------
fips          |FIPS code identifying the county where outage occured          | number  | NA
state         |State where outage occurred                                   | factor  | NA
county          | County where outage occur                                  | factor  | NA
start_time  | Time when outage occurred | ?? | NA
duration  | Duration of the outage | number | hours
min_customers  | Minimum number of affected customers during the outage | number | NA
max_customers  | Maximum number of affected customers during the outage | number | NA
mean_customers | Mean number of affected customers during the outage | number | NA

3. eaglei_outages_with_events_2014_8_hours_lag.csv

Column Name    | Description                                                   | Class         | Units
-------------: | :----------------------------------------------------------- | ------------- | -------------
event_id       | Unique identified for associated event          | factor | NA
state_event         |State of outage event                                   | factor  | NA
Datetime Event Began | Date and time of the start of the outage event | ???  | NA
Datetime Restoration | Date and time of the end of the outage event | ???  | NA
Event Type  | The type of disturbance (e.g. hurricane) causing the outage | factor | NA
fips          |FIPS code identifying the county where outage occured          | number  | NA
state         |State where outage occurred                                   | factor  | NA
county          | County where outage occur                                  | factor  | NA
start_time  | Time when outage occurred | ?? | NA
duration  | Duration of the outage | number | hours
min_customers  | Minimum number of affected customers during the outage | number | NA
max_customers  | Maximum number of affected customers during the outage | number | NA
mean_customers | Mean number of affected customers during the outage | number | NA

4. eaglei_outages_with_events_2014_24_hours_lag.csv

Column Name    | Description                                                   | Class         | Units
-------------: | :----------------------------------------------------------- | ------------- | -------------
event_id       | Unique identified for associated event          | factor | NA
state_event         |State of outage event                                   | factor  | NA
Datetime Event Began | Date and time of the start of the outage event | ???  | NA
Datetime Restoration | Date and time of the end of the outage event | ???  | NA
Event Type  | The type of disturbance (e.g. hurricane) causing the outage | factor | NA
fips          |FIPS code identifying the county where outage occured          | number  | NA
state         |State where outage occurred                                   | factor  | NA
county          | County where outage occur                                  | factor  | NA
start_time  | Time when outage occurred | ?? | NA
duration  | Duration of the outage | number | hours
min_customers  | Minimum number of affected customers during the outage | number | NA
max_customers  | Maximum number of affected customers during the outage | number | NA
mean_customers | Mean number of affected customers during the outage | number | NA


In the Processed data folder: 
1. outage_group_all_years.csv

Column Name    | Description                                                   | Class         | Units
-------------: | :----------------------------------------------------------- | ------------- | -------------
state         |State where outage occurred                                   | character  | NA
year          | Year when outage occurred                                    | integer  | NA
month  | Month when outage occurred | integer | NA
outage_count  | Total number of outages | integer | NA
max_outage_duration  | Maximum duration of any single outage in the period | number | hours
customer_weighted_hours  | Total customer-weighted hours, calculated by multiplying the number of affected customers by the outage duration | number | NA
Date | Date when outage occured | date | NA


## Scripts and code
All found in the Code folder:
Wrangling code:
1. Title.rmd - code used for wrangling ___ outage data
2. 

Exploration code:
Analysis code:
Project Code: Includes all code used to wrangle, visualized and analyze our data.
<list any software scripts/code contained in the repository and a description of their purpose.>
