# 🛠️ Analytical Tools & Applications Portfolio

<div align="center">

[![Economic Analysis](https://img.shields.io/badge/📊_Economic_Analysis-Live-4CAF50?style=for-the-badge)](https://economic-analysis-report-generator.vercel.app/)
[![Trade Analytics](https://img.shields.io/badge/🌐_Services_Trade_Explorer-Live-2196F3?style=for-the-badge)](https://trade-in-services-data-explorer-tool.streamlit.app/)
[![Dependency Analysis](https://img.shields.io/badge/📈_Dependency_Tool-Live-FF9800?style=for-the-badge)](https://services-trade-partner-dependency-analysis.streamlit.app/)
[![Geospatial ML](https://img.shields.io/badge/🛰️_Mangrove_Monitor-Live-009688?style=for-the-badge)](https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya)

</div>

---

## 🚀 Quick Access Dashboard

| Tool | Use Case | Tech Stack | Status |
|------|----------|------------|--------|
| [**Economic Analysis Suite**](https://economic-analysis-report-generator.vercel.app/) | Macro analysis & country briefs | React, Vercel | 🟢 Live |
| [**Services Trade Explorer**](https://trade-in-services-data-explorer-tool.streamlit.app/) | OECD BaTIS data visualization | Streamlit, DuckDB, AWS S3 | 🟢 Live |
| [**Trade Dependency Analyzer**](https://services-trade-partner-dependency-analysis.streamlit.app/) | Partner concentration metrics | Python, Plotly | 🟢 Live |
| [**Mangrove Monitor (GEE)**](https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya) | Ecological change detection | Google Earth Engine, ML | 🟢 Live |

---

## 📚 Detailed Documentation

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
| **Frontend** | React, Streamlit |
| **Backend** | Vercel Serverless, Python |
| **Data Processing** | DuckDB, Pandas, NumPy |
| **Cloud Infrastructure** | AWS S3, Vercel CDN |
| **Geospatial** | Google Earth Engine |
| **Machine Learning** | Scikit-learn (Random Forest) |
| **Visualization** | Plotly, Recharts, Leaflet |
| **APIs** | World Bank, OECD, IMF |

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
- **Satellite imagery**: Weekly updates (Google Earth Engine)

### Browser Compatibility
All tools are optimized for modern browsers:
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari

---

## 📬 Feedback & Support

For questions, bug reports, or feature requests, please use the respective application's interface or contact the development team.

---

<div align="center">

**Last Updated**: January 2025

[![Portfolio](https://img.shields.io/badge/View-Full_Portfolio-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/swaraj-s-54a955167/)

</div>
