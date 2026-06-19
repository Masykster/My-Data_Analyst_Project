# 🗺️ HDI Map of East Java — Spatial-Temporal Geospatial Visualisation (2021-2025)

This project conducts a spatial and temporal trend analysis of the **Human Development Index (HDI) / Indeks Pembangunan Manusia (IPM)** across 38 regencies and cities in East Java Province over a 5-year timeline from **2021 to 2025**. 

Using advanced web-based geospatial visualisations, this project maps regional development disparities, tracks quality-of-life improvements, and produces interactive timeline animations.

---

## 📂 Repository Structure & Dataset

* **Analysis Notebook**: [Analisis_Indeks_Pembangunan_Manusia_(IPM)_Jawa_Timur_Tahun_2021_2025.ipynb](file:///d:/Projek/Data_Analyst/003_Analisis%20Indeks%20Pembangunan%20Manusia%20(IPM)%20Jawa%20Timur%202021-2025/Analisis_Indeks_Pembangunan_Manusia_(IPM)_Jawa_Timur_Tahun_2021_2025.ipynb)
* **Data Directory**: [data/](file:///d:/Projek/Data_Analyst/003_Analisis%20Indeks%20Pembangunan%20Manusia%20(IPM)%20Jawa%20Timur%202021-2025/data/)
  * The dataset consists of 5 yearly CSV files detailing HDI scores by regency/city:
    * `Indeks Pembangunan Manusia... 2021.csv`
    * `Indeks Pembangunan Manusia... 2022.csv`
    * `Indeks Pembangunan Manusia... 2023.csv`
    * `Indeks Pembangunan Manusia... 2024.csv`
    * `Indeks Pembangunan Manusia... 2025.csv`
  * Source: BPS (Central Bureau of Statistics) East Java.

---

## 🛠️ Methodology & Analytical Workflow

1. **Data Loading & Integration**: Ingests time-series data across 5 years from CSV. The notebook supports direct uploads (for Google Colab) and local path detection (for local Jupyter environments).
2. **Geospatial Coordinate Matching**:
   * Cleans HDI values and standardizes administrative names.
   * Merges development statistics with GPS coordinates (Latitude & Longitude) for East Java regencies and cities based on official administrative boundaries.
3. **Trend Analysis with Seaborn (Static)**:
   * Identifies the **Top 10** regencies/cities with the highest HDI and the **Bottom 10** development priority regions for the latest available year.
   * Plots multi-year trajectory lines for the top 5 and bottom 5 regions to evaluate growth velocities.
   * Visualises the distribution and yearly variance of HDI using annual boxplots.
4. **Interactive Geospatial Mapping (Folium)**:
   * **Folium HeatMap**: Maps the spatial density and concentration of HDI scores across East Java to detect regional welfare clusters (e.g., prominent high-density clusters around Surabaya Metropolitan Area and Malang Raya).
   * **CircleMarker Map with Tooltip**: Places interactive markers on each region with color-coded gradients (red representing low HDI scaling to green representing high HDI) using `branca`. Hovering over markers displays localized popups with precise development scores.
   * **Timeline Animation (TimestampedGeoJson)**: Builds a playable timeline widget (play, pause, speed control) animating spatial development shifts over the 5-year period.
5. **Interactive HTML Map Export**: Exports all generated Folium maps to standalone HTML files for web deployment or presentations without requiring a running Python kernel.

---

## 📈 Key Insights

* **Persistent Regional Disparities**: Urban centers (e.g., Surabaya, Malang, Madiun) consistently register HDI scores in the "Very High" category (> 80). Conversely, island regions (e.g., Madura) and several eastern regencies (Tapal Kuda) populate the lower ranks, falls within the "Medium" category (60 - 70).
* **Positive Trajectories**: All 38 regencies and cities show a steady upward trend in HDI scores over the 2021–2025 period, indicating improvements in educational access, basic healthcare, and purchasing power post-pandemic.
* **Category Transitions**: The interactive timeline animation visually captures the transition of several regencies as they successfully elevate their status from the "Medium" development tier to "High."

---

## 🎨 Interactive Maps Exported

1. `heatmap_ipm.html` — Geospatial concentration of human development in East Java.
2. `circlemarker_ipm.html` — Coordinate marker map with red-to-green gradations showing precise regional scores.
3. `timeline_animasi_ipm.html` — A time-series map player illustrating HDI shifts from 2021 to 2025.

---

## 🚀 How to Run

Launch the notebook [Analisis_Indeks_Pembangunan_Manusia_(IPM)_Jawa_Timur_Tahun_2021_2025.ipynb](file:///d:/Projek/Data_Analyst/003_Analisis%20Indeks%20Pembangunan%20Manusia%20(IPM)%20Jawa%20Timur%202021-2025/Analisis_Indeks_Pembangunan_Manusia_(IPM)_Jawa_Timur_Tahun_2021_2025.ipynb) in your preferred Jupyter environment. Ensure the `folium`, `branca`, and `pandas` packages are installed.
