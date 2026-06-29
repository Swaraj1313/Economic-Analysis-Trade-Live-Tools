# 🛠️ Analytical Tools & Applications Portfolio

<div align="center">

[![Economic Analysis](https://img.shields.io/badge/📊_Economic_Analysis-Live-4CAF50?style=for-the-badge)](https://economic-analysis-report-generator.vercel.app/)
[![Trade Analytics](https://img.shields.io/badge/🌐_Services_Trade_Explorer-Live-2196F3?style=for-the-badge)](https://trade-in-services-data-explorer-tool.streamlit.app/)
[![Dependency Analysis](https://img.shields.io/badge/📈_Dependency_Tool-Live-FF9800?style=for-the-badge)](https://services-trade-partner-dependency-analysis.streamlit.app/)
[![Regional Networks](https://img.shields.io/badge/🕸️_Trade_Networks-Live-9C27B0?style=for-the-badge)](https://swaraj1313.github.io/Regional-Trade-Integration/index.html)
[![Geospatial ML](https://img.shields.io/badge/🛰️_Mangrove_Monitor-Live-009688?style=for-the-badge)](https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya)
[![Macro Simulator](https://img.shields.io/badge/🤖_Macro_Simulator-Live-E91E63?style=for-the-badge)](http://3.217.177.12/)
[![OSINT Platform](https://img.shields.io/badge/🛰️_OSINT_Platform-Live-FF5722?style=for-the-badge)](https://osint-dashboard-kxhsy4gvspevhvzvo36ah9.streamlit.app/)

</div>

---
## 🚀 Quick Access Dashboard

| Tool | Use Case | Tech Stack | Status |
|------|----------|------------|--------|
| [**Economic Analysis Suite**](https://economic-analysis-report-generator.vercel.app/) | Macro analysis & country briefs | React, Vercel | 🟢 Live |
| [**Services Trade Explorer**](https://trade-in-services-data-explorer-tool.streamlit.app/) | OECD BaTIS data visualization | Streamlit, DuckDB, AWS S3 | 🟢 Live |
| [**Trade Dependency Analyzer**](https://services-trade-partner-dependency-analysis.streamlit.app/) | Trade Partner concentration metrics | Python, Plotly | 🟢 Live |
| [**Regional Trade Networks**](https://swaraj1313.github.io/Regional-Trade-Integration/index.html) | Networks & trade bloc analysis | Python, NetworkX, Plotly, GitHub Pages | 🟢 Live |
| [**Mangrove Monitor (GEE)**](https://swaraj1313.users.earthengine.app/view/mangrove-monitor-gazibay-kenya) | ML based Mangrooves change detection | Google Earth Engine, ML | 🟢 Live |
| [**OSINT Intelligence Platform**](https://osint-dashboard-kxhsy4gvspevhvzvo36ah9.streamlit.app/) | Real-time monitoring & geolocation with AI| Streamlit, AWS Bedrock, GEE, Telegram | 🟢 Live |
| [**Macro Policy Simulator**](http://3.217.177.12/) | AI-driven macroeconomic forecasting | React, Flask, Moirai AI, VAR, ARIMA | 🟢 Live* |

> ## 👉 AVAILABILITY NOTE for Macro Policy Simulator
> It takes around 120 seconds for it to process if you see "SYNTHESIZING VECTORS" its working. This application requires allocation of dedicated compute resources therefore may not be accessible at all times. It is typically available 📅 Monday to Friday, 🕒 12:30 to 14:30 IST (UTC+5:30). If the application is temporarily unavailable, or if you would like access outside scheduled hours, kindly contact info.swarajsingh@gmail.com.

---

## 📚 Detailed Documentation

<details>
<summary>🛰️ <b>OSINT INTELLIGENCE PLATFORM</b> &nbsp;·&nbsp; <i>Real-Time Multilingual Intelligence Monitoring</i></summary>

<br>

### Overview

A multilingual real-time intelligence and monitoring platform for open-source data collection, geo-locating events and AI-powered analysis. Built for research and policy contexts including transnational organised crime, disaster response and public health surveillance.

This tool collects and analyses open-source intelligence from public Telegram channels and news sources in real time. It monitors content across multiple languages including Burmese, Thai, Chinese, French and English, translates it automatically and uses AI to flag suspicious activity, classify each message into an intelligence category and score how credible the information is. The platform currently tracks organised crime networks in Southeast Asia including scam compounds, arms dealing and sanctions evasion, alongside active crises such as the Philippines earthquake and the DRC Ebola outbreak. Location intelligence is enriched through satellite data from Google Earth Engine - flood extent and building damage are detected using Sentinel-1 SAR imagery that works through cloud cover, new construction at known compound locations is tracked using Sentinel-2 spectral analysis and vegetation stress for food security monitoring is measured against a five-year baseline. Analysts can explore findings through four views - a live intelligence feed showing flagged messages with AI-generated notes, an interactive network graph mapping relationships between people, organisations and locations extracted from the data, a geographic map plotting incidents by location with colour-coded typology markers and a briefing generator that synthesises collected intelligence into a structured analytical report with recommended actions.

### What It Does

The platform ingests content from public Telegram channels and news sources, translates non-English content natively using AI, classifies each message against a 16-category intelligence typology, scores credibility on four dimensions and surfaces actionable analyst findings through a live dashboard.

**Currently monitoring:**
- Organised crime and sanctions evasion networks in Southeast Asia (Myanmar, Thailand, Singapore)
- Disaster response signals (Philippines M7.8 earthquake, June 2026)
- Public health surveillance (DRC/Uganda Ebola outbreak, WHO PHEIC)
- Humanitarian events and state actor activity across the Middle East and Africa

**What it can also monitor with channel list updates:**
- Trafficking recruitment networks and scam compound operations
- Cryptocurrency laundering and blockchain address tracking
- Terrorist financing and violent extremism signals
- Migration and displacement patterns
- Food security and agricultural stress
- Any public Telegram channel or news feed in any language

### Dashboard Pages

**Intelligence Feed**

![Intelligence Feed](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/intelligence_feed.png)

The main analyst view. Shows all priority-flagged and AI-flagged messages sorted by composite credibility score. Each card displays the source channel, timestamp, matched keyword, four-dimension credibility scores (src / coh / corr / manip) and the AI analyst note explaining what was flagged and why.

**Credibility score dimensions:**
- `src` - Source reliability: track record and editorial standards of the channel (1-5)
- `coh` - Content coherence: whether the claims are specific, internally consistent and verifiable (1-5)
- `corr` - Corroboration: how many independent sources report the same claim (1-5)
- `manip` - Manipulation risk: indicators of coordinated inauthentic behaviour or disinformation (1-5, where 5 means lowest risk)

Composite score is a weighted average. 4.0 and above is high credibility. 2.5-3.99 is medium. Below 2.5 is low.

---

**Network Graph**

![Network Graph](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/network_graph.png)

Interactive entity relationship map. Each node is a named entity extracted from messages. Node size reflects mention frequency. Lines between nodes mean those entities appeared together in the same message.

| Colour | Code | Meaning |
|--------|------|---------|
| Orange | PERSON | A named individual (e.g. Min Aung Hlaing, Emmanuel Macron) |
| Blue | ORG | An organisation (e.g. Justice For Myanmar, Hamas, OCHA) |
| Green | GPE | Geopolitical entity - country, city or territory (e.g. Myanmar, Singapore, Gaza) |
| Purple | LOC | A physical location (e.g. Golden Triangle, Strait of Hormuz) |
| Gold/Yellow | NORP | Nationality, religious or political group (e.g. French, Israeli, Palestinian) |
| Pink | FAC | A facility or building (e.g. KK Park, a specific compound) |
| Light pink | EVENT | A named event (e.g. World Cup, Operation 9) |

The table beneath the graph shows top entities by mention count. These are not keywords - they are named entities extracted from message text by a language model.

---

**Geographic Map**

![Geographic Map](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/gi_map0.png)

![Geographic Map - OSINT Crime](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/gi_map1.png)

![Geographic Map - Disaster Response](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/gi_map2.png)

Incident markers plotted at known locations extracted from classified messages. Click any marker for details. Larger dots indicate higher credibility.

| Colour | Typology |
|--------|----------|
| Red | Arms Dealing |
| Orange | Sanctions Evasion / Scam Compound Operations |
| Dark red | Human Trafficking / Forced Labour |
| Blue-grey | Cyber-enabled Fraud |
| Purple | Money Laundering / Crypto Laundering |
| Dark purple | Terrorist Financing |
| Dark blue | State Actor / Military Activity |
| Green | Natural Disaster |
| Light green | Humanitarian Event |
| Blue | Public Health Event |
| Pink | Corruption |
| Grey | Disinformation |

---

**Briefing Generator**

Select a monitoring profile, typology and credibility filter. The platform synthesises all matching classified messages into a structured intelligence brief with six sections: Executive Summary, Key Findings, Entity Analysis, Emerging Patterns, Recommended Actions and Verification Requirements. Download as a text file for distribution.

### Architecture

```
Telegram channels
       |
Module 1 - Ingestion and AI triage
  Language detection
  Nova Lite translate + triage (non-English)
  NER entity extraction (spaCy)
  Crypto address detection
  SQLite database
       |
Module 2 - Classification and credibility scoring
  16-category typology classification (Amazon Nova Micro)
  Four-dimension credibility scoring
  Cross-message corroboration (sentence-transformers)
  Actionable flag generation
       |
Module 3 - Satellite enrichment (GEE)
  SAR flood mapping (Sentinel-1)
  Earthquake damage detection (SAR coherence)
  Compound construction monitoring (NDBI, Sentinel-2)
  NDVI anomaly detection (drought/food security)
       |
S3 (Parquet)
       |
Module 4 - Dashboard
  Streamlit + Folium + PyVis + Amazon Nova Lite
```

### Monitoring Profiles

| Profile | Focus | Active channels |
|---------|-------|----------------|
| OSINT / Organised Crime | Scam compounds, arms dealing, sanctions evasion, Myanmar | MyanmarNowNews, bnionline, narinjara, khitthitnews |
| Disaster Response | Earthquakes, floods, cyclones, Philippines | abscbnnews, aljazeeraglobal, bbcworld |
| Public Health | Outbreaks, epidemics, PHEIC | aljazeeraglobal, bbcworld |
| Humanitarian / MEAL | Displacement, food insecurity, GBV | aljazeeraglobal, bbcworld |
| Migration | Border movements, Rohingya, irregular crossings | aljazeeraglobal, MyanmarNowNews |

### Tech Stack
- Python 3.12, Streamlit, Telethon
- Amazon Bedrock (Nova Micro and Nova Lite)
- sentence-transformers, spaCy
- Google Earth Engine
- Folium, PyVis
- AWS S3, PyArrow/Parquet, SQLite

### Access
🔗 **[Launch Platform](https://osint-dashboard-kxhsy4gvspevhvzvo36ah9.streamlit.app/)**

![OSINT Platform](https://img.shields.io/badge/Stack-Streamlit_|_AWS_Bedrock_|_GEE_|_Telegram-FF5722?style=flat-square)

</details>

<details>
<summary>🤖 <b>MACRO POLICY SIMULATOR</b> &nbsp;·&nbsp; <i>AI Macroeconomic Forecasting</i></summary>

<br>

### Overview
An exploratory research and development testbed evaluating zero-shot time series foundation models (TSFMs) for macroeconomic forecasting across 35 economies. The core research question is whether a large-scale pre-trained AI model can generalise to sovereign macroeconomic data without any fine-tuning, and how its forecasts compare against conventional econometric baselines and IMF projections.

### What It Does
Runs AI-generated macroeconomic forecasts for 35 economies over the 2026 to 2030 horizon using IMF WEO historical data as context. The simulator places Moirai forecasts alongside VAR, ARIMA and IMF reference projections so all four can be directly compared on the same chart.

### Forecasting Models

The simulator runs four distinct forecasting approaches and combines three of them into a Consensus Forecast.

**Moirai (Zero-Shot TSFM)**
Powered by Salesforce Moirai-1.0-R-large, a deep transformer pre-trained on 27 billion time series observations from the LOTSA corpus. The model performs zero-shot multivariate inference, jointly modelling all five macroeconomic variables without any country-specific training. Probabilistic inference with 3,000 Monte Carlo samples produces full uncertainty bands (p10 to p90).

**VAR (Vector Autoregression)**
A classical multivariate econometric model that captures linear interdependencies across all five variables simultaneously. Lag order is selected via AIC (maximum 4 lags). Each variable is tested for stationarity using the Augmented Dickey-Fuller test and first-differenced if non-stationary, with level reconstruction applied to forecasts.

**ARIMA (AutoRegressive Integrated Moving Average)**
A univariate time series model fitted independently per variable. The model uses an ARIMA(2,d,1) specification where the differencing order d is determined automatically via ADF stationarity testing. A fallback to ARIMA(1,d,0) is applied if the primary specification fails to converge.

**Consensus Forecast**
An equal-weighted average of Moirai, VAR and ARIMA. The IMF projection is deliberately excluded from the consensus as it incorporates expert judgement rather than being a purely statistical forecast. The IMF is displayed as a separate reference line.

### Key Features
- **Shock Transmission Engine**: Translates oil price shocks and domestic variable shifts to macroeconomic impacts via country-specific elasticity coefficients across CPI, Current Account and Fiscal Balance.
- **Uncertainty bands**: p10 to p90 probability intervals visualised as shaded bands on the Moirai forecast.
- **Nowcast Override panel**: Pre-fills 2025 values from IMF WEO actuals. Allows analyst overrides on projected values before inference runs.
- **Multi-model comparison tab**: Side-by-side view of all five forecast series (Moirai, VAR, ARIMA, IMF, Consensus) with a summary statistics table.
- **35 economies**: Coverage across South Asia, Southeast Asia, East Asia, Europe, North America, Latin America, Middle East and Africa.

### Variables Modelled
| Code | Indicator |
|------|-----------|
| NGDP_RPCH | Real GDP Growth (%) |
| PCPIPCH | Inflation, CPI (%) |
| GGXCNL_NGDP | Fiscal Balance (% GDP) |
| BCA_NGDPD | Current Account (% GDP) |
| GGXWDG_NGDP | Public Debt (% GDP) |

### Architecture
- **Frontend**: React 19, Vite, Recharts
- **Backend & AI Engine**: Python, Flask, Moirai (uni2ts), statsmodels
- **Inference**: 3,000-sample probabilistic forecasting, seed-locked at 42 for reproducibility
- **Data**: Live IMF DataMapper API, 35-year historical context window (1991 to 2025), winsorized at 5th to 95th percentile
- **Deployment**: AWS EC2 (m7i-flex.large, us-east-1), Nginx, gunicorn, systemd

### Known Limitations
- Moirai does not enforce fiscal accounting identities
- VAR and ARIMA use winsorized data which may bias toward mean reversion
- Run-to-run variance of approximately +/- 0.1pp exists in Moirai median despite fixed seed due to non-deterministic CPU operations
- COVID-era patterns in training data may introduce spurious correlations

### Access
🔗 **[Launch Simulator](http://3.217.177.12/)**

![Macro Simulator](https://img.shields.io/badge/Stack-React_|_Flask_|_Moirai_|_VAR_|_ARIMA-E91E63?style=flat-square)

</details>

<details>
<summary>📊 <b>ECONOMIC ANALYSIS REPORT GENERATOR</b> &nbsp;·&nbsp; <i>Macro Analysis & Country Briefs</i></summary>

<br>

### Overview
An integrated analytical platform combining macroeconomic diagnostics with automated country reporting. Designed for development finance workflows where baseline data compilation currently consumes significant analyst time.

### Key Features
- **Dual-mode interface**: Macro Analyzer (default) + Country Brief Generator
- **One-click navigation**: Toggle between modules using top-left controls
- **Automated report generation**: Select country and time period to download a structured 4-page Word document
- **Live data integration**: Real-time World Bank API connectivity
- **Production-ready outputs**: Charts, tables and statistical observations formatted for institutional use

### Target Users
Development finance professionals at secretariats and member states requiring rapid baseline data compilation (reduces time from approximately 4 hours to under 5 minutes per country).

### Technical Notes
- First load may take 3 to 5 seconds due to serverless cold start
- All modules share a unified data pipeline for consistency
- Built on Vercel for global CDN distribution

### Access
🔗 **[Launch Application](https://economic-analysis-report-generator.vercel.app/)**

</details>

<details>
<summary>🌐 <b>SERVICES TRADE DATA EXPLORER</b> &nbsp;·&nbsp; <i>OECD BaTIS Granular Analysis</i></summary>

<br>

### Overview
Interactive visualization platform for the OECD Balanced Trade in Services (BaTIS) dataset, enabling granular analysis of global services trade flows at the EBOPS category level.

### What It Does
Breaks down aggregate "Total Services" trade into 12 detailed EBOPS categories:
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
- **Automated regional filtering**: Drill down by continent, sub-region or custom groups
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
<summary>📈 <b>TRADE PARTNER DEPENDENCY ANALYZER</b> &nbsp;·&nbsp; <i>Concentration Risk Metrics</i></summary>

<br>

### Overview
Quantitative tool for calculating economic dependency ratios in bilateral services trade relationships. Identifies concentration risks and diversification opportunities.

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
<summary>🕸️ <b>REGIONAL TRADE INTEGRATION & NETWORK ANALYSIS DASHBOARD</b> &nbsp;·&nbsp; <i>Graph Theory Applied to Global Trade Architecture</i></summary>

<br>

### Overview
A research-grade interactive dashboard applying graph theory and network science to bilateral trade data, mapping how Asia's trade architecture has structurally evolved from 2000 to 2024 and benchmarking it against African regional integration.

Most trade analysis asks *how much* countries trade. This dashboard asks a fundamentally different question:

> **How is trade structurally organised, and how has that organisation changed over 24 years?**

**Data Source:** IMF Direction of Trade Statistics (DOTS)

### Dashboard Modules

**1. Asia Trade Network 2024**
Force-directed network graph using Louvain Community Detection to identify emergent trade blocs and Force-Atlas-2 to physically position countries by trade gravity. Three structural communities revealed: a North-East Asian core (China/Japan), an ASEAN manufacturing zone (Singapore, Malaysia as bridges) and a Central Asian periphery.

**2. Intra-Regional ASEAN to Asia Sankey**
Trade Intensity Index-based Sankey diagram mapping how ASEAN's trade energy distributes across broader Asia, distinguishing structurally significant corridors from size-driven relationships.

**3. Shift in Trade Influence (Asia 2000 to 2024)**
Interactive dumbbell chart showing every Asian economy's change in Eigenvector Centrality between 2000 and 2024. Distinguishes "Throughway" economies (embedded in value chains, high centrality) from "Endpoint" economies (raw material exporters or final goods importers, low centrality).

| Feature | Vietnam (Central) | India / Pakistan (Peripheral) |
|---|---|---|
| FDI Type | Efficiency-seeking (export-oriented) | Market-seeking (domestic consumption) |
| Shock Absorption | High, diversified partners enable re-routing | Low, reliance on limited corridors |
| Technology Transfer | High, embedded in global value chains | Low, limited spillovers |

**4. Evolution of Trade Hubs (Power Rankings 2000 to 2024)**
Animated bump chart of top 10 Asian trade hubs ranked by Eigenvector Centrality across benchmark years. Headline finding: Vietnam surged to #3 by 2024, overtaking Taiwan, Singapore and South Korea, providing structural confirmation of the "China Plus One" manufacturing shift.

**5. Asian Trade Network Topology (2000 to 2024)**
Tracks Network Density, Clustering Coefficient and Reciprocity across six benchmark years using binary adjacency networks, isolating structural organisation from trade volumes.

| Year | Network Density | Clustering Coefficient | Reciprocity |
|---|---|---|---|
| 2000 | 0.3048 | 0.5996 | 0.5198 |
| 2024 | 0.4126 | 0.5829 | 0.5448 |

**6. Asia vs. Africa Integration Gap & Post-COVID Divergence**
Comparative structural analysis of intra-regional integration. Africa grew from 0.17 to 0.29 network density over 24 years, but a post-COVID divergence is visible where Africa's integration momentum stalled while Asia accelerated to 0.41. The constraint is not the number of countries but the sparseness of economic linkages between them.

### Methodology

| Metric | What It Captures |
|---|---|
| **Trade Intensity Index (TII)** | Whether bilateral trade is disproportionately strong relative to both countries' global shares |
| **Eigenvector Centrality** | Structural influence, quality not just quantity of trade connections |
| **Network Density** | Breadth of integration across the full regional network |
| **Clustering Coefficient** | Depth of integration, value chain formation and trade bloc cohesion |
| **Reciprocity** | Balance of trade relationships, mutual vs. one-directional dependence |
| **Louvain Community Detection** | Algorithmically emergent trade blocs without pre-defined groupings |

### Technical Stack
- **Network Construction & Analysis**: Python, NetworkX
- **Community Detection**: python-louvain (Louvain algorithm)
- **Network Layout**: ForceAtlas2
- **Visualisations**: Plotly, Pyvis
- **Data Processing**: Pandas, NumPy
- **Hosting**: GitHub Pages

### Access
🔗 **[Launch Dashboard](https://swaraj1313.github.io/Regional-Trade-Integration/index.html)**

![Network Analysis](https://img.shields.io/badge/Stack-Python_|_NetworkX_|_Plotly-9C27B0?style=flat-square)
![Hosted On](https://img.shields.io/badge/Hosted-GitHub_Pages-181717?style=flat-square&logo=github)

</details>

<details><summary>🛰️ <b>MANGROVE CONSERVATION MONITOR</b> &nbsp;·&nbsp; <i>Geospatial ML for Ecological Change Detection</i></summary>

<br>

### The Challenge
Mangroves are difficult to distinguish from other vegetation in standard satellite imagery because of similar visual appearance to terrestrial forests, overlap with wetland vegetation in spectral signatures, seasonal variations affecting color and density and persistent cloud cover in tropical coastal regions.

Standard RGB satellite images cannot reliably separate mangroves from surrounding land cover.

### The Solution
A supervised machine learning approach using the Random Forest algorithm trained on spectral indices beyond visible light.

### How It Works
Satellites capture not just visible light but also infrared wavelengths invisible to human eyes. Different surfaces reflect these wavelengths in unique patterns.

**Training Features**:
- **NDVI (Normalized Difference Vegetation Index)**: Measures vegetation health via near-infrared reflection
- **NDWI (Normalized Difference Water Index)**: Measures water content via shortwave infrared absorption

**Unique Mangrove Signature**:
Mangroves have a distinct spectral fingerprint because they are simultaneously dense vegetation (high NDVI) in a waterlogged environment (high NDWI). The model learns this combination pattern to autonomously classify coastal land cover.

- ## Visual Outputs

### 2015 False Color
![2015_False_Color](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/2015_false_color.png)

### 2025 False Color
![2025](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/2025_false_color.png)

### Mangrove Change (Gain/Loss)
![Change](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/mangroves_gain_loss.png)

### ESA Comparison
![ESA](https://raw.githubusercontent.com/Swaraj1313/Economic-Analysis-Trade-Live-Tools/main/asset/esa_layover.png)

### Outputs
- **Decadal change detection**: Quantified mangrove loss/recovery (2014 to 2025)
- **Land cover classification**: Mangroves, water, bare land, other vegetation
- **Conservation impact assessment**: Measure effectiveness of protection efforts
- **Time-series analysis**: Track ecological shifts over multiple years

### Case Study: Gazi Bay, Kenya
Autonomous monitoring of mangrove ecosystems along the Kenyan coast, tracking both depletion from human activity and recovery from conservation interventions.

### Broader Applications
The same methodology can be applied to agriculture (distinguishing between crops grown in the same season for accurate sown area estimation), forest monitoring, urban expansion detection and wetland conservation.

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
| **Econometrics** | VAR, ARIMA, statsmodels |
| **Network Analysis** | NetworkX, python-louvain, ForceAtlas2 |
| **Cloud Infrastructure** | AWS EC2 & S3, Vercel CDN, GitHub Pages |
| **Geospatial** | Google Earth Engine |
| **Machine Learning** | Moirai (Time Series Foundation Model), Scikit-learn (Random Forest), Amazon Bedrock (Nova) |
| **Visualization** | Plotly, Pyvis, Recharts, Leaflet, Folium |
| **APIs** | World Bank, OECD, IMF DOTS, IMF WEO DataMapper, Telegram |

</div>

---

## 📝 Usage Notes

### First-Time Access
- Initial load may take 3 to 5 seconds on first request (serverless cold start)
- Subsequent requests are instantaneous
- All applications are production-ready and actively maintained

### Data Freshness
- **Economic indicators**: Real-time via API (World Bank, IMF)
- **Trade data**: Annual updates following OECD release cycle
- **Network analysis**: IMF DOTS (benchmark years 2000 to 2024)
- **Satellite imagery**: Weekly updates (Google Earth Engine)
- **OSINT intelligence**: Near real-time, synced after every ingestion run

### Browser Compatibility
All tools are optimized for modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari

---

## 📬 Feedback & Support

For questions, bug reports or feature requests, please email info.swarajsingh@gmail.com

---

<div align="center">

**Last Updated**: June 2026

[![Portfolio](https://img.shields.io/badge/View-Full_Portfolio-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/swaraj-s-54a955167/)

</div>
