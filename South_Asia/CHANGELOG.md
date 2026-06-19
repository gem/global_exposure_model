
# CHANGELOG

This file contains the version history of the model.

## [v2026.0.0](https://github.com/gem/global_exposure_model/South_Asia/-/releases/v2026.0.0)

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

- **Afghanistan**: Exposure model update was conducted in December 2025 to align the repo to the latest format. For all occupancies, new data on the year of construction and heights were extracted from global datasets, updates on replacement costs and area, new boundaries.
- **Pakistan**: Exposure model update was conducted in December 2025, to align the modelling to the latest improvements in the Exposure Factory (e.g. GEM Taxonomy v4.0) and resolve some bugs (eg. adding missing attributes in exposure files; removing one duplicate Adm3 division). New data from the 2023 census reports about number of stories of buildings and households outer walls material and year of constructions have been included.

## [v2025.0.0](https://github.com/gem/global_exposure_model/South_Asia/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

Model updates also include:

- **Bangladesh**: Through the 2023-2024 UNDRR project for Bangladesh, the residential exposure model was updated considering the 2022 Population and Housing Census of Bangladesh at Adm 7 (Enumeration Area level). Wall material information is available at Adm 3, and building height information is included from World Settlement Footprint (WSF) 3D. See additional details in [merge_requests!14](https://github.com/gem/global_exposure_model/South_Asia/-/merge_requests/14).
- **Bhutan and Nepal**: Nepal and Bhutan models were updated within the context of the FORCE project. The updates include revisions to residential, commercial, and industrial exposure models, leveraging the latest data sources available for both countries. In the case of Nepal, the latest 2021 census was used. For all occupancies, new information on the year of construction and heights was taken from global datasets, improvements in disaggregation methodology, and updates on replacement costs. See additional details in [merge_requests!16](https://github.com/gem/global_exposure_model/South_Asia/-/merge_requests/16).
- **Pakistan**: Exposure model updates in the context of the World Food Program (WFP) 2024 project. The residential model was built starting from adm3 data (instead of adm1) and building attributes and counts use the latest 2023 census. For all occupancies, new information on the year of construction and heights was taken from global datasets, improvements in disaggregation methodology, and updates on replacement costs. See additional details in [merge_requests!18](https://github.com/gem/global_exposure_model/South_Asia/-/merge_requests/18). 
- **Afghanistan**: Exposure model updates in the context of the World Food Program (WFP) 2024 project. The residential model was built starting from adm2 data (instead of adm1). For all occupancies, new information on the year of construction and heights was taken from global datasets, improvements in disaggregation methodology, and updates on replacement costs. See additional details in [merge_requests!17](https://github.com/gem/global_exposure_model/South_Asia/-/merge_requests/17). 

## [v2023.1.0](https://github.com/gem/global_exposure_model/South_Asia/-/releases/v2023.1.0)

Aggregated and disaggregated exposure files added. Roof weights for adobe structures are updated for AFG, BGD, IND, and PAK. Both IND and BGD use light-weight roofs (RWO) for 100% of adobe buildings, AFG and PAK for 80%. Additionally, new vulnerability classes for WBB and INF were incorporated into the taxonomy maps for BGD, IND, NPL, and PAK. New high collapse volume loss variants VL100 were also considered in the taxonomy map for NPL.

## [v2023.0.0](https://github.com/gem/global_exposure_model/South_Asia/-/releases/v2023.0.0)

Minor revision relative to the `v2022.0.0` release. Populations, dwellings, and buildings updated to reflect 2021/2 values for BGD, BTN, and NPL. Population distributed across day, night, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/South_Asia/-/releases/v2022.0.0)

Pakistan and Afghanistan have both had a major revision to update building counts, population, replacement values, and mapping schemes. Residential exposure for India is now at the fifth administrative level. Non-residential exposure for all countries has been substantially revised, particularly addressing cases where a large fraction of the commercial and industrial activity occurs outside of dedicated commercial or industrial buildings (eg. street businesses, home manufacturing, etc.), and these have been appropriately excluded from the non-residential exposure.

## [v2018.0.0](https://github.com/gem/global_exposure_model/South_Asia/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.