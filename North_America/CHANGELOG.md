
# CHANGELOG

This file contains the version history of the model.

## [v2026.0.0](https://github.com/gem/global_exposure_model/North_America/-/releases/v2026.0.0)

> This release is a major update affecting all country models. It introduces breaking schema changes (renamed columns, restructured folders), revised cost figures, improved spatial resolution, and new embodied carbon data.

### ⚠️ Breaking Changes

- **Folder structure and file names have been reorganised.** Paths to exposure files have changed — update any hardcoded references in your scripts.
- **Column headers have been renamed.** Cost columns are now split into `BLDG_REPL_COST_USD`, `COST_CONTENTS_USD`, and `TOTAL_REPL_COST_USD `. Changes in the replacement cost columns:
  - The columns `COST_STRUCTURAL_USD` and `COST_NONSTRUCTURAL_USD` have been replaced by `BLDG_REPL_COST_USD`, which lists the combined replacement cost for the structural and nonstructural components of the building(s).
  - `TOTAL_REPL_COST_USD` is the sum of `BLDG_REPL_COST_USD` and `COST_CONTENTS_USD`.
- **Administrative unit fields updated.** `ID_1` and `NAME_1` values have been revised to follow GEM standards and may differ from previous versions.

### Updates

- All models now follow [GEM Taxonomy v4.0](https://github.com/gem/gem_taxonomy/tree/v4.0) and vulnerability mapping has been updated accordingly.
- Building counts and population updated to 2025 figures using R2025A GHS layers and 2025 WorldPop.
- Building replacement cost values have been updated to 2024–2025 values
- The contents costs, which are estimated as a fraction of the building replacement cost, have been revised.
- Revised occupant distribution methodology across time periods (`day`, `night`, `transit`).
- Improved spatial disaggregation at 1 km resolution.
- Added embodied carbon values (`CARBON_BUILDINGS_TON`).

### Country-specific model updates

- `Canada`: Re-implementation of the NRCan 2016 model (2023 version included updates in counts and costs using over simplified methodology). This implementation includes counts and population updates following 2025 methodology.
- `United States`: HAZUS v6.1 model shared by the USGS. The model includes building and housing counts for 2020. Costs and population updated to 2025 figures by the USGS. The number of households and occupants at different times of the day are included in the shared model.
- `Mexico`: The commercial, industrial, and residential exposure models were updated using data from the 2024 Economic Census and the 2020 Population and Housing Census, with national projections to 2025. The updates include:
    - Integration of building heights derived from the new generation of raster data from the Global Human Settlement Layer (GHSL, 2025) to improve structural classification.
    - Use of GHSL Earth observation datasets to estimate construction years, enabling improved linkage to building code levels.
    - Enhanced methodology for occupant distribution.
    - Revised building costs to reflect updated national estimates, along with updated average construction areas and revisions based on building footprint statistics.
    - Updated administrative boundaries according to the 2025 INEGI revision.
    - Non-residential (commercial and industrial) inventories now incorporate enterprise size information to refine area estimates and include improved activity mapping.
    - The residential model includes updated mapping schemes, wall material classifications, and satellite-derived building height and construction year data to assign structural classes consistent with observed distributions. Model resolution increased from AGEB to locality level.

## [v2025.0.0](https://github.com/gem/global_exposure_model/North_America/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).
The USA and CAN models in v2023.1.0 were using the HAZUS taxonomy. This version uses the equivalent GEM Taxonomy v3.3 strings.

## [v2023.1.0](https://github.com/gem/global_exposure_model/North_America/-/releases/v2023.1.0)

Major update for USA and CAN. USA is based on the USACE/NSI exposure model, with some modifications. CAN is based on the NRCan exposure model, with some modifications. MEX taxonomy map was revised to denote roof weights on adobe structures, references to the new WBB and INF vulnerability classes, and to increase the amount of MCF.

## [v2023.0.0](https://github.com/gem/global_exposure_model/North_America/-/releases/v2023.0.0)

Minor revision relative to `v2022.0.0`. Population distributed across day, night, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/North_America/-/releases/v2022.0.0)

- CAN: 2018 exposure replaced by the new NRCan exposure model used in the Canadian National Earthquake Risk Model, costs coverted from CAD (used in the original model) to USD. The newly added taxonomy mapping file maps the HAZUS taxonomy strings used in the exposure to GEM vulnerability functions.
- MEX: Res numbers consider 2020 Census. Non-res numbers consider DENUE 2021. New boundary files to consider the AGEBs from 2020 Census. Costs updated considering cost databases and inflation. Non-res numbers reduced in 10% to discount possible mix building types. New taxonomy mapping for Mexico considering vulnerabilities with code level and ductility.
- USA: Construction cost update from 2014 values to 2021 values. At national level, there's effectively a 40% increase in residential construction costs and 30% increase in non-residential construction costs compared to the previous exposure model which was using 2014 unit replacement costs. The newly added taxonomy mapping file maps the HAZUS taxonomy strings used in the exposure to GEM vulnerability functions.

## [v2018.0.0](https://github.com/gem/global_exposure_model/North_America/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.

