### 🌦️ Weather Data Analysis Project
Python | Pandas | NumPy | Matplotlib

This project performs complete analysis on an hourly weather dataset (Toronto, 2012) enhanced with a synthetic rainfall column.
The original dataset includes:

Date & Time
Temperature
Dew Point
Relative Humidity
Wind Speed
Visibility
Pressure
Weather Condition

Since the dataset does not contain rainfall, a custom rainfall feature (rainfall_mm) is generated using realistic probability-based values to support rainfall statistics and visualization.

---

### 📁 Dataset
Input File Used
Weather Data.csv

Columns in the Original Dataset
Column	Description
Date/Time	Timestamp (hourly)
Temp_C	Temperature in °C
Dew Point Temp_C	Dew point temperature
Rel Hum_%	Relative humidity
Wind Speed_km/h	Wind speed
Visibility_km	Visibility in km
Press_kPa	Air pressure in kPa
Weather	Weather conditions
Added Column
Column	Description
rainfall_mm	Synthetic rainfall amount (0–20 mm)

Rainfall generation logic:

70% → 0 mm (no rain)
20% → light rain (0–5 mm)
10% → heavy rain (5–20 mm)

This allows meaningful rainfall analysis for the project.

This Data set is import from Kaggle.com

---

### 🚀 Full Project Workflow

This project is divided into six main tasks.

✅ Task 1: Data Acquisition & Loading

Read the CSV file using Pandas.

Perform dataset inspection using:

head()

info()

describe()

Understand column names and data types.

✅ Task 2: Data Cleaning & Processing

Convert the Date/Time column to datetime.

Handle missing values using:

.dropna() or

.fillna() with statistical replacements.

Rename key columns for consistency:

Date/Time → date

Temp_C → temperature

Rel Hum_% → humidity

Add the synthetic rainfall column.

Final cleaned dataset contains:

date

temperature

humidity

rainfall_mm

✅ Task 3: Statistical Analysis (NumPy)

Using NumPy, compute:

Daily Temperature Stats

Mean

Minimum

Maximum

Standard deviation

Monthly and Yearly Statistics

Using newly created:

month

year

Statistics computed:

Monthly mean/min/max/std of temperature

Monthly total rainfall

Yearly summary (if dataset spans multiple years)

✅ Task 4: Visualization with Matplotlib

This project generates four major plots, saved as PNG images.

📈 1. Daily Temperature Trend

Line chart showing temperature variation over time.

🌧️ 2. Monthly Rainfall Totals

Bar chart visualizing total rainfall per month.

🔵 3. Humidity vs Temperature

Scatter plot showing the relationship between humidity and temperature.

📊 4. Combined Temperature + Rainfall Plot

Temperature line + rainfall bars combined in one figure.

All are saved as:

daily_temperature.png
monthly_rainfall.png
humidity_vs_temperature.png
combined_plot.png

✅ Task 5: Grouping & Aggregation

Using groupby():

Monthly Aggregates

Average temperature

Average humidity

Total rainfall

Seasonal Analysis

Seasons defined:

Winter (Dec–Feb)

Spring (Mar–May)

Summer (Jun–Aug)

Autumn (Sep–Nov)

Seasonal statistics include:

Mean temperature

Mean rainfall

✅ Task 6: Export & Storytelling
✔ Export Cleaned Data
cleaned_weather_data.csv

✔ Generate Markdown Report

Automatically generated file:

weather_report.md

✔ Save All Plots

PNG files saved in project directory.

The report includes:

Key findings

Temperature summary

Rainfall insights

Full list of generated outputs

---

### 📂 Project Structure

Weather-Analysis-Project/
│
├── your_weather_data.csv
├── weather_analysis.py
├── cleaned_weather_data.csv
├── weather_report.md
│
├── daily_temperature.png
├── monthly_rainfall.png
├── humidity_vs_temperature.png
└── combined_plot.png

🖥 How to Run the Project
1. Install dependencies
pip install pandas numpy matplotlib

2. Place the CSV and script in the same folder
3. Run the script
python weather_analysis.py

4. Check the generated output files

---


### 🎉 Conclusion

This project demonstrates a full data science workflow:

Data loading

Cleaning

Feature engineering (synthetic rainfall)

Statistical analysis

Visualization

Aggregation

Automated report generation

Perfect for academic submissions, portfolio building, or learning data analysis concepts

### Author 

Sameer Mishra