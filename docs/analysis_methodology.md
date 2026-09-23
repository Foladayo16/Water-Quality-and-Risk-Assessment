# Exploratory Analysis Methodology

## Purpose

The exploratory analysis evaluates how selected water-quality indicators vary between 2021 and 2025 and across four River Thames sections.

The analysis focuses on:

- Changes over time
- Differences between river sections
- Potential upstream-to-downstream patterns
- Unusual annual or geographical results
- Indicators that may require further risk assessment

## Indicators Analysed

The current analysis includes:

- pH
- Temperature of water
- Dissolved oxygen, percentage saturation
- Orthophosphate, reactive as phosphorus
- Ammoniacal nitrogen as N

Each indicator is analysed separately because the parameters use different units and have different environmental interpretations.

## Analysis Grouping

The processed observations are grouped by:

- `sample_year`
- `river_stretch`
- `river_section`
- `parameter_name`
- `unit`

Grouping by parameter and unit prevents measurements representing different environmental properties from being combined incorrectly.

## Summary Measure

The arithmetic mean is used to summarise the available measurements for each parameter, year and river stretch.

The annual mean is calculated as:

`Sum of available cleaned measurements ÷ Number of available cleaned measurements`

The results are used for exploratory comparison rather than formal regulatory classification.

## Comparison Approach

For each selected indicator:

1. Filter the processed dataset to the required `parameter_name`.
2. Confirm that the measurement `unit` is consistent.
3. Group observations by `sample_year` and `river_stretch`.
4. Calculate the average of `measurement_value_cleaned`.
5. Compare annual results across the four river stretches.
6. Review changes over time within each river stretch.
7. Record notable patterns, limitations and possible areas for further investigation.

## Interpretation Cautions

Annual averages can summarise broad patterns, but they may conceal seasonal variation, isolated high or low measurements and differences in sampling frequency.

Averages based on different numbers of observations are not equally representative. Results must therefore be considered alongside data coverage, missing months and parameter availability.

Observed differences describe patterns in the available monitoring data. They do not establish that location or time caused the changes.