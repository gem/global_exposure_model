# CHANGELOG

This file contains the version history of the model.

## [v2026.0.0](https://github.com/gem/global_exposure_model/South_America/-/releases/v2026.0.0)

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

- `Brazil`: Updated exposure models developed under the World Bank (JBA) project. The revision incorporates data from the 2022 Population and Housing Census, the 2022 Establishment Survey (Cadastro Central de Empresas), and earth observation datasets (GHSL) to estimate building heights and construction years. A comprehensive review of the model was conducted, improving the classification of buildings by height, construction year, and building code level. The update also includes an enhanced methodology for occupant distribution, as well as revised average construction areas and replacement costs, resulting in significant differences from the previous version.

- `Colombia`: The commercial, industrial, and residential exposure models for Colombia were updated using data from the Registro Estadístico de Empresas (2021) and the 2018 National Population and Housing Census, with national projections to 2025.
    - Integration of building heights derived from the Global Human Settlement Layer (GHSL, 2025) to improve structural class assignment across all models.
    - The non-residential (commercial and industrial) models incorporate enterprise-level data reported by DANE for 2021 (not projected), improving area and cost estimation, with increased spatial resolution from Adm1 to Adm2.
    - The residential model includes refined mapping schemes with city-specific configurations for Bogotá, Cali, Medellín, and Barranquilla, and a national mapping for the rest of the country, informed by previous GEM projects and expert assessments; model resolution increased from Adm2 to Adm4.
    - Residential exposure is represented at block level in urban areas and census section level in rural areas, explicitly including the number of dwellings.
    - Building costs were revised using updated national references and adjusted to account for regional differences and socio-economic strata.
    - Administrative boundaries were not updated due to inconsistencies between input data distributions and the latest area code definitions.
- `Ecuador`: The commercial, industrial, and residential exposure models were updated using data from the Registro Estadístico de Empresas (2023) and the 2022 Population and Housing Census, with national projections to 2025.
    - Integration of building heights derived from the new generation of raster data from the Global Human Settlement Layer (GHSL, 2025) to estimate building heights and improve structural classification.
    - The non-residential (commercial and industrial) inventories now incorporate  enterprise size information to refine area estimates. Increased from Adm1 to Adm2 source data resolution.
    - The residential model has updated mapping schemes, combining housing type, wall material, and satellite-derived height data to assign structural classes consistent with the observed height distribution. Increased model resolution from Adm3 to Adm4.
    - Boundaries updated following the 2022 INEC administrative revision:
    - Building costs revised to reflect updated national estimates.

- `Peru`: The commercial, industrial, and residential exposure models were updated using the most recent data sources. Building heights for all models derived from the Global Human Settlement Layer (GHSL, 2025) to improve estimation of structural classes.
    - Building costs revised to reflect updated national references.
    - The residential model uses data from the 2017 Population and Housing Census (as in the previous version). Building counts were adjusted according to population projections for 2025. Mapping scheme were refined to improve the distribution of building classes consistent with the observed height distribution.
    - For the non-residential (commercial and industrial) models, updated data from the latest National Economic Census is included. Improved spatial resolution from Adm1 to Adm3. Enterprise size information included to enhance estimation of built areas.
    - Boundaries updated using the latest data retrieved in 2025 from the Instituto Nacional de Estadística e Informática (INEI).

- `Chile`: The commercial, industrial, and residential exposure models for Chile were updated using data from the Detalle Catastral de Bienes Raíces provided by the Servicio de Impuestos Internos (2023) and the 2024 Population and Housing Census, with national projections to 2025.
- Integration of building heights derived from the Global Human Settlement Layer (GHSL, 2025) to improve structural class assignment across all models.
- The non-residential (commercial and industrial) inventories now incorporate predominant construction material information directly provided by the official source, improving the assignment of building classes. Built areas were also replaced with values reported directly in the cadastral database, refining area and cost estimation. Source data spatial resolution increased from Adm1 to Adm3.
- The residential model includes updated mapping schemes combining housing type, wall material, floor material, roof material, construction year, and satellite-derived height data to assign structural classes consistent with the observed height distribution.
- Residential information from the 2024 census was only available at Adm3 resolution; more detailed spatial levels were obtained through disaggregation procedures.
Boundaries updated following the 2024 administrative revision published by the Instituto Nacional de Estadísticas (INE).


## [v2025.0.0](https://github.com/gem/global_exposure_model/South_America/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).

## [v2023.1.0](https://github.com/gem/global_exposure_model/South_America/-/releases/v2023.1.0)

Adjustments to the mapping schemes for adobe classes. Additionally, the taxonomy mapping was revised to reflect the distribution of light versus heavy roofs for adobe buildings and to incorporate the new WBB and INF vulnerability classes. Spatial disaggregation was run, but only for the admin areas where refined exposure was not available from local projects in Colombia, Ecuador, and Chile.

## [v2023.0.0](https://github.com/gem/global_exposure_model/South_America/-/releases/v2023.0.0)

Minor revision relative to `v2022.0.0`. Population distributed across day, night, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/South_America/-/releases/v2022.0.0)

- Update Chile res to consider the 2017 Census
- Update Peru res to consider the 2017 Census
- Update Brazil res from GED4GEM country to SARA type country (still using latest available census 2010)
- Update Colombia res to consider the 2018 Census. Change workflow to begin from Edificaciones 'Buildings' available in 2018 Census. Add socio-economic income as variable. Follow workflow from Acevedo (Check mail April 28 2022 for further details). In this version it is still using average costs for all country not region specific ones.
- Household counts and population amplified based on UN numbers for 2021.
- Updated non-res with latest economic census or directories for Chile (2020), Colombia (2020) and Brazil (2019).
- Reduced non-res counts by 10% to account for possible mixed buildings.
- Update of all costs considering cost databases and inflation.
- Changed workflow of WIP to include step to do disaggregation of res and non-res with NP code.
- Updated Chile, Brazil, Colombia, Peru and Argentina shapefiles.
- Updated taxonomy mapping to include specific ones for most SARA countries.

## [v2018.0.0](https://github.com/gem/global_exposure_model/South_America/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.

