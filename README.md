# 🛠️ Analytical Tools & Applications Portfolio

<div align="center">

[![Economic Analysis](https://img.shields.io/badge/📊_Economic_Analysis-Live-4CAF50?style=for-the-badge)](https://economic-analysis-report-generator.vercel.app/)
[![Trade Analytics](https://img.shields.io/badge/🌐_Services_Trade_Explorer-Live-2196F3?style=for-the-badge)](https://trade-in-services-data-explorer-tool.streamlit.app/)
[![Dependency Analysis](https://img.shields.io/badge/📈_Dependency_Tool-Live-FF9800?style=for-the-badge)](https://services-trade-partner-dependency-analysis.streamlit.app/)
[![Regional Networks](https://img.shields.io/badge/🕸️_Trade_Networks-Live-9C27B0?style=for-the-badge)](https://swaraj1313.github.io/Regional-Trade-Integration/index.html)
[![Geospatial ML](https://img.shields.io/badge/🛰️_Mangrove_Monitor-Live-009688?style=for-the-badge)](https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya)
[![Macro Simulator](https://img.shields.io/badge/🤖_Macro_Simulator-Live-E91E63?style=for-the-badge)](http://3.229.14.75/)

</div>

---

## 🚀 Quick Access Dashboard

| Tool | Use Case | Tech Stack | Status |
|------|----------|------------|--------|
| [**Economic Analysis Suite**](https://economic-analysis-report-generator.vercel.app/) | Macro analysis & country briefs | React, Vercel | 🟢 Live |
| [**Services Trade Explorer**](https://trade-in-services-data-explorer-tool.streamlit.app/) | OECD BaTIS data visualization | Streamlit, DuckDB, AWS S3 | 🟢 Live |
| [**Trade Dependency Analyzer**](https://services-trade-partner-dependency-analysis.streamlit.app/) | Partner concentration metrics | Python, Plotly | 🟢 Live |
| [**Regional Trade Networks**](https://swaraj1313.github.io/Regional-Trade-Integration/index.html) | Network topology & trade bloc analysis | Python, NetworkX, Plotly, GitHub Pages | 🟢 Live |
| [**Mangrove Monitor (GEE)**](https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya) | Ecological change detection | Google Earth Engine, ML | 🟢 Live |
| [**Macro Policy Simulator**](http://3.229.14.75/) | AI-driven macroeconomic forecasting baselines | React, Flask, Moirai AI | 🟢 Live* |

> ## 👉 AVAILIBLITY NOTE for Macro Policy Simulator
> This application requires allocation of dedicated compute resources therefore may not be accessible at all times. It's typically available 📅 Monday–Friday, 🕒 09:00–18:00 IST (UTC+5:30). If the application is temporarily unavailable, or if you would like access outside scheduled hours, kindly contact info.swarajsingh@gmail.com.

---

## 📚 Detailed Documentation

<details>
<summary>🧮 <b>Macro Policy Simulator</b> • <i>AI Macroeconomic Forecasting</i></summary>

<br>

### Overview
An exploratory research and development testbed evaluating zero-shot time series foundation models (TSFMs) for macroeconomic forecasting in developing economies. It evaluates how well large-scale pre-trained AI generalizes to sovereign macroeconomic data compared to conventional baselines like VAR, DSGE, and IMF projections.

### What It Does
Runs AI-generated macroeconomic baselines for 35 economies (2026–2030) using IMF WEO data as context, placing them alongside IMF reference projections so the two can be directly compared. 

### Key Features
- **Zero-shot forecasting engine**: Powered by **Moirai** (Salesforce AI), a deep transformer pre-trained on 27 billion time series observations.
- **Multivariate modeling**: Jointly models 5 macroeconomic variables natively (Real GDP Growth, CPI Inflation, Fiscal Balance, Current Account, Public Debt).
- **Shock Transmission Engine**: Translates oil price shocks and domestic variable shifts to macroeconomic impacts via elasticity coefficients.
- **Uncertainty bands**: 500-sample Monte Carlo inference yielding full [p10–p90] probability intervals.

### Architecture
- **Frontend**: React 19, Vite, Recharts
- **Backend & AI Engine**: Python, Flask, Moirai (uni2ts), Pandas
- **Deployment**: AWS EC2 (c7i-flex.large)

### Access
🔗 **[Launch Simulator](http://3.229.14.75/)**

![Macro Simulator](https://img.shields.io/badge/Stack-React_|_Flask_|_Moirai-E91E63?style=flat-square)

</details>

<details>
<summary>📊 <b>Economic Analysis Report Generator</b> • <i>Macro Analysis & Country Briefs</i></summary>

<br>

### Overview
An **integrated analytical platform** combining macroeconomic diagnostics with automated country reporting. Designed for development finance workflows where baseline data compilation currently consumes significant analyst time.

### Key Features
- **Dual-mode interface**: Macro Analyzer (default) + Country Brief Generator
- **One-click navigation**: Toggle between modules using top-left controls
- **Automated report generation**: Select country and time period → Download structured 4-page Word document
- **Live data integration**: Real-time World Bank API connectivity
- **Production-ready outputs**: Charts, tables, and statistical observations formatted for institutional use

### Target Users
Development finance professionals at secretariats and member states requiring rapid baseline data compilation (reduces time from ~4 hours to <5 minutes per country).

### Technical Notes
- First load may take 3-5 seconds due to serverless cold start
- All modules share unified data pipeline for consistency
- Built on Vercel for global CDN distribution

### Access
🔗 **[Launch Application](https://economic-analysis-report-generator.vercel.app/)**

</details>

<details>
<summary>🌐 <b>Services Trade Data Explorer</b> • <i>OECD BaTIS Granular Analysis</i></summary>

<br>

### Overview
Interactive visualization platform for **OECD Balanced Trade in Services (BaTIS)** dataset, enabling granular analysis of global services trade flows at the EBOPS category level.

### What It Does
Breaks down aggregate "Total Services" trade into **12 detailed EBOPS categories**:
- Manufacturing Services on Physical Inputs
- Maintenance and Repair Services
- Transport (Passenger & Freight)
- Travel (Business & Personal)
- Construction
- Insurance and Pension Services
- Financial Services
- Charges for IP Use
- Telecommunications, Computer & Information Services
- Other Business Services
- Personal, Cultural & Recreational Services
- Government Goods & Services

### Key Features
- **Dynamic choropleth maps**: Global trade flow visualization
- **Automated regional filtering**: Drill down by continent, sub-region, or custom groups
- **Bilateral trade analysis**: Export/import flows between specific partners
- **Competitive advantage identification**: Pinpoint sector-specific strengths

### Architecture
- **Frontend**: Streamlit (Python)
- **Query Engine**: DuckDB (in-memory analytics)
- **Data Lake**: AWS S3 (Parquet files for performance)
- **Update Frequency**: Annual (OECD release cycle)

### Access
🔗 **[Launch Explorer](https://trade-in-services-data-explorer-tool.streamlit.app/)**

![Services Trade Explorer](https://img.shields.io/badge/Stack-Streamlit_|_DuckDB_|_AWS_S3-FF4B4B?style=flat-square)

</details>

<details>
<summary>📈 <b>Trade Partner Dependency Analyzer</b> • <i>Concentration Risk Metrics</i></summary>

<br>

### Overview
Quantitative tool for calculating **economic dependency ratios** in bilateral services trade relationships. Identifies concentration risks and diversification opportunities.

### Use Cases
- **Risk assessment**: Measure exposure to single trading partners
- **Policy planning**: Identify over-reliance on specific markets
- **Diversification strategy**: Pinpoint alternative partner opportunities
- **Negotiation preparation**: Understand bargaining positions based on mutual dependence

### Methodology
Calculates dependency indices using:
- Partner share of total exports/imports
- Bilateral trade intensity ratios
- Herfindahl-Hirschman Index (HHI) for concentration
- Year-over-year trend analysis

### Features
- **Automated country/year selection**: Dynamic dropdowns from live data
- **Interactive visualizations**: Plotly-based charts with drill-down capability
- **High-performance querying**: S3-backed Parquet data for sub-second response times
- **Export functionality**: Download analysis results as CSV

### Access
🔗 **[Launch Analyzer](https://services-trade-partner-dependency-analysis.streamlit.app/)**

![Dependency Tool](https://img.shields.io/badge/Tech-Python_|_Plotly_|_AWS-3776AB?style=flat-square)

</details>

<details>
<summary>🕸️ <b>Regional Trade Integration & Network Analysis Dashboard</b> • <i>Graph Theory Applied to Global Trade Architecture</i></summary>

<br>

### Overview
A research-grade interactive dashboard applying **graph theory and network science** to bilateral trade data — mapping how Asia's trade architecture has structurally evolved from 2000 to 2024, and benchmarking it against African regional integration.

Most trade analysis asks *how much* countries trade. This dashboard asks a fundamentally different question:

> **How is trade structurally organised — and how has that organisation changed over 24 years?**

**Data Source:** IMF Direction of Trade Statistics (DOTS)

### Dashboard Modules

**1. 🕸️ Asia Trade Network 2024**
Force-directed network graph using **Louvain Community Detection** to identify emergent trade blocs and **Force-Atlas-2** to physically position countries by trade gravity. Three structural communities revealed — a North-East Asian core (China/Japan), an ASEAN manufacturing zone (Singapore, Malaysia as bridges), and a Central Asian periphery.

**2. 🌊 Intra-Regional ASEAN to Asia Sankey**
Trade Intensity Index-based Sankey diagram mapping how ASEAN's trade energy distributes across broader Asia — distinguishing structurally significant corridors from size-driven relationships.

**3. 📍 Shift in Trade Influence — Asia (2000–2024)**
Interactive dumbbell chart showing every Asian economy's change in **Eigenvector Centrality** between 2000 and 2024. Distinguishes "Throughway" economies (embedded in value chains, high centrality) from "Endpoint" economies (raw material exporters or final goods importers, low centrality).

| Feature | Vietnam (Central) | India / Pakistan (Peripheral) |
|---|---|---|
| FDI Type | Efficiency-seeking (export-oriented) | Market-seeking (domestic consumption) |
| Shock Absorption | High — diversified partners enable re-routing | Low — reliance on limited corridors |
| Technology Transfer | High — embedded in global value chains | Low — limited spillovers |

**4. 🏆 Evolution of Trade Hubs — Power Rankings (2000–2024)**
Animated bump chart of top 10 Asian trade hubs ranked by Eigenvector Centrality across benchmark years. Headline finding: **Vietnam surged to #3 by 2024**, overtaking Taiwan, Singapore, and South Korea — structural confirmation of the "China Plus One" manufacturing shift.

**5. 📐 Asian Trade Network Topology (2000–2024)**
Tracks Network Density, Clustering Coefficient, and Reciprocity across six benchmark years using binary adjacency networks — isolating structural organisation from trade volumes.

| Year | Network Density | Clustering Coefficient | Reciprocity |
|---|---|---|---|
| 2000 | 0.3048 | 0.5996 | 0.5198 |
| 2024 | 0.4126 | 0.5829 | 0.5448 |

**6. 🌍 Asia vs. Africa Integration Gap & Post-COVID Divergence**
Comparative structural analysis of intra-regional integration. Africa grew from 0.17 to 0.29 network density over 24 years — but a **post-COVID divergence** is visible where Africa's integration momentum stalled while Asia accelerated to 0.41. The constraint is not the number of countries but the sparseness of economic linkages between them.

### Methodology

| Metric | What It Captures |
|---|---|
| **Trade Intensity Index (TII)** | Whether bilateral trade is disproportionately strong relative to both countries' global shares |
| **Eigenvector Centrality** | Structural influence — quality, not just quantity, of trade connections |
| **Network Density** | Breadth of integration across the full regional network |
| **Clustering Coefficient** | Depth of integration — value chain formation and trade bloc cohesion |
| **Reciprocity** | Balance of trade relationships — mutual vs. one-directional dependence |
| **Louvain Community Detection** | Algorithmically emergent trade blocs without pre-defined groupings |

### Technical Stack
- **Network Construction & Analysis**: Python · NetworkX
- **Community Detection**: python-louvain (Louvain algorithm)
- **Network Layout**: ForceAtlas2
- **Visualisations**: Plotly · Pyvis
- **Data Processing**: Pandas · NumPy
- **Hosting**: GitHub Pages

### Access
🔗 **[Launch Dashboard](https://swaraj1313.github.io/Regional-Trade-Integration/index.html)**

![Network Analysis](https://img.shields.io/badge/Stack-Python_|_NetworkX_|_Plotly-9C27B0?style=flat-square)
![Hosted On](https://img.shields.io/badge/Hosted-GitHub_Pages-181717?style=flat-square&logo=github)

</details>

<details>
<summary>🛰️ <b>Mangrove Conservation Monitor</b> • <i>Geospatial ML for Ecological Change Detection</i></summary>

<br>

### The Challenge
Mangroves are **difficult to distinguish from other vegetation** in standard satellite imagery because:
- Similar visual appearance to terrestrial forests from above
- Overlap with wetland vegetation in spectral signatures
- Seasonal variations affect color and density
- Cloud cover in tropical coastal regions

Standard RGB satellite images cannot reliably separate mangroves from surrounding land cover.

### The Solution
**Supervised Machine Learning** approach using Random Forest algorithm trained on spectral indices beyond visible light.

### How It Works
Satellites capture not just visible light, but also **infrared wavelengths** invisible to human eyes. Different surfaces reflect these wavelengths in unique patterns:

**Training Features**:
- **NDVI (Normalized Difference Vegetation Index)**: Measures vegetation health via near-infrared reflection
- **NDWI (Normalized Difference Water Index)**: Measures water content via shortwave infrared absorption

**Unique Mangrove Signature**:
Mangroves have a distinct "spectral fingerprint" because they're simultaneously:
- Dense vegetation (high NDVI) + Waterlogged environment (high NDWI)

The model learns this combination pattern to autonomously classify coastal land cover.

### Outputs
- **Decadal change detection**: Quantified mangrove loss/recovery (2014-2025)
- **Land cover classification**: Mangroves, water, bare land, other vegetation
- **Conservation impact assessment**: Measure effectiveness of protection efforts
- **Time-series analysis**: Track ecological shifts over multiple years

### Case Study: Gazi Bay, Kenya
Autonomous monitoring of mangrove ecosystems along the Kenyan coast, tracking both depletion from human activity and recovery from conservation interventions.

### Broader Applications
The same methodology can be applied to:
- **Agriculture**: Distinguish between crops grown in the same season (wheat, mustard, chickpea, barley) for accurate sown area estimation
- **Forest monitoring**: Track deforestation and reforestation
- **Urban expansion**: Detect land-use changes over time
- **Wetland conservation**: Monitor ecosystem health

### Technical Stack
- **Platform**: Google Earth Engine
- **Algorithm**: Random Forest (supervised learning)
- **Input Data**: Landsat/Sentinel multispectral imagery
- **Features**: Engineered spectral indices (NDVI, NDWI)
- **Output**: Classified land cover maps with change detection

### Access
🔗 **[Launch Monitor](https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya)**

![GEE Application](https://img.shields.io/badge/Platform-Google_Earth_Engine-34A853?style=flat-square)
![ML Model](https://img.shields.io/badge/Model-Random_Forest-FF6F00?style=flat-square)

</details>

---

## 🔧 Technology Stack Overview

<div align="center">

| Category | Technologies |
|----------|-------------|
| **Frontend** | React 19, Vite, Streamlit |
| **Backend** | Vercel Serverless, Python, Flask |
| **Data Processing** | DuckDB, Pandas, NumPy |
| **Network Analysis** | NetworkX, python-louvain, ForceAtlas2 |
| **Cloud Infrastructure** | AWS EC2 & S3, Vercel CDN, GitHub Pages |
| **Geospatial** | Google Earth Engine |
| **Machine Learning** | Moirai (Time Series Foundation Model), Scikit-learn (Random Forest) |
| **Visualization** | Plotly, Pyvis, Recharts, Leaflet |
| **APIs** | World Bank, OECD, IMF DOTS, IMF WEO |

</div>

---

## 📝 Usage Notes

### First-Time Access
- Initial load may take 3-5 seconds on first request (serverless cold start)
- Subsequent requests are instantaneous
- All applications are production-ready and actively maintained

### Data Freshness
- **Economic indicators**: Real-time via API (World Bank, IMF)
- **Trade data**: Annual updates following OECD release cycle
- **Network analysis**: IMF DOTS (benchmark years 2000–2024)
- **Satellite imagery**: Weekly updates (Google Earth Engine)

### Browser Compatibility
All tools are optimized for modern browsers:
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari

---

## 📬 Feedback & Support

For questions, bug reports, or feature requests, please email info.swarajsingh@gmail.com

---

<div align="center">

**Last Updated**: May 2026

[![Portfolio](https://img.shields.io/badge/View-Full_Portfolio-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/swaraj-s-54a955167/)

</div>
