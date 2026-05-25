# GHG Emissions Analysis — EDGAR Dataset

A data analysis and visualization project built on the EDGAR 2024 GHG emissions dataset. 
The [EDGAR.ipynb](https://github.com/leonardoy99/EDGAR/blob/main/EDGAR.ipynb) notebook reproduces three charts summarizing global greenhouse gas emission trends from 1970 to 2023.

## Repository structure

- `EDGAR.ipynb` — main notebook with data processing and visualizations
- `data/` — raw input datasets in xlsx format
- `Report_YANG.pdf` — results and methodology writeup

## Overview

The analysis draws from the `GHG_totals_by_country` sheet of the EDGAR 2024 GHG Booklet, 
which reports national and aggregate emissions in megatonnes of CO₂ equivalent per year 
(Mt CO₂eq/yr). All data processing, transformation, and visualization were carried out in 
Python using `pandas`, `numpy`, `matplotlib`, and `seaborn`.

## Charts

**Chart 1 – GHG Emission Growth in the Euro Area, EU27, and Globally (baseline: 1970)**  
A line chart tracking cumulative emission growth relative to 1970. Euro Area emissions were 
derived by subtracting non-Euro Area EU member states from the EU27 aggregate.

**Chart 2 – GHG Emissions per Capita by World Bank Income Group**  
A stacked area chart comparing per capita emission trends across income groups. Country-to-group 
mappings and population data were sourced from the World Bank. Per capita values were computed 
using group-level totals rather than averaging individual country figures, to correctly weight 
for country size.

**Chart 3 – Continental and Country-Level Contributions to Global Emissions**  
A dual-panel visualization combining a stacked area chart (continental shares) and a line chart 
(selected major emitters per continent). Country-to-continent mapping was handled via the 
`pycountry` library.
For more details on the methodologies, see the [report](https://github.com/leonardoy99/EDGAR/blob/main/Report_YANG.pdf).



## Key Findings

- Global GHG emissions rose ~120% between 1970 and 2023, while the EU27 and Euro Area 
  reduced emissions by 30% and 27% respectively over the same period.
- Asia's share of global emissions grew from 26% in 1970 to over 58% by 2023, driven 
  largely by China's industrialization.
- High-income countries remain the highest per capita emitters, though their levels have 
  declined since the early 2000s. Upper-middle-income countries nearly doubled their per 
  capita emissions over the same period.


## Data Source

[EDGAR GHG Emissions Database](https://edgar.jrc.ec.europa.eu/) — European Commission, 
Joint Research Centre (JRC), 2024 release.
