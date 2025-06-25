# ✈️ Sky Analytics: Navigating the Complexities of Airline and Airport Operations

## 📋 Project Description

SkyNet Analysis Inc., a leader in aviation analytics, seeks to uncover actionable insights from large-scale flight operations data. With the aviation industry's increasing complexity, delays, cancellations, and resource utilization have become critical factors for efficiency and customer satisfaction.

This project leverages **Microsoft Excel** to analyze three integrated datasets—`flights.csv`, `airlines.csv`, and `airports.csv`. Using advanced Excel features such as pivot tables, slicers, and calculated fields, a dynamic and interactive dashboard was developed to explore airline and airport performance, delay trends, and cancellation patterns.

---

## 💾 Project Files Description

- `flights.csv`: Contains ~70,000 records of flight-level operational data.
- `airlines.csv`: Lookup table for airline codes and full names.
- `airports.csv`: Metadata for airports including geolocation.
- **Excel Workbook**: Includes cleaned and merged data, pivot analyses, and the interactive dashboard.
- **Visualizations**: Embedded charts, KPIs, and slicer-enabled analysis in Excel.

---

## 🧾 Dataset Contents

### 🔹 flights.csv
Includes flight-specific data such as schedule, delays, cancellations, distance, and aircraft ID.

### 🔹 airlines.csv
Maps airline IATA codes to their full airline names.

### 🔹 airports.csv
Provides detailed metadata about airports, including names, cities, states, countries, and their latitude/longitude.

---

## 📊 Key Variables

### ✈️ flights.csv

| Column                          | Description                                      |
|---------------------------------|--------------------------------------------------|
| YEAR, MONTH, DAY, DAY_OF_WEEK   | Date-related info                                |
| AIRLINE                         | Carrier code                                     |
| FLIGHT_NUMBER                   | Unique flight identifier                         |
| TAIL_NUMBER                     | Aircraft identifier (used for fleet utilization) |
| ORIGIN_AIRPORT / DESTINATION_AIRPORT | Source and destination airports            |
| SCHEDULED_DEPARTURE / DEPARTURE_TIME | Planned vs. actual departure times        |
| DEPARTURE_DELAY / ARRIVAL_DELAY | Delay durations (in minutes)                     |
| WHEELS_OFF / WHEELS_ON          | Actual takeoff and landing times                 |
| AIR_TIME                        | Duration in air                                  |
| TAXI_OUT / TAXI_IN              | Time on taxiway before/after flight              |
| SCHEDULED_TIME / ELAPSED_TIME   | Planned vs. actual total flight time             |
| DISTANCE                        | Distance flown (in miles)                        |
| SCHEDULED_ARRIVAL / ARRIVAL_TIME| Scheduled vs. actual arrival times               |
| CANCELLED, DIVERTED             | Binary flags for disruptions                     |
| CANCELLATION_REASON             | Encoded reason for cancellations                 |
| Delay Columns (e.g., AIRLINE_DELAY) | Delay types in minutes                     |

### 🛩 airlines.csv

| Column     | Description               |
|------------|---------------------------|
| IATA_CODE  | Unique airline code       |
| AIRLINE    | Full name of the airline  |

### 🏙 airports.csv

| Column     | Description                        |
|------------|------------------------------------|
| IATA_CODE  | Unique airport code                |
| AIRPORT    | Full name of the airport           |
| CITY       | City where the airport is located  |
| STATE      | U.S. State                         |
| COUNTRY    | Country of the airport             |
| LATITUDE / LONGITUDE | Geographical coordinates |

---

## ❓ Problem Statement

Flight disruptions—especially delays and cancellations—can significantly affect airline efficiency and customer satisfaction. This project addresses the following:

- Which airlines and airports operate most efficiently?
- What are the main causes of delays?
- Are disruptions influenced by time of day, day of week, or season?
- How can airlines improve fleet utilization and schedule reliability?

By exploring these questions, the project provides stakeholders with the tools to make data-driven decisions for optimizing air travel operations.

---

## 🛠 Technologies Used

- **Tool**: Microsoft Excel

### 🧰 Techniques Applied

- Data Cleaning & Imputation
- Conditional Logic (`IF`, `VLOOKUP`, `TEXT`, `DATE`)
- Pivot Tables and Charts
- Slicers and Timeline Controls
- Time-Based Aggregation
- KPI Tiles and Conditional Formatting
- Geolocation Mapping using coordinates

---

## 🔍 Data Cleaning Summary

| Action         | Column(s)                                        | Reason                                                                 |
|----------------|--------------------------------------------------|------------------------------------------------------------------------|
| Dropped Rows   | `TAIL_NUMBER` (0.65% missing)                    | Insignificant proportion; safe to remove                               |
| No Change      | Time-related columns (3.1–3.4% missing)          | Missing only for cancelled or diverted flights                         |
| Imputed Value  | `ELAPSED_TIME`                                   | Logically calculated as `ARRIVAL_TIME - DEPARTURE_TIME`               |
| Skipped Columns| Delay reason columns (79–96% missing)            | Sparse, encoded, and non-essential for core metrics                    |

---

## 🔍 Steps Involved

### 1. **Data Preparation**
- Removed unnecessary and sparse records
- Imputed missing values where applicable
- Merged airline and airport metadata

### 2. **Exploratory Data Analysis (EDA)**
- Identified delay trends across time slots, days, and airlines
- Evaluated fleet utilization and airport traffic

### 3. **Dashboard Design**
- Developed an Excel dashboard using pivot tables, slicers, and charts
- Enabled user-friendly filtering and insights with KPIs and interactivity

---

## 📌 Key Insights from Dashboard

- **Most Active Airports**: ATL, ORD, and DFW lead in total flight volume.
- **Top Performing Airlines**: AS, US, and HA show high on-time performance.
- **Delay Analysis**:
  - **Late Aircraft** is the top cause: avg **22.30 min**
  - **Airline-related** delays average **18.28 min**
  - **Weather-related** delays follow at **13.71 min**
- **Time Trends**:
  - **Evenings** show highest delays
  - **Mornings** have more flight activity and cancellations
  - **Mondays (Day 1)** and **Sundays (Day 7)** are most prone to delays
- **Fleet Utilization**: TAIL_NUMBER analysis reveals aircraft workload distribution.
- **Cancellations**: Account for only **2.56%** of all flights, concentrated in specific months.

---

## 🧭 Slicer Functionality in Dashboard

Interactive slicers allow users to dynamically explore performance metrics:

- **By Airline**: Compare KPIs across different carriers
- **By Month**: Identify seasonal delay and traffic patterns
- **By Time Slot**: Detect peak operational hours and bottlenecks
- **By Cancellation Status**: Filter only disrupted flights for root cause analysis

---

## 🎯 Conclusion 

The Excel dashboard enables a powerful, interactive exploration of aviation operations:

- Provides real-time answers to questions about which airlines or airports perform best  
- Helps identify bottlenecks caused by operational inefficiencies or environmental factors  
- Equips decision-makers with data-driven insights for scheduling, resource planning, and service enhancements  

By leveraging Excel’s visualization and analytical capabilities, the project transforms raw aviation data into strategic intelligence for **smarter skies**—empowering stakeholders to make informed, efficient, and customer-centric decisions.

