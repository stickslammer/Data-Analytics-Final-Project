# Data Sources

This document records the datasets used in the Monterey County Housing Market Analysis. Sources, access dates, geographic coverage, time periods, and other relevant information are documented to support reproducibility and data provenance.

## Primary Housing Dataset

### Median Prices of Existing Single-Family Detached Homes

**Provider:** California Association of REALTORS® (C.A.R.)

**Source Type:** Historical housing market data

**Geographic Coverage:** California statewide and county-level housing data

**Primary Geography Used in Analysis:** Monterey County, California

**Available Historical Coverage:** Approximately 1990–2026

**Project Analysis Period:** January 2015 through December 2025

**Frequency:** Monthly

**Housing Type:** Existing single-family detached homes

**Metric:** Median home sale price

**Raw File Location:** `data/raw/`

**Raw File:** `Raw_Median Prices Existing 1 Family Homes.csv`

**Purpose:** This dataset will serve as the primary source for analyzing changes in Monterey County median home prices between 2015 and 2025.

## Initial Data Structure

The source dataset contains historical housing prices for California and individual California counties.

The dataset is structured in wide format:

* Each row represents a month.
* Geographic areas are represented by columns.
* The `Monterey` column represents Monterey County.
* Values are reported as median home prices in U.S. dollars.
* The raw dataset contains observations outside the project's 2015–2025 analysis period.

The complete source dataset is being retained in the `data/raw/` directory. A separate cleaned dataset will be created for analysis so the original source data remains unchanged.

## Planned Processing

The primary housing dataset will be processed to:

1. Isolate Monterey County.
2. Restrict observations to January 2015 through December 2025.
3. Verify that all expected monthly observations are present.
4. Identify missing or invalid values.
5. Verify date and price data types.
6. Check for duplicate observations.
7. Standardize column names.
8. Create a cleaned analysis-ready dataset.

All transformations will be documented separately in the project's data-cleaning log.

## Supporting Datasets

Additional datasets will be added to investigate economic and demographic factors associated with changes in Monterey County housing prices.

Planned supporting data includes:

* 30-year fixed mortgage interest rates
* Consumer Price Index (CPI)
* Monterey County unemployment rate
* Population estimates
* Housing inventory and market activity data
* Supplemental housing data for validation where appropriate

Each dataset will be documented here when it is acquired.

## Data Limitations

Potential limitations include differences in reporting methodology over time, missing observations, revisions to historical housing statistics, and differences between county-level and more localized housing markets.

Relationships identified between housing prices and economic variables will be treated as associations unless sufficient evidence exists to support causal conclusions.
