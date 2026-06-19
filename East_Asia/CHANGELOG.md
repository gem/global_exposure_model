# CHANGELOG

This file contains the version history of the model.

## [v2026.00](https://github.com/gem/global_exposure_model/East_Asia/-/releases/v2026.0.0)

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

- `Japan`: The residential, commercial and industrial exposure models for Japan were updated using the latest datasets available. The Population and Households Census of Japan 2020 and 2023 Housing and Land Survey were used for the residential models. The 2008 survey on corporations and the 2008-2024 'building starts' annual statistics were included in the nonresidential models. In addition, reference construction costs by material and Prefecture from the National Tax Agency for 2025 were used to estimate the total replacement cost. Wooden building classes reflect now the evolution of timber construction, from traditional (and still common) heavy timber post-and-beam frames to the light timber North-American-style wall framing systems. The vulnerability mapping uses classes W+WLI/LWAL and W+WHE/LPB, in place of the W/LFM classes. 
- `Taiwan`: The residential exposure model was updated using the official 2020 Population and Housing Census of Taiwan, and Household registration statistics data in 2022. The model now directly incorporates from the census the number of housing units, construction material, constructed floor space, construction period, number of storeys and occupied or vacant status, at the City, District or Township level (Administrative Level 2). Official tax records information from the city of Taipei was used to derive dwelling-to-bulding convertion factors and improve the total number of building counts. The replacement costs were also updated per building class using estimates obtained from the update costs methodology, which were revised against local data for the city of Taipei. No changes were introduced for the commercial and industrial exposure datasets in this version.

## [v2025.0.0](https://github.com/gem/global_exposure_model/East_Asia/-/tags/v2025.0.0)
All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

## [v2023.1.0](https://github.com/gem/global_exposure_model/East_Asia/-/releases/v2023.1.0)

Aggregated and disaggregated exposure added. For Japan, NSCA taxonomy substrings were added to denote anchored nonstructural components and contents and taxonomy strings were harmonized across occupancy classes. For China, revisions were made to the taxonomy mapping CSV, increasing the fraction of non-ductile and soft-storey concrete buildings and high collapse volume loss buildings. For Taiwan, the taxonomy map was revised for residential and commercial buildings.

## [v2023.0.0](https://github.com/gem/global_exposure_model/East_Asia/-/releases/v2023.0.0)

Complete revision of models for North Korea and South Korea. Population distributed to day, night, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/East_Asia/-/releases/v2022.0.0)

Replacement costs updated for all countries. The exposure model for China has been substantially improved based on feedback from the China model task force.

## [v2018.0.0](https://github.com/gem/global_exposure_model/East_Asia/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.
