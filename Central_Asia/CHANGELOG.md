# Changelog

This file contains the version history of the model.


## [v2026.0.0](https://github.com/gem/global_exposure_model/Central_Asia/-/releases/v2026.0.0)

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

- `Kyrgyztan` and `Tajikistan`: Model updates for for all occupancies as part of the CAREC-II project. Includes new base data and improved methodologies from the Exposure Factory, such us GHSL layers for year of construction, heihgts, etc.

## [v2025.0.0](https://github.com/gem/global_exposure_model/Central_Asia/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

## [v2023.1.0](https://github.com/gem/global_exposure_model/Central_Asia/-/releases/v2023.1.0)

Minor update relative to `v2023.0.0`. Aggregated and disaggregated exposure now included. Light roofs are additionally considered for 25% of adobe block buildings.

## [v2023.0.0](https://github.com/gem/global_exposure_model/Central_Asia/-/releases/v2023.0.0)

Minor update relative to `v2022.0.0`. Population distributed to night, day, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/Central_Asia/-/releases/v2022.0.0)

Major update to all the exposure models, using the latest national databases available, global datasets and information from neighbouring countries. Added exposure models for non-residential occupancies for TKM. Exposure is derived at the subnational level, but further disaggregated to a 0.04deg resolution using WorldPop population estimates.

## [v2018.0.0](https://github.com/gem/global_exposure_model/Central_Asia/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.

