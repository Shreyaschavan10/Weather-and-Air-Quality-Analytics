<p align="center">
  <img src="https://github.com/Shreyaschavan10/Weather-and-Air-Quality-Analytics/blob/main/images/DashBoard.png" width="1000"/>
</p>

👉 **[Click here to interact with dashboard](https://app.powerbi.com/view?r=eyJrIjoiYjJhMTM0OTItNmVmNC00Y2JkLWEzZGQtMTZmN2I4MzViMGVhIiwidCI6ImRjYzhhODY2LWM1ZTMtNDE0Yi04Yzk0LWE4MjA5MTY3Nzc1NCJ9)**

# 🌦️ Weather & Air Quality Analytics Dashboard (Power BI)

An end-to-end **data analytics and business intelligence project** that collects weather and air quality data using APIs, models it using a **Star Schema**, and delivers insights through an **automated Power BI dashboard** with daily refresh in Power BI Service.

---

## 📌 Project Overview

This project demonstrates how raw weather and environmental data can be transformed into a **production-ready analytics solution**.

The workflow includes:
- Collecting **7 days historical** and **7 days forecast** weather data using Weather APIs
- Designing a **Star Schema data model**
- Building an interactive Power BI dashboard
- Publishing dataset and report to **Power BI Service**
- Configuring **automatic daily data refresh**

---

## 🔄 Data Pipeline Architecture

**End-to-End Flow:**

1. Weather & Air Quality data fetched using Weather APIs
2. Secure API authentication using API keys
3. Data cleaning and transformation
4. Star Schema data modeling (Fact & Dimension tables)
5. Dataset published to Power BI Service
6. Dashboard created using the semantic model
7. Scheduled refresh configured (once per day)

---

## 🧱 Data Model & ETL Design

### Data Ingestion (Staging Layer)
Weather data is collected for multiple cities using a Weather API.  
Each city’s API response is initially stored in **city-specific staging tables** such as:

- Weather_Pune  
- Weather_MUM  
- Weather_Nagpur  
- Weather_Nasik  
- Weather_Kolhapur
- Weather_SN (SambhajiNagar)

These tables represent the **raw API ingestion layer** and are retained for traceability, validation, and debugging purposes.

---

### ETL & Data Transformation
The city-level staging tables are **referenced in Power Query** and transformed to create consolidated reporting tables.  
Key ETL steps include:
- Selecting relevant weather and air-quality fields  
- Standardizing column names and data types  
- Combining city data into unified structures  
- Creating separate fact tables based on granularity  

The transformed output tables are:
- `Current` – real-time weather and air quality data  
- `Forecast_Day` – daily forecast and astronomical data  
- `Forecast_Hours` – hourly forecast and precipitation probability  

Only these consolidated tables are used for reporting and visualization.

---

### Star Schema Design (Reporting Layer)

The final reporting model follows a **Star Schema** design.

#### Dimension Table
**Locations**
- Central dimension table containing city/location information
- Used to filter and slice all weather data

#### Fact Tables
- **Current**
  - AQI, PM2.5, PM10, gaseous pollutants
  - Cloud cover and weather conditions

- **Forecast_Day**
  - Daily weather forecast
  - Sunrise, sunset, moon phase, temperature metrics

- **Forecast_Hours**
  - Hourly weather forecast
  - Hourly AQI and chance of rain

All fact tables are connected to the **Locations** dimension using one-to-many relationships, enabling efficient filtering and optimized query performance.

---

### Measures Layer
A dedicated `_measures` table is used to store reusable DAX measures such as:
- AQI Status
- AQI Health Suggestions
- Chance of Rain

This approach ensures a clean semantic layer and avoids duplication of business logic across visuals.

---

### Design Rationale
- Separating staging and reporting layers improves maintainability
- Star schema optimizes Power BI performance and simplifies analysis
- Centralized measures ensure consistent calculations across the dashboard
- The model is scalable and can easily support additional cities

---

## 🚀 Dashboard Features

- 🌡️ Current weather overview
- 📈 7-day historical and forecast temperature trends
- 🌅 Sunrise & sunset timings
- 🌫️ Air Quality Index (AQI) monitoring
- 🌬️ Wind speed, humidity, pressure & visibility
- 🌧️ Rain probability forecast
- 🔄 Automatic daily data refresh
- 🎨 Dark-themed, user-friendly analytical UI

---

## 📊 Metrics Included

### Weather Metrics
- Temperature (°C)
- Weather Condition
- Wind Speed (kph)
- Humidity (%)
- Atmospheric Pressure
- Visibility
- UV Index
- Precipitation

### Time-Based Metrics
- Date hierarchy
- Sunrise time
- Sunset time

### Air Quality Metrics
- Air Quality Index (AQI)
- PM2.5
- PM10
- Carbon Monoxide (CO)
- Nitrogen Dioxide (NO₂)
- Sulfur Dioxide (SO₂)
- Ozone (O₃)

### Forecast Metrics
- 7-day historical trend
- 7-day forecast trend
- Rain probability (%)

---

## 🎯 Outcomes & Insights

This dashboard enables users to:
- Analyze **weather trends** over time
- Monitor **air quality and pollution levels**
- Assess **health-related AQI impact**
- Support **outdoor planning and decision-making**
- Access **automated insights without manual updates**

---

## 🛠️ Tech Stack

- **Data Source:** Weather & Air Quality APIs
- **Data Modeling:** Star Schema
- **Visualization Tool:** Power BI
- **Deployment:** Power BI Service
- **Automation:** Scheduled dataset refresh (Daily)

---

## ▶️ Power BI Service Deployment

- Dataset and semantic model published to Power BI Service
- Dashboard connected to centralized dataset
- Scheduled refresh configured to run **once per day**
- Ensures up-to-date insights automatically

---

## 🔮 Future Enhancements

- Multi-city comparison
- Historical seasonality analysis
- Health recommendations based on AQI
- Alerting for extreme weather conditions
- Real-time data streaming integration

---

## 📚 Skills Demonstrated

- API data extraction
- Data cleaning & transformation
- Dimensional data modeling
- Power BI dashboard development
- DAX calculations
- Power BI Service deployment
- Data refresh automation

---

⭐ If you found this project useful, feel free to star the repository!
