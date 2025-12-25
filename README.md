# ✈️ Flight Delay Analysis Dashboard

## 📌 Overview

This project presents an **interactive data analytics dashboard** for analyzing **flight delays within the United States**. The dashboard provides a comprehensive view of flight performance, delay patterns, and contributing factors using **real-world aviation data**.

The project supports both **Light Mode** and **Dark / Night Mode**, enhancing usability and accessibility for different user preferences.

---

## 📊 Data Source

* **Dataset:** US Domestic Flights Delay Data
* **Platform:** Kaggle
* **Scope:** Domestic flights within the United States
* **Data Includes:**

  * Flight status (Delayed / On-Time / Early)
  * Departure & arrival delays
  * Airlines
  * Airports (Origin)
  * Delay reasons (Weather, Carrier, NAS, Security, Late Aircraft)
  * Distance & time-based attributes

---

## 🎯 Project Objectives

* Analyze flight delay patterns across airlines and airports
* Identify major causes of delays
* Compare on-time, delayed, and early flights
* Study the relationship between departure delay and arrival delay
* Provide decision-support insights using interactive visuals

---

## 🛠 Tools & Technologies

* **Data Visualization:** Power BI
* **Data Modeling:** Star Schema (Fact & Dimension Tables)
* **Data Source:** CSV files from Kaggle
* **Design:**

  * Light Mode Dashboard
  * Dark / Night Mode Dashboard
* **Charts & Visuals Used:**

  * KPI Cards
  * Line Charts
  * Bar Charts
  * Stacked Bar Charts
  * Scatter Plots
  * Pie Charts
  * Interactive Slicers

---

## 🧩 Data Model (Star Schema)

The project uses a **Star Schema data model** to ensure optimal performance, clean relationships, and scalable analytics within Power BI.

### ⭐ Fact Table – Fact_Flights

The central table that stores **flight-level transactional data** and all measurable metrics:

* DepDelay (Departure Delay)
* ArrDelay (Arrival Delay)
* AirTime
* ActualElapsedTime
* Cancelled Flag
* Diverted Flag
* Flight Status (Delayed / On-Time / Early)
* Delay Components:

  * CarrierDelay
  * WeatherDelay
  * NASDelay
  * SecurityDelay
  * LateAircraftDelay

**Foreign Keys:**

* Date_Key
* Carrier_Key
* Route_Key
* Cancellation_Key

This table acts as the **single source of truth** for all KPIs and calculations.

---

### ⭐ Dimension Tables

#### 📅 Date_Dim

Provides full time intelligence support:

* Date
* Day
* Month
* Month Name
* Quarter
* Year

Used for time-based analysis, trends, and seasonality.

---

#### ✈️ Airport_Dim

Contains route and distance attributes:

* Origin Airport
* Destination Airport
* Route
* Distance

Used for origin-based delay analysis and distance insights.

---

#### 🏢 Carrier_Dim

Contains airline reference data:

* Airline Name
* Unique Carrier Code

Used for airline performance and delay comparison.

---

#### ❌ Cancellation_Dim

Lookup table for cancellation details:

* Cancellation Code
* Cancellation Reason

Used for cancellation analysis and operational insights.

---

### 🔗 Relationships

* One-to-Many relationships from **Dimension Tables → Fact_Flights**
* Single-directional filtering to avoid ambiguity
* Optimized for accurate aggregations and performance

---

### 📐 DAX Measures Layer

A dedicated **DAX Measures table** is used to centralize business logic:

* Total Flights
* Delayed Flights
* On-Time Flights
* Early Flights
* Average Delay (Minutes)

This approach improves model readability, reusability, and maintenance.

---

### ✅ Why Star Schema?

* Faster query performance
* Cleaner relationships
* Simpler and more readable DAX
* Industry-standard BI modeling approach

---

---

## 📈 Dashboard Features

### 🔹 Key Performance Indicators (KPIs)

* Total Flights
* Total Delayed Flights
* Total On-Time Flights
* Total Early Flights
* Average Delay Time (minutes)

---

### 🔹 Flight Status Analysis Over Time

* Monthly trend of:

  * Delayed Flights
  * On-Time Flights
  * Early Flights
* Helps identify seasonal patterns and peak delay periods

---

### 🔹 Airline Delay Composition

* Breakdown of delay reasons per airline:

  * Late Aircraft Delay
  * NAS Delay
  * Weather Delay
  * Security Delay
  * Carrier Delay
* Enables comparison of operational efficiency between airlines

---

### 🔹 Average Delay per Airline

* Ranking airlines by average delay minutes
* Highlights best and worst performers

---

### 🔹 Departure vs Arrival Delay

* Scatter plot showing correlation between departure delay and arrival delay
* Demonstrates how departure issues impact arrival performance

---

### 🔹 Flight Status Distribution

* Pie chart showing percentage of:

  * Delayed flights
  * On-time flights
  * Early flights

---

### 🔹 Top 10 Origin Airports by Delayed Flights

* Identifies airports with the highest number of delayed flights
* Useful for operational and infrastructure analysis

---

### 🔹 Delay by Distance Analysis

* Scatter plot analyzing average delay minutes against flight distance
* Reveals whether longer flights experience more delays

---

## 🎛 Interactivity

* **Time Slicer:** Filter data by time
* **Airline Slicer:** Filter by specific airline
* Dynamic visuals update instantly based on selections

---

## 🌙 Light Mode & Dark Mode

* Two complete dashboard themes implemented:

  * **Light Mode:** Clean and professional layout
  * **Dark / Night Mode:** Reduced eye strain, modern appearance

Both modes maintain identical insights and functionality.

---

## 📌 Key Insights

* Departure delay has a strong positive correlation with arrival delay
* Certain airlines consistently show higher average delays
* Weather and late aircraft are among the top delay causes
* Major hub airports experience higher delay volumes
* Distance alone does not significantly increase average delay

---

## 🚀 Future Enhancements

* Add predictive delay modeling
* Include weather severity data
* Drill-through pages for individual airlines and airports
* Deployment using Power BI Service or embedded analytics

---

## 👤 Author

* **Project Type:** Data Analysis & Visualization
* **Focus Area:** Aviation Analytics

---

⭐ If you find this project useful, feel free to star the repository!
