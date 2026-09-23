# Water-Quality-and-Risk-Assessment


## Project Overview

This portfolio project examines water-quality conditions across selected sections of the River Thames using monitoring data from the Environment Agency.

The analysis investigates how key water-quality indicators vary over time and between upstream and downstream river sections. The project includes data collection, data cleaning, exploratory analysis, geographical comparison and the development of a transparent water-quality risk-assessment framework.

The purpose of the project is to demonstrate an end-to-end environmental data-analysis workflow, from preparing raw monitoring records to communicating meaningful and reproducible insights.


## Project Questions
The project is designed to answer the following questions:
How has water quality changed across the study period?
Do water-quality conditions differ between upstream and downstream river sections?
Which water-quality parameters show the greatest spatial or temporal variation?
Which locations or periods may require closer monitoring?
Can selected indicators be combined into a transparent water-quality risk score?

## Study Area

The analysis covers four sections of the River Thames:
Wallingford to Caversham: upstream
Reading to Cookham: upper-middle
Cookham to Egham: lower-middle
Egham to Teddington:  downstream

This structure allows water-quality conditions to be compared along the selected upstream-to-downstream pathway.

## Data Source

The project uses publicly available water-quality monitoring data from the Environment Agency's Water Quality Explorer.

The source data include observations collected at monitoring sites along selected sections of the River Thames. Each observation may contain information about the sampling location, sample date, water-quality parameter, measured value and unit of measurement.

**Publisher:** Environment Agency
**Source:** [Water Quality Explorer](https://www.data.gov.uk/dataset/583e771f-1af6-4934-b8f0-28f1d1ddd48c/water-quality-explorer)
**Data accessed:** 31 July 2026
**Geographical coverage:** Selected River Thames monitoring locations between     Wallingford and Teddington
**Analysis period:** 2021–2025
**Sample material:** River or running surface water
**Raw data location:** `data/raw/`
**Processed data location:** `data/processed/`

The original source files are preserved unchanged in the local `data/raw/` directory. The public repository does not include all raw files because of their volume and to avoid unnecessary duplication of the source data.

## Project Objectives

Combine water-quality records from multiple years and river sections.
Preserve the original raw data separately from cleaned and processed data.
Standardise column names, dates, numerical values and location categories.
Identify missing values, duplicates, invalid values and possible outliers.
Analyse changes in selected water-quality indicators over time.
Compare average conditions across the four river sections.
Identify parameters that may contribute to water-quality risk.
Develop a documented and reproducible risk-assessment method.
Present the findings through charts, a dashboard and a concise project report.

## Parameters Analysed
```text
pH
Temperature of Water
Dissolved oxygen, percentage saturation
Orthophosphate, reactive as phosphorus
Ammoniacal nitrogen as N
```

## Analysis Approach

The exploratory analysis compares average annual measurements across the four river sections from 2021 to 2025. Each parameter is analysed separately and only records with matching measurement units are combined.

Annual averages are interpreted alongside sampling coverage because the number and timing of observations differ between river sections and years. The analysis identifies patterns for further investigation and does not represent a formal regulatory water-quality classification.
Further details are provided in the docs/analysis_methodology.md.

## Preliminary Findings

## Preliminary Findings

pH: Annual averages remained relatively stable, with only minor variation between years and river sections.
Dissolved oxygen saturation: Annual averages remained relatively high overall, although Egham to Teddington recorded a temporary reduction in 2023 before recovering.

Detailed findings are documented in docs/findings.md.


## Repository Structure
```text
Water-Quality-and-Risk-Assessment/
├── README.md              # Main project documentation
├── .gitignore             # Files excluded from version control
├── data/
│   ├── raw/               # Original source files, not publicly uploaded
│   └── processed/         # Cleaned and analysis-ready data
├── analysis/              # Excel, SQL or other analytical work
├── docs/                  # Methodology, data dictionary and limitations
├── visuals/               # Exported charts, maps and figures
└── dashboard/             # Dashboard files, screenshots and supporting notes
```

## Documentation

Supporting project documentation

docs/data_dictionary.md
docs/analysis_methodology.md
docs/findings.md

## Data Preparation and Cleaning

The original files were combined into a single analysis-ready dataset covering the four selected River Thames sections and the 2021–2025 analysis period.

The following preparation steps were completed:

- Preserved the original downloaded files separately in `data/raw/`.
- Combined records from different river sections and years.
- Standardised the main column names across the source files.
- Converted date fields into consistent date formats.
- Created `sample_year` to support annual comparisons.
- Retained `parameter_code` as a categorical identifier.
- Checked measurement units across parameters and source files.
- Created a numeric `measurement_value_cleaned` field for analysis.
- Created detection-limit flags to distinguish censored measurements from ordinary numeric values.
- Restricted the main analysis to 2021–2025 because the available 2020 records were incomplete.

The processed dataset retains source-identification, location, sampling, parameter, measurement and unit fields to support traceability.

### Handling Detection-Limit Values

Some source measurements contain qualifiers such as `<` or `>`, rather than ordinary numeric values. These indicate that the reported concentration was below or above a stated detection or reporting limit.

To preserve this information:

- The original reported value was retained in `measurement_value`.
- A numeric analysis value was stored in `measurement_value_cleaned`.
- `below_detection_limit` identifies values reported below a stated limit.
- `above_detection_limit` identifies values reported above a stated limit.

Detection-limit records were therefore not treated automatically as missing values. They were retained with separate flags so that their treatment remains visible during analysis.

### Data Quality Review

Before interpreting water-quality trends, the combined dataset was reviewed for:

Missing values
Duplicate observations
Invalid or inconsistent dates
Non-numeric measurement values
Below-detection and above-detection measurements
Inconsistent units for the same parameter
Unexpected or potentially extreme values
Uneven coverage between river sections and years
Differences in parameter availability and sampling frequency

Potentially extreme measurements were not assumed to be errors automatically. Unusual records require investigation because they may represent either data-quality issues or genuine environmental events.


## Data Attribution
Source: Environment Agency, Water Quality Explorer, accessed 31 July 2026.

© Environment Agency copyright and/or database right 2025. Used under the Open Government Licence.

### Source Data Considerations

The Water Quality Explorer is a continuously maintained source, so records may be updated or corrected after the project data are downloaded. Sampling frequency and parameter availability may also differ between monitoring locations and years.

For reproducibility, this project records the data-access date and preserves the downloaded raw files unchanged. The analysis reflects the version of the source data available when the project files were collected.