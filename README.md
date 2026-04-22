# Policy & Data Intelligence Tools Suite

## Live Applications

### 1. Macroeconomic Analysis & Country Brief Platform

https://economic-analysis-report-generator.vercel.app/
Integrated macroeconomic dashboard combining multi-indicator analysis and automated country report generation.

---

### 2. Trade in Services Data Explorer

https://trade-in-services-data-explorer-tool.streamlit.app/
Interactive visualization of OECD BaTIS data with granular EBOPS-level trade insights.

---

### 3. Services Trade Dependency Analysis

https://services-trade-partner-dependency-analysis.streamlit.app/#services-trade-dependency-analysis
Analytical tool to compute dependency ratios in services trade across countries and years.

---

### 4. Mangrove Monitoring (Gazi Bay, Kenya)

https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya
Geospatial machine learning application tracking mangrove loss and regeneration using satellite data.

---

## Detailed Overview (Expand Sections)

<details>
<summary><b>Macroeconomic Analysis & Country Brief Platform</b></summary>

This application integrates multiple analytical tools within a unified interface.

* The **Macro Analyzer** loads by default
* Use navigation buttons to switch between modules
* The **Country Brief Generator** produces structured 4-page reports using live data

Each module operates on a shared data pipeline, ensuring consistency across outputs.

A browser-based system designed to automate the *Country at a Glance* workflow used in development finance institutions. Tasks that typically require several hours of manual compilation are reduced to seconds.

> Note: Initial load may take a few seconds due to backend startup latency.

</details>

---

<details>
<summary><b>Trade in Services Data Explorer</b></summary>

Interactive visualization platform built on OECD BaTIS data.

* Covers **12 EBOPS service categories**
* Dynamic choropleth mapping
* Automated regional filtering
* Built using **Streamlit, DuckDB, and AWS S3**

Enables identification of granular competitive advantages in global services trade.

</details>

---

<details>
<summary><b>Services Trade Dependency Analysis</b></summary>

Economic analysis tool for measuring dependency structures in international services trade.

* Computes dependency ratios across partner countries
* Dynamic selection of country and year
* High-performance querying via S3-backed datasets
* Built using **Python and Plotly**

Supports policy analysis on trade concentration and vulnerability.

</details>

---

<details>
<summary><b>Mangrove Monitoring (Gazi Bay, Kenya)</b></summary>

Geospatial machine learning application for tracking coastal ecosystem changes.

Mangroves are difficult to distinguish from other vegetation in satellite imagery because all appear as dense green cover. To address this:

* A **Random Forest model** was trained
* Using **NDVI (vegetation health)** and **NDWI (water content)**
* To differentiate mangroves from other vegetation, water, and bare land

The system quantifies mangrove loss and recovery (2014–2025).

The approach is transferable to other domains such as agriculture, where similar models can distinguish crops grown in the same season (e.g., wheat, mustard, chickpea, barley) to estimate crop-wise sown area.

</details>
