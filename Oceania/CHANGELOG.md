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

### Country-specific model updates

New models have been developed for 13 countries (COK, KIR, MHL, FSM, NRU, NIU, NZL, PLW, WSM, SLB, TON, TUV and VUT):

- In the previous release, the models were primarily based on data from PCRAFI (I and II), mapped to the GEM taxonomy and formats. The updated models are now constructed using national census information, while also incorporating elements from earlier versions to refine the mappings, building classifications, and replacement cost estimates. For models originally derived from PCRAFI I, inflation adjustments were applied, where data were available, to update cost estimates to current values.
- `AUS`: The models have been updated using NEXIS v5.19 shared by Geoscience Australia. The resolution is Statistical Areas 1 (SA1), as before, but now tagged as Admin 5. Boundaries have been updated to be aligned with the ASGS 2021 boundaries used in the GA models. A simplified mapping scheme for GA building classes has been used for now, without including much details of roof and exterior walls. Building classes reflect the evolution of the building codes. Prior to 1979 no seismic regulations were in place in Australia. After the introduction of the first seismic code (CDL) in 1979, and until 1995, still very few buildings were built according to seismic regulations. With the introduction of the new seismic code AS 1170.4 (CDM), and its update in 2007 (CDH), all buildings are expected to be following the seismic code. Contents cost is estimated using GEM's cost distribution function for COM and IND models, while the values for the residential model are based on NEXIS data. The model includes the updated methodology for occupants' distribution and spatial disaggregation.
- `NZL` (RES): The development of the residential exposure model used as input information the latest datasets available from Stats NZ: dwellings (Adm5) and residents (Adm2) from 2023 census 2023 and building consents (Adm4) for the period 2023-2025 (post census). The model is at administrative level 5, which corresponds to the Statistical Areas 1 (100–200 residents). Material and lateral load resisting system mappings from the 2021 model (based on GNS data) were used. In addition, reference construction costs by dwelling type from the recent datasets were used to estimate the replacement cost and average area by dwelling type (Stats NZ) were considered. The update includes a review of the seismic design regulations and seismic zoning maps since 1930s. Building replacement cost by NEXIS is used. The model includes the updated methodology for occupants' distribution and spatial disaggregation.
- `US oversea territories` (American Samoa, Guam, Northen Mariana Islands): HAZUS v6.1 model shared by the USGS. The model includes building and housing counts for 2020. Costs and population updated to 2025 figures by the USGS. The number of households and occupants at different times of the day are included in the shared model.

## [v2025.0.0](https://github.com/gem/global_exposure_model/Oceania/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

Exposure model updates for seven countries: COK, SLB, TON, VUT, WSM, PNG, and FJI. The updates include revisions of residential, commercial, and industrial exposure models, incorporating the latest available data for each country.

For FJI and PNG, the latest information on population estimates and building counts was used to update counts. For the other countries (COK, SLB, TON, VUT, WSM), the latest 2024 PCRAFI II data was used to update the models.See additional details in [merge_requests!8](https://github.com/gem/global_exposure_model/Oceania/-/merge_requests/8).


## [v2023.1.0](https://github.com/gem/global_exposure_model/Oceania/-/releases/v2023.1.0)

Aggregated and disaggregated exposure files included. Lightweight roofs assigned to adobe buildings for the PNG and Oceania taxonomy mapping files. Additionally, the new WBB and INF vulnerability classes are referenced in the taxonomy maps


## [v2023.0.0](https://github.com/gem/global_exposure_model/Oceania/-/releases/v2023.0.0)

Minor update relative to `v2022.0.0`. Population, dwellings, and building counts brought to year 2020/1 for:  KIR, NRU, PNG, SLB, and VUT. Population distributed across day, night, and transit time periods.


## [v2022.0.0](https://github.com/gem/global_exposure_model/Oceania/-/releases/v2022.0.0)

Updated the replacement costs for all the countries in the region. Non-residential models for FJI updated using the latest census data. Exposure models for FJI, NCL, PNG, TLS disaggregated to a 0.04deg resolution using WorldPop population estimates. Australia updated to reflect NEXIS 2020.


## [v2018.0.0](https://github.com/gem/global_exposure_model/Oceania/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.

