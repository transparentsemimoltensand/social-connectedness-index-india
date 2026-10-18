Here is your updated README.md content in clean Markdown format.

Since you do not have a standalone local script, the Quickstart & Usage section has been updated to reflect running the pipeline directly via your Kaggle environment or accessing the live hosted maps.

Meta Social Connectedness Index (SCI) India Map
A spatial data engineering and visualization pipeline that maps social connection density across 700+ Indian districts using Meta's Social Connectedness Index (SCI) data, GADM 4.1 boundary geometries, and DuckDB/GeoPandas.

Interactive Dashboards & Kaggle Execution
Interactive District-to-District Map: Explore Live Map

Interactive District-to-Country Map: Explore Live Map

Executable Pipeline & Analysis: View Notebook on Kaggle

Features
DuckDB Analytics Engine: Replaced memory-heavy Pandas merge operations with DuckDB SQL for processing million-row SCI pairwise tables with minimal memory overhead.

Dynamic Relative Peak Normalization: Computes dynamic relative connectivity scaling on district selection, adjusting color gradients via interactive JavaScript/Leaflet bindings.

Boundary Optimization & Spatial Cleaning: Unified inconsistent state-level administrative prefixes (ZXX codes) to standardized IND ISO boundary schemas, eliminating dangling non-matching district records.

Custom Spatial Overlay Injection: Integrated PoK and Aksai Chin geographic boundaries with spatial containment algorithms for complete map coverage.

Interactive Multi-Level Viewports: Dual-mode rendering enabling both District-to-District Connectivity Analysis and District-to-Country Global Outward Social Linkage Mapping.

Tech Stack
Data Processing & SQL: DuckDB, Pandas, PyArrow

Geospatial & Spatial GIS: GeoPandas, Shapely, PyCountry

Interactive Mapping: Folium, Leaflet.js, JavaScript

Environment: Python 3.10+ (Kaggle Environment)

Quickstart & Usage
Open the full execution pipeline and data processing environment directly on Kaggle:
[https://www.kaggle.com/code/mohdfarhanshaikh/social-connectedness-index-india](https://www.kaggle.com/code/mohdfarhanshaikh/social-connectedness-index-india)

Fork or run the Kaggle notebook to execute the DuckDB processing queries, spatial boundary joins, and HTML rendering pipeline.

Access the generated interactive HTML dashboards directly via the hosted Hugging Face links listed above.

Data Validation Summary
Total Pairwise Links Evaluated: 100% In-Memory Processing via DuckDB

Pre-Cleanup Alignment Match Rate: ~96%

Post-Unification Match Rate: 100% Zero Dangling Entities

Net Matching Improvement: +28+ Districts Mapped Correctly
