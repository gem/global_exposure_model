
# CHANGELOG

This file contains the version history of the model.


## [v2026.0.0](https://github.com/gem/global_exposure_model/Africa/-/releases/v2026.0.0)

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

## [v2025.0.0](https://github.com/gem/global_exposure_model/Africa/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).  
In sub-Saharan Africa, adjustments on masonry construction to account for lightweight roofs (previously, the lightweight roof (RWO) vulnerability class variants were only available for MUR+ADO). This change should result in the lowering of the fatality estimates. See additional details in [merge_requests!7](https://github.com/gem/global_exposure_model/Africa/-/merge_requests/7).


## [v2023.1.0](https://github.com/gem/global_exposure_model/Africa/-/releases/v2023.1.0)

Aggregated exposure files were added. The disaggregation process is slightly different to conform to the GRM standard. Taxonomy maps for North African countries were differentiated to allow Sub-Saharan countries to explicitly note lightweight roofs for adobe block structures. The taxonomy map for Sub-Saharan Africa also now references new WBB and INF vulnerability classes.


## [v2023.0.0](https://github.com/gem/global_exposure_model/Africa/-/releases/v2023.0.0)

Minor update relative to `v2022.0.0`. Population distributed across day, night, and transit time periods. Additional updates include a minor revision to the mapping schemes in Cairo, Egypt.


## [v2022.0.0](https://github.com/gem/global_exposure_model/Africa/-/releases/v2022.0.0)

Revision of the Africa Exposure model using a consistent approach across the entire continent, using latest available national and global databases. Exposure is derived at the subnational level, but further disaggregated to a 0.04deg resolution using WorldPop population estimates. Updates relative to the Paul et. al. (2022) paper are: inclusion of census data for Eswatini, revision of cost disaggregation (i.e., into structural, nonstructural, and contents) to match GRM standards, and revision of assumptions for non-residential buildings counts (particularly for Egypt, Equatorial Guinea, Ghana, and Namibia).


## [v2018.0.0](https://github.com/gem/global_exposure_model/Africa/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.
