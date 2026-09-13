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
pH
Temperature of Water
Dissolved oxygen, percentage saturation
Orthophosphate, reactive as phosphorus
Ammoniacal nitrogen as N

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

## Current Progress

- [ ] Organise raw datasets
- [ ] Add `Source_Year`
- [ ] Merge yearly datasets
- [ ] Complete data-quality assessment
- [ ] Clean the data
- [ ] Conduct risk assessment
- [ ] Create charts
- [ ] Document conclusions