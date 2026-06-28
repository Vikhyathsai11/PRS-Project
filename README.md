# 🚗 German Autobahn Traffic Analysis & Bottleneck Detection

> **Data Analytics Project**
> Analysis of German Autobahn Traffic Count Data (BASt Dataset) using Python, Pandas, NumPy, Matplotlib, and Statistical Analysis.

---

# 📌 Project Overview

This project analyzes long-term German Autobahn traffic count data collected by **BASt (Federal Highway Research Institute)**. The objective is to study traffic evolution over time on selected highways (**A6, A9, and A93**) and develop a rule-based algorithm to detect potential traffic bottlenecks.

The project follows a complete data analytics workflow, including:

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Traffic Evolution Analysis
* Correlation & Statistical Analysis
* Rule-Based Bottleneck Detection
* Final Reporting & Visualization

---

# 🎯 Project Objectives

## Question 1

Analyze Autobahn traffic count data over time for common roads:

* A6
* A9
* A93

Investigate:

* How traffic evolved between 2003–2023
* Growth trends
* Heavy vehicle movement
* Statistical correlations
* Road-specific characteristics

---

## Question 2

Develop an algorithm capable of detecting and locating potential traffic bottlenecks caused by:

* High traffic density
* Heavy truck movement
* Sudden traffic drops
* Construction activities
* Traffic anomalies

---

# 📊 Dataset

Source: **BASt – German Federal Highway Research Institute**

The dataset contains annual traffic statistics from highway counting stations across Germany.

Important columns used in this project:

| Column       | Description                  |
| ------------ | ---------------------------- |
| Jahr         | Year                         |
| Str_Nr       | Autobahn Number              |
| DZ_Name      | Counting Station             |
| Betriebs_km  | Kilometer Position           |
| DTV_Kfz_W_Q  | Average Weekday Traffic      |
| DTV_SV_W_Q   | Heavy Vehicle Traffic        |
| pSV_W_Q      | Percentage of Heavy Vehicles |
| Anz_Fs_Q     | Number of Lanes              |
| Koor_WGS84_N | Latitude                     |
| Koor_WGS84_E | Longitude                    |
| Anmerkungen  | Remarks / Construction Notes |

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* SciPy
* Jupyter Notebook

---

# 📁 Project Structure

```
German_Autobahn_Traffic_Analysis/

│
├── data/
│   ├── raw_traffic.csv
│   └── cleaned_traffic.csv
│
├── notebooks/
│   ├── 01_Data_Cleaning.ipynb
│   ├── 02_Exploratory_Data_Analysis.ipynb
│   ├── 03_Traffic_Evolution.ipynb
│   ├── 04_Correlation_Analysis.ipynb
│   ├── 05_Bottleneck_Detection.ipynb
│   └── 06_Final_Report.ipynb
│
├── plots/
│
├── results/
│
├── README.md
│
└── requirements.txt
```

---

# 📚 Project Workflow

```
Raw BASt Dataset
        │
        ▼
Phase 1
Data Cleaning
        │
        ▼
Phase 2
Exploratory Data Analysis
        │
        ▼
Phase 3
Traffic Evolution Analysis
        │
        ▼
Phase 4
Correlation Analysis
        │
        ▼
Phase 5
Rule-Based Bottleneck Detection
        │
        ▼
Phase 6
Final Report & Dashboard
```

---

# 📌 Phase 1 – Data Cleaning

Objectives:

* Load dataset
* Handle missing values
* Remove duplicates
* Convert German number formats
* Correct data types
* Prepare clean dataset for analysis

Output:

```
cleaned_traffic.csv
```

---

# 📌 Phase 2 – Exploratory Data Analysis

Performed:

* Dataset overview
* Missing value analysis
* Road distribution
* Station distribution
* Traffic statistics
* Data quality assessment

Purpose:

Understand the dataset before performing analysis.

---

# 📌 Phase 3 – Traffic Evolution Analysis

Focused Roads:

* A6
* A9
* A93

Analysis included:

* Yearly average traffic
* Growth calculation
* Traffic evolution trends
* Heavy vehicle trends
* Station stability
* Summary statistics

