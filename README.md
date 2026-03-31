# DSA210 Term Project - Turkey EV Charging Infrastructure Analysis
#### Spring 2025-2026
#### Sabancı University
#### Student/ID: Melike Yıldırım 32204

## Motivation
After my family switched to electric vehicles, range anxiety — the fear of running out of charge — quickly became a real concern in our daily lives. This made me wonder: is Turkey's charging infrastructure actually ready for the growing number of EV users?

As electric vehicle adoption continues to increase, the availability and distribution of public charging stations become increasingly important. This project aims to explore the current state of EV charging infrastructure in Turkey, evaluate its adequacy across different regions, and examine how well it supports the rapid growth of electric vehicles.

## Data Sources
The project utilizes dynamically acquired API data and official statistics:
- **sarj.dev API** — Primary data source providing real-time geographic coordinates (latitude/longitude) and operator metadata for thousands of active EV charging stations across Turkey.
- **Turkey Provincial GeoJSON** — Spatial boundary data used to accurately map and assign charging station coordinates to specific provinces via spatial join techniques.
- **TÜİK (Turkish Statistical Institute)** — Provincial-level transportation data (registered EVs) and population statistics, used to normalize infrastructure metrics (e.g., stations per capita, stations per EV).
- **IEA (International Energy Agency)** — Global EV Data Explorer statistics for macro-level EV adoption trends and historical benchmarks.

## Planned Analysis
The analysis will include the following steps:
- Data collection and preprocessing (including spatial mapping of API coordinates)
- Exploratory Data Analysis (EDA)
- Visualization of charging station distribution across Turkey
- Comparison between regional EV growth and charging infrastructure
- Hypothesis testing on infrastructure readiness
- Machine learning models (e.g., clustering regions by infrastructure coverage)

## Tools
- Python
- Pandas & GeoPandas (for spatial data processing)
- Requests (for API data acquisition)
- Matplotlib / Seaborn
- Scikit-learn
