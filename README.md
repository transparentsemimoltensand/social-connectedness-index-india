# Meta Social Connectedness Index (SCI) India Map

A spatial data engineering and visualization pipeline that maps social connection density across 700+ Indian districts using Meta's Social Connectedness Index (SCI) data, GADM 4.1 boundary geometries, and DuckDB/GeoPandas.

---

## Features

- **DuckDB Analytics Engine**: Replaced memory-heavy Pandas merge operations with DuckDB SQL for processing million-row SCI pairwise tables with minimal memory overhead.
- **Dynamic Relative Peak Normalization**: Computes dynamic relative connectivity scaling on district selection, adjusting color gradients via interactive JavaScript/Leaflet bindings.
- **Boundary Optimization & Spatial Cleaning**: Unified inconsistent state-level administrative prefixes (`ZXX` codes) to standardized `IND` ISO boundary schemas, eliminating dangling non-matching district records.
- **Custom Spatial Overlay Injection**: Integrated PoK and Aksai Chin geographic boundaries with spatial containment algorithms for complete map coverage.
- **Interactive Multi-Level Viewports**: Dual-mode rendering enabling both District-to-District Connectivity Analysis and District-to-Country Global Outward Social Linkage Mapping.

---

## Tech Stack

- **Data Processing & SQL**: DuckDB, Pandas, PyArrow
- **Geospatial & Spatial GIS**: GeoPandas, Shapely, PyCountry
- **Interactive Mapping**: Folium, Leaflet.js, JavaScript
- **Environment**: Python 3.10+

---

## Quickstart & Usage

1. Clone the repository:
   git clone https://github.com/your-username/meta-sci-india-map.git
   cd meta-sci-india-map

2. Run the pipeline script to clean datasets, build DuckDB lookup tables, and generate the standalone interactive map:
   python build_interactive_sci_map.py

3. Open `india_sci_interactive.html` in any web browser to explore the interactive dashboard.

---

## Data Validation Summary

- **Total Pairwise Links Evaluated**: 100% In-Memory Processing via DuckDB
- **Pre-Cleanup Alignment Match Rate**: ~96%
- **Post-Unification Match Rate**: 100% Zero Dangling Entities
- **Net Matching Improvement**: +28+ Districts Mapped Correctly
