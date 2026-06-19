
# CHANGELOG

This file contains the version history of the model.

## [v2026.0.0](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/releases/v2026.0.0)

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

- `Dominican Republic` residential model updated with latest census data and improved methodologies for exposure development, such as the incorporation of GHSL for heights and year of construction.
- `Guatemala` residential model updated with latest census data and improved methodologies for exposure development, such as the incorporation of GHSL for heights and year of construction.
- `Panama`residential model updated with latest census data and improved methodologies for exposure development, such as the incorporation of GHSL for heights and year of construction.
- `US oversea territories` (Puerto Rico and US Virgin Islands): HAZUS v6.1 model shared by the USGS. The model includes building and housing counts for 2020. Costs and population updated to 2025 figures by the USGS. The number of households and occupants at different times of the day are included in the shared model.

## [v2025.0.0](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

- `El Salvador`: exposure model updates in the context of the FORCE project. New aggregated and disaggregated exposure models developed in collaboration with MARN that include building counts, costs and areas for RES, IND and COM models. In 2024, the political and territorial organization of El Salvador changed, dissolving what was known before as `Municipios` into larger administrative regions, and subdividing them into what is today called `Distritos`. See additional details in [merge_requests!10](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/merge_requests/10).
- `Haiti`: exposure model updates in the context of the World Food Program (WFP) 2024 project. The updates include information from the new generation of raster GHSL - Global Human Settlement Layer (2025), and population projections from the Institut Haïtien de Statistique et d'Informatique (2024). The IND and COM models were updated based on Economic activity indicators, Labour force indicators (2024) and enterprise surveys data from the World Bank Group (2019). See additional details in [merge_requests!11](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/merge_requests/11).

## [v2023.1.0](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/releases/v2023.1.0)

Spatial disaggregation of exposure for most countries. Individual taxonomy mapping files provided for each Central American country, differentiating roof weight on adobe structures relative to the Caribbean countries. More low ductility and high collapse volume classes assigned to HTI in the taxonomy map. The taxonomy maps were also adjusted to incorporate the new WBB and INF vulnerability classes. Some tags for `ID_1` fixed for CYM and TCA.

## [v2023.0.0](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/releases/v2023.0.0)

Minor update to `v2022.0.0`. Occupants, dwellings, and buildings were brought from the previous vintage to a target year of 2020/1: BLZ, CRI, DOM, SLV, HTI, HND, JAM, NIC, PAM, LCA, TTO. Population was distributed to night, day, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/releases/v2022.0.0)

This version updates the 2018 replacement costs for all countries in the region. In addition, there are major changes in the non-residential models for the following countries: DOM, CUB, GTM, NIC, CRI, PAN, HND, JAM. The main changes include a revision in the amount and geographical distribution of the establishments, a revision of average area size, number of stories, replacement cost, code and expected ductility of the establishments, and an additional tag describing the economic purpose or use of the establishments.

## [v2018.0.0](https://github.com/gem/global_exposure_model/Caribbean_Central_America/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.