Output:

* Traffic evolution plots
* Growth analysis
* Road comparison

---

# 📌 Phase 4 – Correlation Analysis

Investigated relationships between:

* Total Traffic
* Heavy Vehicle Traffic
* Truck Percentage
* Year

Methods:

* Pearson Correlation
* Correlation Matrix
* Scatter Plots
* Regression Trend Analysis
* Statistical Summary

Purpose:

Understand relationships among traffic variables.

---

# 📌 Phase 5 – Rule-Based Bottleneck Detection

Instead of using a black-box machine learning model, this project implements an explainable rule-based algorithm.

The algorithm evaluates each station using:

### 1. Traffic Density

```
Traffic Density =
Traffic Volume / Number of Lanes
```

Higher density indicates increased congestion risk.

---

### 2. Traffic Drop

Traffic is compared with the previous station.

Large drops may indicate:

* Construction
* Lane closures
* Diversions
* Congestion

---

### 3. Heavy Vehicle Percentage

Higher truck percentages increase congestion probability.

---

### 4. Construction Remarks

Stations containing remarks such as:

* Netzmodernisierung
* Baustelle

receive additional risk scores.

---

### 5. Traffic Outlier Detection

Statistical outliers are identified using Z-Score analysis.

---

### Risk Scoring

Each indicator contributes to a final bottleneck score.

| Risk Score | Classification |
| ---------- | -------------- |
| 0          | Normal         |
| 1          | Low            |
| 2          | Medium         |
| 3–4        | High           |
| ≥5         | Critical       |

---

# 📌 Phase 6 – Final Report

Final notebook provides:

* Dataset summary
* Road comparison
* Traffic evolution
* Growth analysis
* Correlation summary
* Bottleneck summary
* Exported tables
* Exported figures
* Project conclusions
* Limitations
* Future work

---

# 📈 Key Findings

* Traffic evolution from **2003–2023** was analyzed.
* Average weekday traffic trends were compared for **A6**, **A9**, and **A93**.
* Heavy vehicle traffic showed a strong relationship with total traffic.
* Rule-based bottleneck detection successfully identified high-risk locations.
* Construction remarks and statistical anomalies improved bottleneck identification.

---

# ⚙ Bottleneck Detection Algorithm

```
Traffic Dataset
       │
       ▼
Sort Stations by Kilometer
       │
       ▼
Traffic Density
       │
       ▼
Traffic Drop
       │
       ▼
Truck Percentage
       │
       ▼
Construction Detection
       │
       ▼
Traffic Outlier Detection
       │
       ▼
Risk Score
       │
       ▼
Bottleneck Classification
```

---

# 📊 Generated Outputs

Results:

```
road_summary.csv

growth.csv

dashboard.csv

final_summary.csv

top10_stations.csv
```

Plots:

```
traffic_evolution.png

growth.png

correlation.png

risk_map.png

traffic_density.png
```

---

# 🚀 Future Improvements

Potential enhancements include:

* Real-time traffic sensor integration
* Weather data integration
* Accident database integration
* Construction schedule integration
* Interactive dashboard using Streamlit
* Machine learning traffic forecasting
* GIS-based visualization

---

# ⚠ Limitations

* Dataset contains annual traffic summaries.
* Hourly congestion cannot be detected.
* Accident information is unavailable.
* Weather conditions are not included.
* Bottlenecks identified are potential locations rather than confirmed traffic jams.

---

# 💡 Skills Demonstrated

* Data Cleaning
* Exploratory Data Analysis
* Data Visualization
* Statistical Analysis
* Correlation Analysis
* Rule-Based Algorithm Design
* Traffic Analytics
* Geospatial Analysis
* Python Programming
* Report Generation

---

# 👨‍💻 Author

**Vikhyath Gupta**

Master's Student – AI for Industrial Applications

Germany

---

# ⭐ Project Summary

This project demonstrates a complete end-to-end traffic analytics workflow using real-world German highway traffic data. It combines data preprocessing, statistical analysis, visualization, and an explainable bottleneck detection algorithm to provide insights into long-term traffic evolution and identify potential congestion hotspots on selected Autobahns.
