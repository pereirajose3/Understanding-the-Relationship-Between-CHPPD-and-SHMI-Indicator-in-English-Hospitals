# Understanding-the-Relationship-Between-CHPPD-and-SHMI-Indicator-in-English-Hospitals

This repository contains the analysis code used for the paper:

**Pereira J, Eusébio C, Sherlaw-Johnson C, Black S, Punshon G, Hardy S, Leary A (2025)**  
*Understanding the relationship between care hours per patient day and summary hospital-level mortality indicator in English hospitals: A time series approach*  
Journal of Patient Safety and Risk Management.  
Paper link: https://journals.sagepub.com/doi/full/10.1177/25160435251410480

## Overview
The code in this repository reproduces the key steps described in the manuscript, including:

- Extracting, cleaning, and consolidating **monthly CHPPD** files (trust level) from NHS England / NHS Digital outputs  
- Merging CHPPD with **SHMI (12-month rolling)** data by trust code and date  
- Feature engineering (e.g., mean-centering time series)  
- **Cross-correlation analysis** (lead–lag relationships) between CHPPD and SHMI at the trust level  
- Stratified summaries/plots by SHMI cohorts (above / within / below control limits)

> Note: SHMI is published as a 12-month rolling value; the analysis therefore focuses on **negative lags (0 to −18 months)** to interpret staffing leading mortality, consistent with the paper.

## Data sources
This study uses **publicly available** datasets:
- CHPPD (Care Hours Per Patient Day) – NHS England guidance/datasets  
- SHMI (Summary Hospital-level Mortality Indicator) – NHS England / NHS Digital publication

This repository does **not** include raw data files by default (depending on your choice).  
If you want full reproducibility, you can either:
1) download the datasets manually (recommended for transparency), or  
2) add a data-download script if your repo supports it.



