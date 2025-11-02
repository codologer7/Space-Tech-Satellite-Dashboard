# 🛰️ Space Technology & Satellite Operations Dashboard

## 📘 Project Overview

The **Space Technology & Satellite Operations Dashboard** is a data analytics project built entirely in **Power BI**.
It provides a unified, visual understanding of global satellite operations, launch statistics, telemetry health, urban impact, and mission outcomes.

This dashboard enables users to explore **how satellites perform, which countries lead in space activity, and how space technology influences our planet** — through intuitive, interactive visuals.

---

## 🎯 Objectives

1. Track satellite telemetry metrics (battery, temperature, orbit stability).
2. Analyze mission success and failure trends.
3. Compare launches and missions by country.
4. Monitor climate and urban growth indicators via satellite data.
5. Assess mission cost vs. performance outcomes.
6. Predict satellite lifespan using historical data patterns (via built-in forecast visuals).
7. Compare public vs. private space missions.
8. Track and visualize real-time space debris records.

---

## 🧩 Project Architecture

### 🔹 1. Datasets Used

| Dataset                             | Source                        | Key Use                                                   |
| ----------------------------------- | ----------------------------- | --------------------------------------------------------- |
| **UCS Satellite Database**          | Union of Concerned Scientists | Satellite details – country, orbit, launch date, lifespan |
| **CSIS Launch Dataset**             | CSIS Aerospace Security       | Launch counts & success by country                        |
| **OPS-SAT Telemetry (ESA)**         | ESA Open Data                 | Telemetry health readings & anomaly examples              |
| **Urban Growth (Nighttime Lights)** | NASA EarthData                | City expansion via satellite imaging                      |
| **Cost of Launches to LEO**         | Our World In Data             | Mission cost and performance comparison                   |

All datasets were combined and cleaned entirely using **Power Query**.

---

### 🔹 2. Data Preparation (No Code)

In **Power Query**, we performed:

* Renamed columns for clarity (e.g., “Launch_Date” → “Year of Launch”)
* Removed null and duplicate records
* Created calculated columns via “Add Column” → “Custom Column”:

  * **Satellite Age (Years)** = Current Year – Launch Year
  * **Mission Outcome Category** = Success / Failure / Ongoing
  * **Cost in Millions USD** = `[Cost]/1,000,000`
* Merged datasets by satellite ID or country for combined analysis
* Loaded processed tables into the Power BI data model

This entire workflow required **zero scripting**.

---

## 📊 Dashboard Design

### 🧭 Dashboard Sections

1. **Mission Overview Page** – KPI cards for total satellites, active satellites, and success rate.
2. **Launch Insights Page** – Bar and map visuals comparing launches by country and organization type.
3. **Telemetry & Health Page** – Line charts showing battery %, temperature, and anomaly flags.
4. **Cost vs Outcome Page** – Scatter and column charts linking mission cost with success rates.
5. **Climate & Urban Growth Page** – Integration of nightlight-based urban expansion and emission data.
6. **Future Forecast Page** – Uses built-in **Power BI Forecasting** (no DAX) to predict lifespan & upcoming launches.

---

## 📈 Key Insights

* India, USA, and China lead in new satellite launches (2020 – 2024).
* Private sector missions are growing rapidly, with ~30 % lower cost per launch.
* Satellites older than 6 years show higher anomaly rates and reduced battery performance.
* Urban expansion (from nightlight data) correlates 90 % with regional emission increase.
* Global debris concentration is highest in **Low Earth Orbit (LEO)** — requiring closer monitoring.

---

## ⚙️ Tools Used

| Category         | Tool                       |
| ---------------- | -------------------------- |
| Data Preparation | **Power Query**            |
| Visualization    | **Power BI Desktop**       |
| Data Cleaning    | Power BI built-in features |
| Documentation    | Excel / Word / PowerPoint  |
| Presentation     | Power BI Report + Slides   |

---

## 🧪 Workflow Steps

1. **Collect Data:** Download all CSV/Excel datasets into `/data/raw/`.
2. **Import into Power BI:** Use *Get Data → Excel/CSV → Load*.
3. **Transform Data:**

   * Clean, rename, and merge in **Power Query**.
   * Add calculated columns using *“Add Column → Custom Column”*.
4. **Create Relationships:**

   * Link `Satellite_ID` between tables.
   * Connect `Country` or `Year` for comparative visuals.
5. **Build Visuals:**

   * Use cards, bar charts, line charts, maps, and gauges.
   * Add slicers for *Country*, *Year*, *Agency Type*, *Orbit Type*.
6. **Design Pages & Navigation:**

   * Add a title banner and navigation buttons between pages.
   * Apply consistent theme colors (dark space theme).
7. **Forecasts & Trends:**

   * Select a chart → *Analytics Pane → Forecast* → Set periods.
8. **Finalize & Publish:**

   * Save final `.pbix` as `SpaceTech_Dashboard_Final.pbix`.
   * Export presentation slides showing key visuals and KPIs.

---

## 📂 Folder Structure

```
Space-Tech-Satellite-Dashboard/
│
├── Datasets/
│   ├── Raw Datsets/
│   └── Processed Datasets/
│
├── Power Bi/
│   └── SpaceTech_Dashboard_Final.pbix
│
├── Docs/
│   └── Methodology_Report.docx
│
└── PPTs/
    └── Final_Presentation.pptx
```

---

## 💡 Team Roles

| Role                   | Responsibility                                 |
| ---------------------- | ---------------------------------------------- |
| **Data Lead**          | Collect and clean datasets in Power Query      |
| **Visualization Lead** | Design visuals, maps, and layout               |
| **Research Lead**      | Gather domain context (space & climate impact) |
| **Documentation Lead** | Prepare final report and presentation          |

---

## 📜 References

* Union of Concerned Scientists – Satellite Database
* CSIS Aerospace Launch Data
* ESA OPS-SAT Telemetry Dataset
* Our World in Data – Cost of Space Launches
* NASA EarthData – Urban Growth and Climate Change

---

## 🧠 Learning Outcomes

* Built a **complete Power BI analytical dashboard** with **no coding or DAX**.
* Understood **space mission analytics** through real-world data.
* Learned **data integration, visualization, and storytelling** using Power BI only.

---

## 🏆 Project Summary

> “Our project proves that you don’t need coding to uncover powerful insights from space data.
> With teamwork, clear objectives, and Power BI’s analytical power, we turned complex satellite information into an interactive, story-driven dashboard that helps visualize the future of space technology.”
