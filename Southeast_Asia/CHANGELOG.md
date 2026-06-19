
# CHANGELOG

This file contains the version history of the model.

## [v2026.0.0](https://github.com/gem/global_exposure_model/Southeast_Asia/-/releases/v2026.0.0)

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

## [v2025.0.0](https://github.com/gem/global_exposure_model/Southeast_Asia/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

Country model updates:

- **Philippines**: Exposure model updates in the context of the World Food Program (WFP) 2024 project. The model incorporates detailed correlated variables for the latest 2020 census of population and housing (+7 attributes). The non-residential models were updated using the 2023 enterprises survey. See additional details in [merge_requests!9](https://github.com/gem/global_exposure_model/Southeast_Asia/-/merge_requests/9).

## [v2023.1.0](https://github.com/gem/global_exposure_model/Southeast_Asia/-/releases/v2023.1.0)

Aggregated and disaggregated exposure files added. Minor adjustment to ensure consistent boundary names for Myanmar. The taxonomy maps for IDN, PHL, MMR, and TLS were updated to consider new WBB and INF vulnerability classes.

## [v2023.0.0](https://github.com/gem/global_exposure_model/Southeast_Asia/-/releases/v2023.0.0)

Minor revision relative to `v2022.0.0`. Population, dwellings, and buildings brought to 2020 for Myanmar and the Philippines. Population distributed across day, night, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/Southeast_Asia/-/releases/v2022.0.0)

Improved non-residential data and more detailed mapping schemes. Singapore and Myanmar exposure models included extensive review of building and construction practice. Singapore includes a building by building model.

## [v2018.0.0](https://github.com/gem/global_exposure_model/Southeast_Asia/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.