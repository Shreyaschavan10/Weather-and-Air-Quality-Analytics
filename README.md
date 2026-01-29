
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

## 🧩 Data Modeling – Star Schema

The project follows **dimensional modeling best practices** to ensure performance and scalability.

### ⭐ Fact Table
**FactWeather**
- Temperature
- Humidity
- Wind Speed
- Pressure
- Visibility
- Precipitation
- AQI & pollutant measures
- Forecast indicators

### 📐 Dimension Tables
- **DimDate** – Date, Day, Week, Month
- **DimCity** – City Name, Location
- **DimWeatherCondition** – Overcast, Sunny, etc.
- **DimPollutant** – PM2.5, PM10, CO, NO₂, SO₂, O₃

---

## 📊 Dashboard Preview

![Dashboard Preview](./dashboard.png)

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
