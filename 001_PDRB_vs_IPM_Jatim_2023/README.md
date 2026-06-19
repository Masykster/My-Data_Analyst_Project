# 💰📊 GRDP vs. HDI — East Java Province 2023

This project measures, maps, and analyzes the relationship between **Gross Regional Domestic Product (GRDP) at Current Prices** (a proxy for regional economic capacity) and the **Human Development Index (HDI)** (a measure of human welfare and development) across 38 regencies and cities in East Java Province in the year 2023.

The primary objective of this analysis is to identify economic anomalies (regions with high economic output but lagging social welfare indices) and map priority areas that require targeted, dual-aspect policy interventions.

---

## 📂 Repository Structure & Dataset

* **Analysis Notebook**: [PDRB_vs_IPM_Jatim_2023.ipynb](file:///d:/Projek/Data_Analyst/001_PDRB_vs_IPM_Jatim_2023/PDRB_vs_IPM_Jatim_2023.ipynb)
* **Data Directory**: [data/](file:///d:/Projek/Data_Analyst/001_PDRB_vs_IPM_Jatim_2023/data/)
  * `Produk Domestik Regional Bruto Atas Dasar Harga Berlaku... 2023.csv`: GRDP data per regency/city in East Java for 2023 (in billions of IDR). Source: BPS (Central Bureau of Statistics) East Java.
  * `Indeks Pembangunan Manusia Menurut Kabupaten_Kota... 2023.csv`: HDI data per regency/city in East Java for 2023. Source: BPS East Java.

---

## 🛠️ Analysis Steps & Methodology

1. **Data Ingestion & Merging**: Ingests GRDP and HDI CSV files into a unified pandas DataFrame.
2. **Data Cleaning**: Standardizes regional administrative names, removes irrelevant columns, and formats data types.
3. **Geospatial Coordinate Joining**: Merges statistical data with GPS coordinates (Latitude & Longitude) for each regency/city in East Java.
4. **Correlation Analysis**: Calculates the Pearson correlation coefficient to measure the strength and direction of the linear relationship between GRDP and HDI.
5. **Quadrant Analysis (Klassen Typology)**:
   * **Quadrant 1 (Q1)**: High GRDP & High HDI (Developed and Prosperous).
   * **Quadrant 2 (Q2)**: Low GRDP & High HDI (Economic output under-optimized, but high social welfare).
   * **Quadrant 3 (Q3)**: Low GRDP & Low HDI (Priority development regions requiring attention).
   * **Quadrant 4 (Q4)**: High GRDP & Low HDI (High economic output but lagging social welfare — Anomaly).
6. **Geospatial Mapping (Folium)**: Generates web-based interactive Leaflet maps:
   * Spatial HeatMaps representing the density of GRDP and HDI.
   * Dual-variable CircleMarker maps (circle radius represents GRDP size; circle colour indicates HDI score).
   * Automated fly-to camera animations to step through each region.
   * Interactive popups housing HTML micro-bar charts to display local socioeconomic profiles dynamically on hover.

---

## 📈 Key Findings & Strategic Insights

* **Moderate Positive Correlation ($r = 0.499$)**: There is a positive linear relationship between regional economic size (GRDP) and human development. Higher economic output generally correlates with higher HDI, but this relationship is not absolute.
* **Significant Socioeconomic Disparities**:
  * The highest GRDP per capita is recorded in **Kediri City (IDR 541.1 million / billion IDR)**, while the lowest is in **Pamekasan Regency (IDR 23.8 million)**, showing a stark **22.7x** economic disparity ratio.
  * The highest HDI is recorded in **Malang City (84.00)**, while the lowest is in **Sampang Regency (66.19)**, representing a gap of **17.81 points**.
* **Economic Anomalies (Q4 - High GRDP & Low HDI)**:
  * Regions: **Malang Regency, Banyuwangi, Pasuruan, Bojonegoro, Tuban, Sumenep**.
  * **Insight**: These regions generate substantial economic output (often driven by large-scale manufacturing or extractive oil, gas, and mining industries), yet their human development index remains relatively low. Local policy should shift focus from raw economic output toward income redistribution, local education investment, and healthcare access to ensure economic gains translate directly into local human capital.
* **Priority Regions (Q3 - Low GRDP & Low HDI)**:
  * Regions: **Pacitan, Ponorogo, Trenggalek, Blitar, Lumajang, Jember, Bondowoso, Situbondo, Probolinggo, Ngawi, Bangkalan, Sampang, Pamekasan**.
  * **Insight**: These regions require a dual-action policy approach: economic stimulation through investment incentives alongside structural social safety nets (education subsidies, healthcare assistance, and clean water infrastructure).

---

## 🎨 Interactive Visualizations Generated

The interactive maps exported from this notebook include:
1. **Distribution & Correlation Map (Seaborn)**: A scatter plot featuring linear regression fit and quadrant-based colour coding.
2. **GRDP HeatMap**: A geospatial density map representing the concentration of economic activity.
3. **HDI HeatMap**: A geospatial density map representing the concentration of human development.
4. **Dual-Variable Circle Map**: A composite representation displaying economic scale (circle size) and social welfare (traffic-light scale from red to green).
5. **Interactive Dashboard Map**: A map containing custom popup markers embedded with HTML micro-bar charts representing the regional economic breakdown.

---

## 🚀 How to Run

Open the Jupyter Notebook [PDRB_vs_IPM_Jatim_2023.ipynb](file:///d:/Projek/Data_Analyst/001_PDRB_vs_IPM_Jatim_2023/PDRB_vs_IPM_Jatim_2023.ipynb) using your local Python environment (e.g., Anaconda, JupyterLab) or Google Colab. Ensure the dependencies `folium`, `seaborn`, `pandas`, and `branca` are installed.
