# Taxi Trip Duration Prediction with Inferential Statistics 📊🚖

## Overview

This project focuses on practicing inferential statistics using Python to predict taxi trip durations based on a given dataset. The dataset includes information such as pickup and dropoff times, locations, and trip durations. The goal is to create a set of Python functions that perform specific tasks and generate predictions with meaningful statistical insights.

## Data Set

The dataset provided contains information about taxi trips, including pickup_datetime, dropoff_datetime, and trip duration.
https://data.cityofnewyork.us/Transportation/2019-High-Volume-FHV-Trip-Records/4p5c-cbgn/data

## Functions

1. **trip_duration(data_frame)**
   - Description: This function takes a data frame as input and computes the trip duration by calculating the difference between pickup_datetime and dropoff_datetime. The new column with trip durations is added to the data frame, and the updated data frame is returned.
   
2. **add_features_time(data_frame)**
   - Description: This function takes a data frame as input and adds two new columns to it - the hour of the day and the day of the week. The information is extracted from the pickup_datetime field. The modified data frame is then returned.

3. **calculate_confidence_interval(data_frame)**
   - Description: This function computes a new data frame called predictions. The index of this data frame is a combination of PULocationID, DOLocationID, day of the week, and hour. It includes two columns: 
     - Mean Trip Duration: Calculated as the mean trip duration for all instances with the same PULocationID/DOLocationID/day of the week/hour.
     - Margin of Error: Computed using a 95% confidence interval.
   The resulting predictions data frame is returned.

4. **generate_predictions(data_frame)**
   - Description: This function reads the data file specified by the data_frame and calls the three aforementioned functions in sequence to generate the final predictions data frame. The entire process is documented and follows the specified requirements using scipy for t or z scores.
