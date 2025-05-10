

# HVAC Sensor Data Analysis

**By M. SUNDARRAJAN**
**2nd Year, Department of Mechanical Engineering**
**ARM College of Engineering & Technology**
**Course: Data Analysis in Mechanical Engineering**

---

## Introduction

This project is part of my coursework in *Data Analysis in Mechanical Engineering*. The goal of this project is to analyze data collected from HVAC (Heating, Ventilation, and Air Conditioning) sensors and to understand how different environmental and operational factors interact with each other. Through this analysis, I aim to observe how things like temperature, humidity, air flow, and CO₂ levels relate to occupancy and energy usage. The overall intention is to gain insights that could help in making HVAC systems more energy efficient and comfortable.

---

## Objective of the Project

The main purpose of this project is:

* To identify patterns and trends in how the HVAC system operates throughout the day.
* To find what causes high energy consumption.
* To help improve decision-making in HVAC maintenance and automation by using real sensor data.

---

## About the Dataset

The dataset includes several readings that were taken over a period of time. Each row represents one time-stamped data point with the following features:

| Feature Name              | Description                                  |
| ------------------------- | -------------------------------------------- |
| Date\_Logged              | The date and time when the data was recorded |
| Temperature (C)           | The indoor temperature in Celsius            |
| Humidity (%)              | The indoor relative humidity                 |
| Air\_Flow (CFM)           | Air flow in cubic feet per minute            |
| CO2\_Level (ppm)          | CO₂ level in parts per million               |
| Occupancy                 | Number of people in the area at that time    |
| Energy\_Consumption (kWh) | HVAC energy consumption in kilowatt-hours    |

---

## Steps Taken During Data Preparation

1. **Importing and Inspecting Data**
   The dataset was first loaded using the Pandas library. I looked at the top rows to understand how the data is structured.

2. **Datetime Formatting**
   The `Date_Logged` column was converted into a datetime format. This allowed me to perform time-based analysis, like checking hourly or daily trends.

3. **Handling Missing Data**
   Some columns, such as `CO2_Level (ppm)` and `Air_Flow (CFM)`, had missing values. I replaced them with the average value of each column to keep the data balanced.

4. **Creating New Features**
   To make analysis easier, I added two new columns:

   * `Hour`: The hour of the day from the timestamp.
   * `DayOfWeek`: The day of the week (0 for Monday to 6 for Sunday).

---

## Exploratory Data Analysis (EDA)

To understand the dataset better, I used various plots and graphs.

### Time-Based Patterns

* Energy usage follows a daily pattern and is usually higher during office hours.
* CO₂ levels and temperature also change depending on how many people are present.

### Correlation Between Features

* Energy consumption increases as air flow and temperature increase.
* CO₂ levels have a strong relationship with how many people are in the room.

### Distribution and Outliers

* Histograms and boxplots were used to study how each feature is distributed.
* Some data points, especially in energy and airflow, seemed unusually high or low and might be outliers.

---

## Main Observations

* **CO₂ Levels Rise with More People**: This is expected, but clearly visible in the data.
* **More People = More Air Flow**: The system adjusts airflow based on occupancy.
* **Energy Peaks at Specific Times**: Energy use is higher between 9 AM and 6 PM, which matches typical work hours.
* **Temperature and Humidity Are Quite Stable**: The HVAC system does a good job maintaining comfort.

---

## Future Improvements

* Use methods like the IQR technique to find and remove outliers.
* Try building a simple machine learning model to predict energy use or detect unusual patterns in HVAC performance.

---

## Tools and Technologies

* **Python** with **Pandas** and **NumPy** for data cleaning and manipulation.
* **Matplotlib** and **Plotly** for creating charts and graphs.
* **Jupyter Notebook** for writing code, notes, and visualizations in one place.
