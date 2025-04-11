# a360
## The following preparation work has been complete:

1. AWS configuration, as described in https://docs.snowflake.com/en/user-guide/data-load-s3-config-storage-integration
    a. S3 bucket creation
    b. IAM policy, role and trust creation
2. Snowflake integration configuration:
    CREATE OR REPLACE STORAGE INTEGRATION S3INTEGRATION
      TYPE = EXTERNAL_STAGE
      STORAGE_PROVIDER = 'S3'
      STORAGE_AWS_ROLE_ARN = 'xxxx'
      ENABLED = TRUE
      STORAGE_ALLOWED_LOCATIONS = ('s3://demos-sf-2025/demodata/*')
   
## Data sources
https://www.kaggle.com/c/nyc-taxi-trip-duration \
https://www.kaggle.com/mathijs/weather-data-in-new-york-city-2016, additional data used for cleaning

## Repository structure
1_A360_EL - Jupyter Notebook for loading \
2_A360_T - Jupyter Notebook for cleaning \  
           &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Reused the code shared by: https://github.com/justin-hj-kim/NYCtaxi_data_science/blob/master/notebooks/Taxi_Data_ETL.ipynb \
3_A360_Analysis - Jupyter Notebook with simple analysis / visualizations


## Analysis / charts

### Analysis
1. There are two service providers, with Vendor ID 1 and 2. #2 owns 65% of the market. Augmenting the data with the vendor information may be helpful
2. Passenger count and trip duration are key measures that seem to correlate with revenue and utilization, importand business KPIs
3. Most of the trips occured in Manhattan area (see the heat map below, credit to https://github.com/justin-hj-kim/NYCtaxi_data_science/blob/master/README.md). Further analysis of the geospacial data may be complete to explore vehicle utilization opportunities
4. Taxi utilization distribution for time of the day, week or specific public events may be analyzed (the data set is limited to 7 months)
5. The vendor may analyze data from competetive intelligence perspective to explore better practices patterns of the competition 

![image](https://github.com/user-attachments/assets/50da79a2-d8d5-4604-8cd2-fd0b7f49b2b5)


### Charts

![image](https://github.com/user-attachments/assets/2e1ad47b-3d5c-4bbf-acbb-c148f3915ecd)

![image](https://github.com/user-attachments/assets/a1b8348e-d07d-4af1-9011-63767f0ca4c3)

![image](https://github.com/user-attachments/assets/0aa84c0b-b2df-4d45-8d0c-0c74253b026a)

![image](https://github.com/user-attachments/assets/1243625c-519b-47b2-a1cf-240a5fd29f29)




