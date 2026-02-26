# District-Level WASH Vulnerability Typology in Bangladesh (MICS 2019)

This repository contains the materials for the undergraduate project report:

**District-Level WASH Vulnerability Typology in Bangladesh Using MICS 2019: A Comparative Clustering Analysis**  
**Author:** Jokhrof Ahmed Doha (ISRT, University of Dhaka)  
**Supervision:** Nasrin Lipi, Assistant Professor, ISRT  
**Date:** March 2026

## Project summary
This study develops a **district-level WASH vulnerability typology** for Bangladesh using **MICS 2019** and compares **hard vs. fuzzy clustering** approaches to classify districts into vulnerability groups. The workflow constructs district profiles for **drinking water, sanitation, hygiene, and combined WASH**, then applies clustering and agreement checks to evaluate robustness and identify transitional (borderline) districts.

## Data
- **Source:** Bangladesh Multiple Indicator Cluster Survey (MICS) 2019 (nationally representative household survey).
- **Unit of analysis:** District (64 districts).
- **Weights:** Household sampling weights are applied to produce district-level weighted percentages.

> **Note:** If you cannot share the raw microdata publicly, keep data out of the repo and document how to obtain it.

## Indicators (district-level)
The analysis uses four outcome indicators:
1. Improved drinking-water service  
2. Improved sanitation service  
3. Basic handwashing service  
4. Combined WASH service (meets water + sanitation + hygiene simultaneously)

## Methods (high-level)
- **Preprocessing**
  - Construct household service-status indicators aligned to JMP/SDG service ladder concepts.
  - Aggregate to district-level **weighted percentages**.
  - Standardize indicators using **z-scores** before clustering.

- **Clustering approaches**
  - **Ward’s hierarchical clustering (Ward.D2)**
  - **K-means**
  - **Fuzzy c-means (FCM)** for soft membership and identifying borderline districts

- **Choosing number of clusters**
  - **Gap statistic** with the **1-SE rule** (tested for both K-means and FCM)

- **Robustness / agreement**
  - **Adjusted Rand Index (ARI)**
  - **Normalized Mutual Information (NMI)**

- **Mapping**
  - District maps showing vulnerability groups and, for FCM, membership strength and ambiguity/transitional districts.

