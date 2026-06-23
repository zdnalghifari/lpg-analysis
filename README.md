<h1 align="center">⛽ LPG Distribution Analysis</h1>
<p align="center">
  <b>Spatial Analysis of LPG Distribution in Tangerang Selatan</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/GeoPandas-139C5A?style=for-the-badge&logo=pandas&logoColor=white"/>
  <img src="https://img.shields.io/badge/Folium-77B829?style=for-the-badge&logo=python&logoColor=white"/>
</p>

---

## 📌 Overview

A geospatial analysis project that maps and analyzes the distribution of **LPG (Liquefied Petroleum Gas) merchants and distribution points** across **Tangerang Selatan**, Indonesia. The analysis includes coverage mapping, population correlation, and spatial clustering of LPG supply points.

---

## 🔍 Analysis Pipeline

```
  [ Web Scraping ]
  scraping_data_lpg.ipynb
  → Collect LPG merchant locations
          │
          ▼
  [ Data Cleaning ]
  extract_coordinates.ipynb
  → Remove duplicates & out-of-bounds coordinates
          │
          ▼
  [ Spatial Analysis ]
  lpg_vis.ipynb
  → Coverage analysis at 300m / 500m / 1000m radius
  → Population correlation per district
          │
          ▼
  [ Output ]
  → Maps, charts, and CSV reports
```

---

## 🗺️ Visualizations

| Output | Description |
|--------|-------------|
| `map_tangsel.png` | Spatial distribution map of LPG points across Tangerang Selatan |
| `persebaran_kecamatan.jpg` | LPG distribution chart by district |
| `bar_plot_jumlah_penduduk_per_pangkalan.png` | Population per LPG base bar chart |
| `scatter_plot_jumlah_penduduk_pangkalan.png` | Population vs LPG points scatter plot |

---

## 📊 Key Outputs

| Coverage Radius | Output File |
|----------------|-------------|
| 300 m | `uncovered_analysis_300m.csv` |
| 500 m | `uncovered_analysis_500m.csv` |
| 1000 m | `uncovered_analysis_1000m.csv` |

Distribution data available by:
- **Kecamatan** (district): `persebaran_kecamatan.csv / .xlsx`
- **Kelurahan** (sub-district): `persebaran_kelurahan.csv / .xlsx`

---

## 🗂️ Project Structure

```
lpg-analysis/
├── scraping_data_lpg.ipynb          # Web scraping LPG merchant data
├── extract_coordinates.ipynb         # Coordinate cleaning & validation
├── lpg_vis.ipynb                     # Spatial visualization & analysis
├── adm_tangsel.geojson               # Tangerang Selatan admin boundaries
├── adm_tangsel.qmd                   # Quarto document
├── loc_lpg_tangsel_2.csv             # Final cleaned LPG locations
├── merchants_tangsel_final.csv       # Final merchant dataset
├── persebaran_kecamatan.*            # Distribution by district
├── persebaran_kelurahan.*            # Distribution by sub-district
├── uncovered_analysis_300m.csv       # Areas uncovered within 300m
├── uncovered_analysis_500m.csv       # Areas uncovered within 500m
├── uncovered_analysis_1000m.csv      # Areas uncovered within 1000m
├── map_tangsel.png                   # Output map
└── persebaran_kecamatan.jpg          # Distribution chart
```

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas geopandas folium matplotlib seaborn jupyter requests
```

### Run

```bash
git clone https://github.com/zdnalghifari/lpg-analysis.git
cd lpg-analysis
jupyter notebook
```

Open notebooks in this order:
1. `scraping_data_lpg.ipynb` — collect raw data
2. `extract_coordinates.ipynb` — clean & validate
3. `lpg_vis.ipynb` — analyze & visualize

---

## 🛠️ Tech Stack

| Purpose | Library |
|---------|---------|
| Data manipulation | Pandas, NumPy |
| Geospatial analysis | GeoPandas, Shapely |
| Interactive maps | Folium |
| Visualization | Matplotlib, Seaborn |
| Reporting | Quarto |
| Web scraping | Requests, BeautifulSoup |
