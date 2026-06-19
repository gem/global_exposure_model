
# CHANGELOG

This file contains the version history of the model.

## [v2026.0.0](https://github.com/gem/global_exposure_model/Middle_East/-/releases/v2026.0.0)

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

- **Syria**: Exposure model update was conducted in January 2026 to align the repo to the latest format. For all occupancies, new data on the year of construction and heights were extracted from global datasets, updates on replacement costs and area, new documentation on building code.

## [v2025.0.0](https://github.com/gem/global_exposure_model/Middle_East/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

- **Syria**: Exposure model updates in the context of the World Food Program (WFP) 2024 project. The residential model was built starting from adm3 data (instead of adm1). For all occupancies, new information on the year of construction and heights was taken from global datasets, improvements in disaggregation methodology, and updates on replacement costs. See additional details in [merge_requests!8](https://github.com/gem/global_exposure_model/Middle_East/-/merge_requests/8).

## [v2023.1.0](https://github.com/gem/global_exposure_model/Middle_East/-/releases/v2023.1.0)

Aggregated versions of the exposure models included. In Iran, the amount of residential buildings with low ductility was slightly increased (approximately 5% nationwide). In both Iran and Armenia, more high collapse volume buildings were added.

## [v2023.0.0](https://github.com/gem/global_exposure_model/Middle_East/-/releases/v2023.0.0)

Full revision of Palestine exposure model. Moderate revision to the Armenia, Azerbaijan, and Georgia models to reflect newly available or updated datasets. Population for Israel corrected. Population across all models distributed for day, night, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/Middle_East/-/releases/v2022.0.0)

A major revision of the non-residential exposure for all countries and for residential of Azerbaijan, Armenia, Georgia, Israel, Iraq, and Iran. A minor revision across all countries to update population, building counts, and replacement values.

## [v2018.0.0](https://github.com/gem/global_exposure_model/Middle_East/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.