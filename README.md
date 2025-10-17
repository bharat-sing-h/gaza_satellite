# Gaza Nighttime Light Analysis

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

Analysis of nighttime light changes in the Gaza Strip using VIIRS satellite data via Google Earth Engine.

---

## Project Overview

This project quantifies the change in nighttime light intensity over the Gaza Strip by comparing satellite imagery from a "before" period (Jan-Sep 2023) with an "after" period (Jan-Jun 2024). Nighttime light radiance, captured by the VIIRS satellite, serves as a proxy for electricity access, infrastructure integrity, and human activity.

The analysis is performed entirely within a Google Colab notebook using the Google Earth Engine (GEE) platform for large-scale geospatial data processing.

---

## Key Findings

The analysis reveals a significant and widespread reduction in nighttime light across the entire study area.

- **Overall Reduction:** An average decrease of **-56.4%** in nighttime light radiance was observed across the Gaza Strip.
- **Widespread Impact:** **55.1%** of the total area experienced a significant light reduction of more than 30%.
- **Temporal Trend:** The time-series data shows stable light levels throughout 2023, followed by a sharp and sustained drop beginning in late 2023 and continuing into 2024.

---

## Interactive Visualization

**Important:** The interactive map widget from `geemap` cannot be rendered in the static notebook preview on GitHub.

To explore the data layers, including the "before" and "after" imagery, percentage change, and areas of significant decrease, you must open the generated HTML file.

**[Click here to view the interactive map](https://htmlpreview.github.io/?https://github.com/bharat-sing-h/gaza_satellite/blob/main/interactive_map.html)**

---

## Methodology

The analysis follows these steps:
1.  **Setup:** Installs and imports necessary Python libraries (`earthengine-api`, `geemap`, `pandas`, `matplotlib`).
2.  **Authentication:** Connects to the Google Earth Engine (GEE) API.
3.  **Scope Definition:** Defines the Area of Interest (AOI) for the Gaza Strip and the "before" and "after" time periods.
4.  **Data Processing:** Fetches VIIRS DNB monthly composite imagery and creates median composites for both periods to reduce noise and cloud cover.
5.  **Change Detection:** Calculates the pixel-wise percentage change in light radiance and flags areas with a decrease greater than 30%.
6.  **Output Generation:** Produces the interactive map, statistical plots (histograms, time-series), and a summary report.

---

## How to Run the Analysis

To replicate this analysis, you will need a Google account with Google Earth Engine access enabled.

1.  **Prerequisites:**
    - A Google Account.
    - [Sign up for Google Earth Engine](https://code.earthengine.google.com/register).
    - Create a [Google Cloud project](https://console.cloud.google.com/) and enable the Earth Engine API.

2.  **Steps:**
    - Clone or download this repository.
    - Open the `Gaza_City_Satellite.ipynb` notebook in Google Colab.
    - When prompted, authenticate your Google account to grant access to GEE.
    - Run the cells sequentially to execute the analysis and generate the outputs.

---

## Data Source

- **Dataset:** VIIRS Day/Night Band (DNB) Monthly Composites.
- **Platform:** Google Earth Engine.

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
