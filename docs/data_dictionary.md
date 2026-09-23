# Data Dictionary

## Purpose

This data dictionary describes the main fields used in the processed River Thames water-quality dataset.

The processed dataset combines monitoring observations from four river sections between 2021 and 2025. It retains source, location, sampling, parameter, measurement and data-quality fields to support traceability and reproducibility.

## Dataset Grain

Each row represents one reported water-quality observation for a particular parameter, sampling location and sampling date.

A single sampling event may therefore appear across multiple rows because several water-quality parameters can be measured during the same event.

## Field Definitions

| Field | Description |
|---|---|
| `observation_url` | Unique source-system URL identifying the individual observation. |
| `site_id` | Unique code identifying the monitoring or sampling location. |
| `site_name` | Human-readable name of the sampling location. |
| `longitude` | East-to-west coordinate of the sampling point in decimal degrees. |
| `latitude` | North-to-south coordinate of the sampling point in decimal degrees. |
| `region` | Broad Environment Agency region associated with the monitoring location. |
| `monitoring_area` | Operational monitoring area within the Environment Agency region. |
| `monitoring_subarea` | Smaller operational area within the monitoring area. |
| `river_stretch` | Named River Thames stretch used to group the source records geographically. |
| `river_section` | Analytical position of the river stretch: upstream, upper-middle, lower-middle or downstream. |
| `sampling_point_status` | Status of the monitoring point recorded in the source data. |
| `sampling_point_type` | Type of sampling site or water source. |
| `sample_datetime` | Date and time associated with the sampling observation. |
| `sample_date` | Calendar date extracted or standardised from the sampling datetime. |
| `sample_year` | Year extracted from the sampling date for annual analysis. |
| `sampling_purpose` | Source description of why the sample was collected. |
| `sample_material_type` | Type of material sampled, such as river or running surface water. |
| `parameter_code` | Source-system code identifying the measured substance, property or test. |
| `parameter_name` | Name of the water-quality parameter measured. |
| `measurement_value` | Original result as reported in the source data, including any detection-limit qualifier. |
| `measurement_value_cleaned` | Numeric value prepared for calculations and analytical comparisons. |
| `below_detection_limit` | Indicator showing whether the original result was reported below a stated detection or reporting limit. |
| `above_detection_limit` | Indicator showing whether the original result was reported above a stated detection or reporting limit. |
| `unit` | Measurement unit associated with the reported parameter. |
| `data_type` | Classification used to distinguish numeric and other result formats. 

## River-Section Classification

The four study stretches are classified according to their relative position along the selected River Thames study area.

| River stretch | Analytical classification |
|---|---|
| Wallingford to Caversham | Upstream |
| Reading to Cookham | Upper-middle |
| Cookham to Egham | Lower-middle |
| Egham to Teddington | Downstream |

These categories support geographical comparison within the defined study area. They should not be interpreted as classifications of the entire River Thames.

## Measurement Interpretation

Water-quality parameters must be interpreted together with their corresponding units. Measurements from different parameters should not be compared directly simply because they contain similar numerical values.

For example, a result for ammoniacal nitrogen does not represent the same environmental measurement as a result for biochemical oxygen demand, even if both results use milligrams per litre.

Values beginning with `<` indicate that the result was reported below a stated detection or reporting limit. Values beginning with `>` indicate that the result was reported above a stated limit. These qualified values are retained in the original measurement field and identified using separate detection-limit flags.

## Coverage Notes

Sampling coverage is not uniform across all river sections, years and months. Some combinations contain substantially more observations than others, while some months have no available records.

The analysis uses the observations available for each comparison. Missing months were not filled with estimated values because doing so could introduce artificial patterns.

Differences between annual or geographical averages should therefore be interpreted alongside observation counts, parameter availability and sampling frequency.