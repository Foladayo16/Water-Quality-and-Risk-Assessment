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

## Data Quality Checks

## Data Attribution
Source: Environment Agency, Water Quality Explorer, accessed 31 July 2026.

© Environment Agency copyright and/or database right 2025. Used under the Open Government Licence.

### Source Data Considerations

The Water Quality Explorer is a continuously maintained source, so records may be updated or corrected after the project data are downloaded. Sampling frequency and parameter availability may also differ between monitoring locations and years.

For reproducibility, this project records the data-access date and preserves the downloaded raw files unchanged. The analysis reflects the version of the source data available when the project files were collected.