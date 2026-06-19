# 🌏 FDI Realisation Analysis in Indonesia 2019–2023
### *The Impact of the COVID-19 Pandemic on Foreign Direct Investment by Economic Sector*

This project provides a comprehensive analysis of **Foreign Direct Investment (FDI) / Penanaman Modal Asing (PMA)** realisations in Indonesia during the 2019–2023 period. The study tests hypotheses regarding the impact of the COVID-19 pandemic on investment stability, sectoral volatility, and post-pandemic structural recovery (*investment super-cycle*).

---

## 📂 Repository Structure & Dataset

* **Analysis Notebook**: [Analisis_Realisasi_FDI_Indonesia_2019_2023.ipynb](file:///d:/Projek/Data_Analyst/002_Analisis%20Realisasi%20FDI%20Indonesia%202019-2023/Analisis_Realisasi_FDI_Indonesia_2019_2023.ipynb)
* **Data Directory**: [data/](file:///d:/Projek/Data_Analyst/002_Analisis%20Realisasi%20FDI%20Indonesia%202019-2023/data/)
  * The dataset consists of 5 yearly CSV files detailing quarterly FDI realisations by economic sector (in millions of USD):
    * `Realisasi Investasi... 2019.csv`
    * `Realisasi Investasi... 2020.csv`
    * `Realisasi Investasi... 2021.csv`
    * `Realisasi Investasi... 2022.csv`
    * `Realisasi Investasi... 2023.csv`
  * Data source: Indonesia Investment Coordinating Board (BKPM) / Ministry of Investment.

---

## 🛠️ Statistical Hypothesis Testing & Methodology

This analysis employs rigorous inferential statistical methods to substantiate trend observations:

1. **Normality Test (Shapiro-Wilk)**: Tests whether the distribution of FDI across economic sectors is normal. The results confirm a *non-normal (highly right-skewed)* distribution, which is typical as a few dominant capital-intensive sectors (such as Basic Metal Industry) attract the vast majority of foreign capital.
2. **Independent Two-Sample t-Test**:
   * **H1 (Direct Pandemic Impact)**: Compares the mean FDI per sector between 2019 (pre-pandemic) and 2020 ( pandemic onset). The statistical test yields $t = -0.0428$ and $p = 0.9661$, **failing to reject the null hypothesis**. This suggests there was no statistically significant collapse in the average FDI across sectors, demonstrating the resilience of Indonesia's investment ecosystem.
   * **H2 (Long-Term Structural Shift)**: Compares 2019 and 2023 to verify the presence of a structural transformation ($t = -1.4894, p = 0.1435$).
3. **One-Way ANOVA**: Simultaneously compares mean investments across all five years, yielding $F = 1.1240$ and $p = 0.3490$ (failing to reject $H_0$).
4. **Pearson Correlation Analysis**: Measures the linear relationship between time (annual timeline) and total nominal FDI. The result shows an extremely strong and significant positive correlation ($r = 0.9296, p = 0.0222$), confirming that post-pandemic investment growth represents a persistent structural uptrend rather than a temporary cyclical spike.

---

## 📈 Narrative of Investment Phases

Based on the statistical and visual findings, Indonesia's investment dynamics can be categorised into three main phases:

### 🔴 PHASE 1 — Pandemic Shock (2020)
* **Status**: Total FDI reached **US$28.7 billion** (a minor growth of +1.6% YoY compared to 2019's US$28.2 billion).
* **Observation**: Uncertainty increased, as evidenced by a rise in the standard deviation across sectors. Service-oriented sectors such as transportation, warehousing, telecommunications, and tourism contracted due to global lockdowns. Conversely, primary and strategic manufacturing sectors remained resilient.

### 🟠 PHASE 2 — Early Recovery (2021)
* **Status**: Total FDI increased to **US$31.1 billion** (+8,5% YoY).
* **Observation**: National vaccination rollouts and relaxed mobility restrictions stimulated the manufacturing sector. The **Basic Metal, Metal Goods, Non-Machinery and Equipment Industry** sector expanded rapidly, marking the onset of the *nickel downstream processing boom* and electric vehicle battery supply chain investments.

### 🟢 PHASE 3 — Investment Super-Cycle (2022–2023)
* **Status**:
  * 2022 recorded **US$45.6 billion** in FDI (a massive +46.6% YoY growth — the largest annual increase).
  * 2023 reached a record high of **US$50.3 billion** (+10.2% YoY).
* **Observation**: A structural transformation in the investment portfolio took place. Downstream mineral processing (nickel, bauxite smelters) dominated foreign capital inflows, followed closely by investments in renewable energy infrastructure and data centres.

---

## 📊 Core Visualizations

The notebook generates several premium visualizations:
1. **Annual FDI Trends & Growth Rates**: A dual-axis bar and line chart illustrating total annual volume and percentage growth.
2. **Quarterly Heatmap**: A seasonal heatmap mapping investments by quarter to detect quarterly performance trends, highlighting a recurrent surge in Q4 realisations.
3. **Sector Distribution (Box + Violin Plots)**: Displays the spread of investments across sectors, revealing skewness and highlighting prominent outliers.
4. **Top 8 Dominant Sectors**: A dynamic horizontal bar chart ranking the top 8 sectors absorbing foreign capital annually.
5. **Radar Chart of Sectoral Composition**: A spiderweb chart with custom drop shadows that visually demonstrates how Indonesia's investment portfolio shifted from 2019 to 2023.

---

## 🚀 How to Run

Execute the Jupyter Notebook [Analisis_Realisasi_FDI_Indonesia_2019_2023.ipynb](file:///d:/Projek/Data_Analyst/002_Analisis%20Realisasi%20FDI%20Indonesia%202019-2023/Analisis_Realisasi_FDI_Indonesia_2019_2023.ipynb) in your local environment. Ensure that the packages `scipy`, `pandas`, `seaborn`, and `matplotlib` are installed.
