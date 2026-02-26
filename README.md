# District-Level WASH Vulnerability Typology (Bangladesh, MICS 2019)

This repository contains a single R Markdown workflow (`analysis.Rmd`) that produces a **district-level WASH vulnerability typology** for Bangladesh using **MICS 2019**. The analysis constructs district indicators for water, sanitation, hygiene, and a combined WASH measure, then applies and compares clustering approaches (including fuzzy clustering) and robustness checks.

## Repository contents
- `analysis.Rmd` — complete end-to-end analysis (data → indicators → district aggregation → clustering → agreement measures → plots/maps)
- `analysis.pdf` — knitted output / analysis report (generated from the Rmd)
- `Final_project_report.pdf` — final written project report (PDF)

## Data (not included)
This project uses Bangladesh MICS 2019 microdata, which may be restricted.  
You must obtain the data separately and place it where `analysis.Rmd` expects it (or edit the file paths inside the Rmd).

Typical MICS module files used in this workflow (examples):
- Household (`hh.sav`)
- Household listing (`hl.sav`)
- Women (`wm.sav`)
- Children (`ch.sav`)
- (Optional) Field staff / facilities module if applicable (`fs.sav`)

> If your file names differ, just update the paths inside `analysis.Rmd`.

## Spatial files for maps (if you run mapping)
If your Rmd produces maps, you will also need district boundary and name-matching resources (not always shareable).  
Place them in the repo (e.g., `data/` or `shapefiles/`) and update paths in `analysis.Rmd` as needed.

## Requirements
- R (and RStudio recommended)
- Common packages for this workflow may include: `rmarkdown`, `knitr`, `haven`, `dplyr`, `tidyr`, `ggplot2`, `cluster`, `factoextra`, `e1071`, and mapping packages such as `sf`/`readxl` (depending on your enabled sections).

## How to run
### Option A: Knit in RStudio (recommended)
1. Open `analysis.Rmd` in RStudio
2. Set the working directory to the repository folder
3. Click **Knit**

### Option B: Render from R

## Citation
If you use this repository, please cite the associated project report:

> Doha, J. A. (2026). *District-Level WASH Vulnerability Typology in Bangladesh Using MICS 2019: A Comparative Clustering Analysis.* ISRT, University of Dhaka.
```r
rmarkdown::render("analysis.Rmd")
