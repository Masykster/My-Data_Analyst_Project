# 📊 Data Analyst Portfolio — East Java & Indonesia Investment Studies

Welcome to my **Data Analyst Portfolio** repository! This repository contains a curated collection of data analysis projects, interactive visualizations, geospatial mapping, and statistical hypothesis testing using Python. The primary analytical focus includes regional economic development (GRDP), human welfare index (HDI), and the dynamics of Foreign Direct Investment (FDI) at the national level.

---

## 📁 Repository Structure

The repository is structured into three primary projects:

1. **[001_PDRB_vs_IPM_Jatim_2023](file:///d:/Projek/Data_Analyst/001_PDRB_vs_IPM_Jatim_2023/)**
   * A study on the relationship between Gross Regional Domestic Product (GRDP) and the Human Development Index (HDI) across regencies and cities in East Java in 2023.
   * Features economic and social welfare quadrant analysis (Klassen Typology) along with web-based interactive geospatial mapping (Folium).
2. **[002_Analisis Realisasi FDI Indonesia 2019-2023](file:///d:/Projek/Data_Analyst/002_Analisis%20Realisasi%20FDI%20Indonesia%202019-2023/)**
   * An analysis of the impact of the COVID-19 pandemic on Foreign Direct Investment (FDI) realisations in Indonesia by economic sector.
   * Employs inferential statistical hypothesis testing (independent t-test, One-way ANOVA, Shapiro-Wilk normality test, and Pearson correlation) to verify economic resilience and structural recovery (*investment super-cycle*).
3. **[003_Analisis Indeks Pembangunan Manusia (IPM) Jawa Timur 2021-2025](file:///d:/Projek/Data_Analyst/003_Analisis%20Indeks%20Pembangunan%20Manusia%20(IPM)%20Jawa%20Timur%202021-2025/)**
   * Advanced interactive geospatial mapping (Choropleth maps and Timestamped timeline animation) to monitor and analyze the spatial-temporal progression of HDI in East Java over a 5-year period.

---

## 🛠️ Technology Stack & Libraries

These projects are developed in **Python** utilising the following scientific computing and data visualization libraries:

* **Data Manipulation & Processing**:
  * [pandas](https://pandas.pydata.org/) — For tabular data (.csv) preprocessing, cleaning, joining, and aggregation.
  * [numpy](https://numpy.org/) — For numerical computations and array operations.
* **Statistical Analysis**:
  * [scipy.stats](https://scipy.org/) — For inferential statistics (independent t-test, One-way ANOVA, Shapiro-Wilk normality test, and Pearson correlation).
* **Data Visualization (Static)**:
  * [matplotlib](https://matplotlib.org/) — For foundational plots, multi-variable charts, radar charts, and custom layout styling.
  * [seaborn](https://seaborn.pydata.org/) — For distribution profiling (boxplots, violin plots), quarterly heatmaps, and aesthetic trend charts.
* **Geospatial & Interactive Visualization**:
  * [folium](https://python-visualization.github.io/folium/) — For generating Leaflet.js-based interactive maps.
  * `folium.plugins` (HeatMap, TimestampedGeoJson) — For spatial density profiling and temporal map animations.
  * [branca.colormap](https://github.com/python-visualization/branca) — For building custom gradient scales mapping development indicators onto geography.

---

## 🚀 Getting Started Locally

To run the Jupyter Notebooks on your local machine, please follow the steps below:

### 1. Clone the Repository
```bash
git clone https://github.com/USERNAME/repository-name.git
cd repository-name
```

### 2. Set Up a Virtual Environment (Recommended)
```bash
python -m venv venv
# Activate the environment:
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install pandas numpy matplotlib seaborn folium scipy branca notebook
```

### 4. Launch Jupyter Notebook
```bash
jupyter notebook
```
Navigate to and open any of the following project notebooks:
* `001_PDRB_vs_IPM_Jatim_2023/` -> [PDRB_vs_IPM_Jatim_2023.ipynb](file:///d:/Projek/Data_Analyst/001_PDRB_vs_IPM_Jatim_2023/PDRB_vs_IPM_Jatim_2023.ipynb)
* `002_Analisis Realisasi FDI Indonesia 2019-2023/` -> [Analisis_Realisasi_FDI_Indonesia_2019_2023.ipynb](file:///d:/Projek/Data_Analyst/002_Analisis%20Realisasi%20FDI%20Indonesia%202019-2023/Analisis_Realisasi_FDI_Indonesia_2019_2023.ipynb)
* `003_Analisis Indeks Pembangunan Manusia (IPM) Jawa Timur 2021-2025/` -> [Analisis_Indeks_Pembangunan_Manusia_(IPM)_Jawa_Timur_Tahun_2021_2025.ipynb](file:///d:/Projek/Data_Analyst/003_Analisis%20Indeks%20Pembangunan%20Manusia%20(IPM)%20Jawa%20Timur%202021-2025/Analisis_Indeks_Pembangunan_Manusia_(IPM)_Jawa_Timur_Tahun_2021_2025.ipynb)

---

## 📈 Executive Summary of Project Findings

### 1. GRDP vs. HDI in East Java 2023
* **Moderate Positive Correlation ($r = 0.499$)**: Regional economic output is positively associated with human welfare, but does not guarantee high HDI due to structural disparities.
* **Significant Disparities**: The GRDP per capita ratio between the highest region (Kediri City) and the lowest (Pamekasan) is **22.7x**. The HDI gap spans **17.81 points** (Malang City highest vs. Sampang lowest).
* **Quadrant Classification (Klassen Typology)**:
  * **Q1 (High GRDP & High HDI)**: 13 prosperous regencies/cities with robust local economies.
  * **Q3 (Low GRDP & Low HDI)**: 13 priority regions requiring dual policy intervention (primarily in the Madura and Tapal Kuda regions).
  * **Q4 (Economic Anomaly)**: 6 high-output but lower-HDI regions (e.g., Bojonegoro, Tuban, Sumenep) heavily dominated by capital-intensive, extractive resource sectors.

### 2. FDI Realisation in Indonesia 2019-2023
* **Pandemic Resilience (2020)**: Independent t-test results ($p = 0.9661$) indicate that the mean FDI per sector did not undergo a statistically significant collapse compared to 2019. PE/VC and digital/healthcare investments compensated for declines in transportation and tourism.
* **Investment Super-Cycle (2022-2023)**: A massive surge in FDI was observed in 2022 (+46.6% YoY) and 2023 (+10.2% YoY). The "Basic Metal Industry" (mineral downstream processing/nickel battery ecosystem) represents the primary growth driver.
* **Temporal Trend**: Pearson correlation analysis ($r = 0.9296, p = 0.0222$) confirms that post-pandemic FDI growth is structurally robust rather than cyclical.

### 3. Spatial-Temporal HDI Trends in East Java 2021-2025
* **Interactive Spatio-Temporal Maps**: Utilises Folium *CircleMarkers* with a custom colour scale (red-to-green) to visualize regional development achievements, as well as spatial density profiling via *HeatMaps*.
* **Interactive Temporal Animations**: Implements *TimestampedGeoJson* animations to display the progression of regional development status over time, capturing key transitions of regencies graduating from "Medium" to "High" HDI categories.

---

## 📬 Contact & Collaboration
Feel free to open an *Issue* or *Pull Request* to discuss regional economic development, spatial data analysis, or economic policy modeling.

* **Author**: [Your Name]
* **LinkedIn**: [Your LinkedIn Profile]
* **Email**: [Your Email Address]
