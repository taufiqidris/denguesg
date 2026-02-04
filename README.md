# Singapore Dengue Outbreak Analysis & Decision Support Tool

## 📌 Project Overview
Transitioning 5 years of Public Health experience into Data Science, I developed this end-to-end analytical pipeline to identify spatial-temporal trends in Singapore's Dengue transmission. This project bridges epidemiological domain knowledge with advanced Python modeling to optimize public health resource allocation.

## 🛠️ Tech Stack
* **Language:** Python 3.13
* **Libraries:** Pandas, GeoPandas (Spatial Analysis), Folium (Interactive Mapping), Seaborn/Matplotlib (Statistical Visualization)
* **Data Sources:** NEA Dengue Cluster KML/GeoJSON, MOH Weekly Infectious Disease Records (Data.gov.sg)

## 📊 Analytical Deep Dive

### 1. Spatial Correlation: Construction Site Impact
Using GeoPandas to parse KML metadata, I isolated clusters linked to construction activities. 
* **Methodology:** Applied **Logarithmic Scaling** to visualize distributions skewed by extreme outliers (clusters with >300 cases).
* **Insight:** Construction-linked clusters are significantly more likely to become "mega-clusters" compared to standard residential areas.


### 2. Temporal Intensity: DHF vs. Standard Dengue
I developed a dual-visualization approach to compare disease severity.
* **Standard Dengue:** Visualized using line overlays with a "Typical Peak Season" highlight (Weeks 20-35).
* **DHF:** Visualized via **Heatmaps** to identify high-intensity anomalies that standard line charts fail to capture due to low frequency.


### 3. Interactive GIS Mapping
I transformed static GeoJSON polygons into an interactive Leaflet map.
* **Feature:** Integrated tooltips that extract locality-specific data (e.g., specific breeding sites like "flower pot trays" or "bins").
* **Outcome:** A scannable dashboard that allows a health officer to identify high-risk "hot zones" at a glance.


## 🚀 Technical Challenges Overcome
* **Data Type Cleaning:** Resolved `ValueError` issues by converting categorical case sizes into numerical integers, enabling statistical quartile (Q1, Median, Q3) analysis.
* **Coordinate Reference Systems (CRS):** Managed the transformation of geospatial data into WGS84 format for web-map compatibility.
* **Visual Communication:** Optimized high-density temporal charts by adjusting label orientations and color palettes for maximum scannability.

## ⚖️ Data Ethics & Privacy
All data utilized is sourced from public Open Data portals. In accordance with Singapore's **PDPA** and **Public Service Data Governance** standards, all personal identifiers were excluded to ensure the highest level of patient confidentiality.