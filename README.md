

# HVAC Sensor Data Analysis

**By S. KARTHIK**
**2nd Year, Mechanical Engineering**
**ARM College of Engineering & Technology**
**Course: Data Analysis in Mechanical Engineering**

---

## Project Overview

This project is part of my coursework in Data Analysis in Mechanical Engineering. The main goal is to work with real-world data from an HVAC (Heating, Ventilation, and Air Conditioning) system and understand how different factors affect its performance. By studying this sensor data, I aim to gain basic insights into how buildings consume energy and how that can be optimized.

This analysis focuses on key factors like:

* Indoor temperature and humidity
* Air flow rates and CO₂ concentration
* Occupancy levels and energy usage

Studying these can help improve energy efficiency and maintain a comfortable indoor environment.

---

## Description of the Dataset

The dataset contains a series of time-stamped readings collected from HVAC sensors. Each entry records several features:

| Feature Name              | Description                               |
| ------------------------- | ----------------------------------------- |
| Date\_Logged              | Date and time when the data was recorded  |
| Temperature (C)           | Temperature measured indoors              |
| Humidity (%)              | Relative humidity percentage              |
| Air\_Flow (CFM)           | Air flow in cubic feet per minute         |
| CO2\_Level (ppm)          | Carbon dioxide levels in the room         |
| Occupancy                 | Number of people present                  |
| Energy\_Consumption (kWh) | HVAC system energy used in kilowatt-hours |

---

## Data Preprocessing Steps

Before analyzing the data, some cleaning and preparation steps were followed:

1. **Data Loading**
   The dataset was imported using the Pandas library. I checked for basic structure and types of data.

2. **Datetime Formatting**
   The Date\_Logged column was changed into a proper datetime format to help with time-based analysis.

3. **Handling Missing Data**
   Missing values in features like CO2\_Level and Air\_Flow were filled using the average values.

4. **Creating New Features**
   From the timestamp, I created two new columns:

   * *Hour*: To see patterns throughout the day
   * *DayOfWeek*: To analyze weekday and weekend behavior

---

## Exploratory Data Analysis (EDA)

Using basic graphs and charts, I explored how the features behave over time and how they relate to one another.

* **Daily Patterns**
  Energy usage was higher during the day, especially working hours. CO₂ levels and temperature also showed some variation with occupancy.

* **Relationships Between Features**

  * Energy\_Consumption had moderate correlation with temperature and air flow.
  * CO₂ levels were strongly related to how many people were in the room.

* **Distributions and Outliers**
  I used histograms and boxplots to look at the spread of data. Some unusual values were noticed, especially in energy and air flow readings.

---

## Main Takeaways

Here are some important findings from the analysis:

* **CO₂ levels rise with more people** – This is expected, as more people breathe out more CO₂.
* **Air Flow increases with occupancy** – Suggests the system adjusts itself when more people are present.
* **Energy is used mostly during working hours** – Around 9 AM to 6 PM on weekdays.
* **Temperature and humidity are mostly stable** – The HVAC seems to be doing a good job at maintaining indoor comfort.

---

## Future Improvements

For future work, I plan to:

* Use outlier detection methods like IQR to remove unusual sensor readings.
* Try basic prediction models to forecast energy use or detect unusual HVAC behavior.

---

## Tools and Technologies Used

* **Python**: For all the data handling (mainly using Pandas and NumPy)
* **Matplotlib & Plotly**: For creating visualizations
* **Jupyter Notebook**: Used for coding and documenting my process
