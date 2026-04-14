# DSA210 Term Project - Turkey EV Charging Infrastructure Analysis
#### Spring 2025-2026
#### Sabancı University
#### Student/ID: Melike Yıldırım 32204

## Motivation
After my family switched to electric vehicles, range anxiety — the fear of running out of charge — quickly became a real concern in our daily lives. This made me wonder: is Turkey's charging infrastructure actually ready for the growing number of EV users?

As electric vehicle adoption continues to increase, the availability and distribution of public charging stations become increasingly important. This project aims to explore the current state of EV charging infrastructure in Turkey, evaluate its adequacy across different regions, and examine how well it supports the rapid growth of electric vehicles.

## Data Sources

 
| File | Source | Description | Year |
|------|--------|-------------|------|
| `(Mart 2026) Hangi şehirde kaç tane elektrikli araç şarj istasyonu var.xlsx` | Donanım Haber (source: EPDK — Energy Market Regulatory Authority) | Provincial charging station counts derived from EPDK's official licensing registry (`lisans.epdk.gov.tr`), compiled and published by Donanım Haber (14,811 total stations) | March 2026 |
| `Cinsiyete Göre Nüfus_nip.tuik.xlsx` | TÜİK — ADNKS | Province-level population data | 2025 |
| `İllere göre motorlu kara taşıtları sayısı.xls` | TÜİK | Road motor vehicles by province (81 provinces, 12 vehicle categories) | 2026 |
| `Motorlu Kara Taşıt Sayısı.xls` | TÜİK | National annual time series of registered vehicles by type | 1966–2026 |
| `Trafiğe Kayıtlı Otomobillerin Yakıt Cinsine Göre Dağılımı.xls` | TÜİK | National annual breakdown of registered cars by fuel type (gasoline, diesel, LPG, hybrid, electric) | 2004–2026 |
| `EV Data Explorer 2025.xlsx` | IEA | Country-level EV stock, sales, and public charging point counts; Turkey has 154 historical records | 2012–2024 |
 

## Planned Analysis
 
**Stage 1 — Data cleaning and integration**
- Merge provincial charging station counts with TÜİK vehicle and population data
- Compute infrastructure adequacy metrics: stations per 10,000 registered cars, stations per 100,000 population
 
**Stage 2 — Exploratory Data Analysis**
- National EV and hybrid growth trends (2004–2026) from fuel-type time series
- Geographic distribution of charging stations across 81 provinces
- IEA international comparison for Turkey's EV trajectory
 
**Stage 3 — Statistical testing and ML**
- Hypothesis tests: is infrastructure significantly concentrated in a few provinces? Has charger growth kept up with EV adoption?
- K-means clustering of provinces by infrastructure readiness profile
- Regression model: station density as a function of vehicle stock and population
 
---
 
## Tools
 
- **Python** — all analysis and modeling
- **Pandas** — data cleaning and integration
- **Matplotlib / Seaborn / Folium** — visualization and provincial maps
- **Scikit-learn** — clustering and regression
- **Statsmodels** — hypothesis testing
 
---
## Notes on Data Limitations & AI Usage
 
- The Donanım Haber charging station dataset (March 2026) aggregates figures from operator websites and may not capture every private or semi-public station.
- The sarj.dev API (used in early exploration) returned 8,895 records without explicit timestamps; it was replaced by the Donanım Haber dataset for greater reliability and recency.
- Provincial vehicle data and population are from 2024; the charging station snapshot is from March 2026. This small temporal gap is acknowledged as a limitation.

- AI tools such as ChatGPT and Claude were used for guidance in code development, debugging, and refining analysis explanations throughout the project.
