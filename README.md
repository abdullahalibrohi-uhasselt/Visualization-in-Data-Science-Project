# Madrid Air Quality Visualisation Project

A data visualisation project exploring Madrid's air quality between 2001 and 2018 using hourly readings from the city's monitoring stations. Built in R with R Markdown. The project answers three research questions about long-term trends, spatial distribution, and seasonal patterns through nine static visualisations.

All charts are saved as PNGs in the `figures/` directory and compiled into a single HTML report when the notebook is knitted.

## Table of Contents

- [Project Structure](#project-structure)
- [Requirements](#requirements)
- [Dataset Setup](#dataset-setup)
- [How to Run](#how-to-run)
- [Reproducing the Visualisations](#reproducing-the-visualisations)
- [Output Files](#output-files)

## Project Structure

```
.
├── Madrid_implementation.Rmd      
├── Madrid_implementation.html     
├── data/                         
│   ├── madrid_2001.csv … madrid_2018.csv
│   └── stations.csv
├── figures/                       
│   ├── 01_trend_pct_change.png
│   ├── 02_bubble_map_2018.png
│   ├── 03_diverging_change.png
│   ├── 04_seasonal_heatmap.png
│   ├── 05_slope_graph.png
│   ├── 06_small_multiples.png
│   ├── 07_parallel_coords.png
│   ├── 08_radar.png
│   └── 09_dashboard_composite.png
└── README.md
```

## Requirements

This project requires R 4.0+ and the following libraries:

- `tidyverse`
- `lubridate`
- `sf`
- `ggrepel`
- `scales`
- `viridis`
- `patchwork`
- `fmsb`
- `png`

You can install dependencies with:

```
install.packages(c("tidyverse", "lubridate", "sf", "ggrepel",
                   "scales", "viridis", "patchwork", "fmsb", "png"))
```
## Dataset Setup

You must have the following CSV files (from the Air Quality in Madrid (2001-2018) dataset on Kaggle) available:

- `madrid_2001.csv`
- `madrid_2002.csv`
- `madrid_2003.csv`
- `madrid_2004.csv`
- `madrid_2005.csv`
- `madrid_2006.csv`
- `madrid_2007.csv`
- `madrid_2008.csv`
- `madrid_2009.csv`
- `madrid_2010.csv`
- `madrid_2011.csv`
- `madrid_2012.csv`
- `madrid_2013.csv`
- `madrid_2014.csv`
- `madrid_2015.csv`
- `madrid_2016.csv`
- `madrid_2017.csv`
- `madrid_2018.csv`
- `stations.csv`

## How to Run

1. Ensure all CSV files are in the `data/` directory next to the notebook.
2. Open RStudio and navigate to the project folder.
3. Open the main notebook and click Knit:

```
Madrid_implementation.Rmd
```
The notebook will load and clean the data, run the analysis, print progress, and save all generated visualisations automatically.

## Reproducing the Visualisations

All visualisations are generated and saved as PNG files in the `figures/` folder. Each figure is named according to its content (e.g., `01_trend_pct_change.png`, `08_radar.png`, etc.).

No manual intervention is needed, simply knitting the notebook will create the full set of outputs, including:

- Multi-line trend chart
- Geographic bubble map
- Diverging bar chart
- Seasonal heatmap
- Slope graph
- Small multiples
- Parallel coordinates
- Radar chart
- Comprehensive dashboard

To view a visualisation: Open any PNG file from the `figures/` directory using your image viewer.

To reproduce everything: Delete the contents of the `figures/` folder, then re-knit the notebook.

## Output Files

- All generated images are saved in `figures/` (created automatically).
- A cleaned data cache is saved as `data_clean.rds` to speed up subsequent runs.
- A self-contained HTML report is saved as `Madrid_implementation.html`.
- Console output summarises the analysis progress and row counts.
---

**Project by Group 6**
Members: Muhammad Atif (2502637), Bilal Malik (2505964), Abdullah Ali Brohi (2501314), Muhammad Ibrahim (2502094)
