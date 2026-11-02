# Modeling Austin Shared Micromobility Trip Duration

**STATS 500 — Regression Analysis | University of Michigan | Fall 2025**  
**Author:** Yifeng Huang

## Project overview

This course project uses the City of Austin's 2022 shared micromobility trip records to study how trip duration varies with trip distance, vehicle type, time of day, day of week, month, and trip-origin council district. It addresses two questions:

1. Which trip characteristics are associated with longer or shorter trips?
2. Which characteristics are associated with a trip lasting more than **10 minutes**?

## Data and statistical methods

- **Dataset:** 858,100 recorded trips from 2022; **294,309 complete observations** in the final modeling dataset after cleaning and filtering.
- **Data preparation:** Handling invalid records and missing values, creating a log-duration outcome and a binary long-trip indicator.
- **Exploratory analysis:** Distribution summaries and visualizations of trip duration, distance, and long-trip frequency.
- **Multiple linear regression:** Modeling log trip duration using trip distance and temporal, vehicle-type, and spatial covariates.
- **Logistic regression:** Modeling the probability that trip duration exceeds 10 minutes using the same explanatory variables.
- **Model interpretation and diagnostics:** Coefficient interpretation, statistical significance, and residual diagnostics.

## Selected findings

- Trip distance is a major predictor of both trip duration and the probability of a long trip.
- Vehicle type and time-related factors are also associated with trip length.
- Approximately **6.2%** of trips in the final modeling sample last longer than 10 minutes.
- The multiple linear regression model reports **R² = 0.2057**, indicating that substantial variation remains unexplained.

The results describe **associations, not causal effects**; see the full report for qualifications and limitations.

## Repository files

| File | Description |
| --- | --- |
| [`1.Rmd`](1.Rmd) | Original R Markdown analysis and R source code. |
| [`1.html`](1.html) | Rendered HTML report with analysis output and visualizations. |
| [`Project_Yifeng Huang_09130484.pdf`](Project_Yifeng%20Huang_09130484.pdf) | Original 12-page final project report. |
| [`500_project.pdf`](500_project.pdf) | Instructor-provided final project instructions. |

## Data source and reproducibility

The dataset is publicly available through the [City of Austin Open Data Portal — Shared Micromobility Vehicle Trips](https://data.austintexas.gov/Transportation-and-Mobility/Shared-Micromobility-Vehicle-Trips/7d8e-dm7r/about_data).

The large raw data file is **not included** in this repository. To reproduce the analysis, download the relevant 2022 data, install the R package `data.table`, and update the **local CSV file path** in `1.Rmd` before running or rendering the document. The uploaded HTML and PDF preserve the original project results.
