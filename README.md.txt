# HVAC Sensor Data Analysis

*Submitted by Tamilselvan .J*
**2nd Year, Mechanical Engineering**
**Course: Data Analysis in Mechanical Engineering**
**ARM College of Engineering & Technology**

---

## Introduction

This project focuses on analyzing HVAC (Heating, Ventilation, and Air Conditioning) sensor data. The goal is to study how different environmental and system parameters behave over time, and how they influence energy usage and indoor comfort levels. This kind of analysis can help improve building management and save energy in the long run.

---

## Why This Project?

As part of understanding real-world mechanical systems, this project was chosen to:

* Observe how HVAC systems operate under different indoor conditions.
* Find out when and why more energy is being used.
* Support smarter building management through data insights.

It also helps in developing skills in handling real datasets, cleaning them, analyzing trends, and using visual tools to present results.

---

## What the Data Contains

The dataset includes sensor readings recorded at different times. Each row in the data represents one timestamp with multiple measurements related to indoor climate and system operation.

| Feature                   | What It Represents                            |
| ------------------------- | --------------------------------------------- |
| Date\_Logged              | When the reading was recorded                 |
| Temperature (C)           | Indoor air temperature                        |
| Humidity (%)              | Indoor air humidity percentage                |
| Air\_Flow (CFM)           | Volume of air moved, in cubic feet per minute |
| CO2\_Level (ppm)          | CO2 concentration in the room                 |
| Occupancy                 | Number of people present                      |
| Energy\_Consumption (kWh) | How much energy the HVAC system used          |

---

## Steps Taken to Clean and Prepare the Data

1. **Importing and Looking at the Data**
   Used Python libraries like Pandas to load the dataset and check for any issues.

2. **Fixing Date Formats**
   The time column (`Date_Logged`) was converted into a datetime format so it could be analyzed more easily.

3. **Handling Missing Data**
   Some values were missing in the `CO2_Level` and `Air_Flow` columns. These were filled using the average (mean) of each column.

4. **Creating Extra Features**
   New columns were added from the timestamp to help with the analysis:

   * `Hour`: The hour of the day (e.g., 14 for 2 PM).
   * `DayOfWeek`: Day of the week (0 = Monday, 6 = Sunday).

---

## What the Data Tells Us

Here are some things observed during the analysis:

### Time-Based Patterns

* Energy use goes up during working hours, especially between 9 AM and 6 PM.
* CO2 levels increase when more people are in the room, which makes sense.

### Relationships Between Features

* Energy usage seems to rise when temperature or air flow increases.
* CO2 levels are clearly affected by how many people are in the space.

### Data Distributions

* Some values, especially for airflow and energy, are uneven and show outliers.
* Visual tools like histograms and boxplots helped spot these.

---

## Key Learnings and Observations

* **More People = More CO2**: The air gets stuffy faster when there are more people in a room.
* **Air Flow Adjusts Automatically**: The HVAC system appears to respond to higher occupancy.
* **Energy Usage Matches Office Hours**: Most energy is used during the day, especially on weekdays.
* **Temperature is Mostly Stable**: HVAC controls seem to be doing their job well in keeping the room comfortable.

---

## What Can Be Done Next

* Use techniques like IQR (Interquartile Range) to remove abnormal values from the dataset.
* Build a simple prediction model to forecast energy consumption.
* Try detecting unusual behavior in the HVAC system for better maintenance.

---

## Tools and Technologies Used

* **Python** – Main programming language
* **Pandas, NumPy** – For handling and processing data
* **Plotly, Matplotlib** – For creating charts and graphs
* **Jupyter Notebook** – To write code, display results, and document the process
