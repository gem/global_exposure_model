
# CHANGELOG

This file contains the version history of the model.

## [v2026.0.0](https://github.com/gem/global_exposure_model/Europe/-/releases/v2026.0.0)

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

- `Italy`: New residential, commercial, and industrial exposure models for ITA, based on the new housing and population census (2021) and additional available documents (such as ISTAT reports titled as “Annuari Statistici Italiani”, and the GHS-OBAT database). The models also come with new boundary and toponomy files.
Such improvements to ITA models are carried out in the context of the PAPERS project (2025).
  - **Residential Model**
      - Integrated new data on dwellings and occupants from the 2021 Census, improving population and residential stock estimates
      - Construction materials are now mapped using a more detailed classification of building types, based on both year of construction and building height, with attributes assigned using private DPC data
      - Lateral force coefficients have been assigned in accordance with NTC18 specifications
      - Unit replacement costs have been increased by 20% to account for inflation
  - **Commercial Model**
    - The model includes commercial buildings from the 2011 Census, updated using annual data from Annuari Statistici (2012–2023). The distribution is refined at the municipality level, based on the number of employees in the commercial sector (2011 Census)
    - Construction material mapping follows the same methodology as the residential model, using year of construction and building height, assigned based on the GHS-H and GHS-S datasets
    - Unit replacement costs have been increased by 20% to account for inflation
  - **Industrial Model**
    - The shapefiles provided by ISTAT (see source) are used to delineate areas of industrial production and energy facilities, as well as quarries and mines (Macro-area M03 – Industrial and energy production facilities; quarries and mines), based on the official 2021 territorial base dataset
    - Individual industrial buildings are identified within these areas using the GHS-OBAT database, enabling a building-by-building exposure model
    - Construction material assignments are based on year of construction and building height, derived from the GHS-H and GHS-S datasets
    - Unit replacement costs have been increased by 20% to account for inflation

## [v2025.0.0](https://github.com/gem/global_exposure_model/Europe/-/tags/v2025.0.0)

All models have been updated to follow the [GEM Taxonomy v3.3](https://github.com/gem/gem_taxonomy/tree/v3.3).
In addition, the cost per area for all countries was updated to have consistency with the GEM global exposure models, where the value of the contents is not included (only building cost). The previous model considered contents, as per the ESRM2020 standards. See additional details in [merge_requests!10](https://github.com/gem/global_exposure_model/Europe/-/merge_requests/10).

Model updates also include:

- `Portugal`: The residential exposure model was updated using the 2021 census data and including the overseas territories. For RES, IND and COM models, the distribution of occupants at different times was updated, and new boundary files were considered (administrative regions with different IDs/NAMEs).
- `Türkiye`: A 2024 project with the World Bank on developing earthquake scenarios for Istanbul led to a substantial update of the exposure model for Türkiye. The new exposure considers updates in building counts, 6.11× construction cost inflation in Turkish Lira from Dec 2020 to May 2024, change in the currency exchange rate from 8.3₺/$ in Apr 2021 to 32.2₺/$ in May 2024, and population increase from 83.6 million in Dec 2020 to 85.4 million. See additional details in [merge_requests!12](https://github.com/gem/global_exposure_model/Europe/-/merge_requests/12).

## [v2023.1.0](https://github.com/gem/global_exposure_model/Europe/-/releases/v2023.1.0)

Exposure was spatially disaggregated for many countries. Revised taxonomy map. Specific updates for Turkey and Switzerland. For Turkey, buildings that collapsed in the 2023 earthquakes were removed, mixed occupancy classes were defined, and the taxonomy map was revised to increase soft-storeys, non-ductile concrete classes, and high collapse volume loss buildings. For Switzerland, floor areas and costs were updated with consideration of the ERM-CH23 model. For Italy, the masonry unit types used in residential construction was changed.

## [v2023.0.0](https://github.com/gem/global_exposure_model/Europe/-/releases/v2023.0.0)

Minor update relative to `v2022.0.0`. Population has been distributed across day, night, and transit time periods.

## [v2022.0.0](https://github.com/gem/global_exposure_model/Europe/-/releases/v2022.0.0)

The model has been updated using The European Seismic Risk Model 2020 (ESRM20) project outputs, which covered all countries except for Belarus and Ukraine. Türkiye has additionally been improved under the scope of a World Bank project.

## [v2018.0.0](https://github.com/gem/global_exposure_model/Europe/-/releases/v2018.0.0)

Original version within the larger 2018 Global Risk Model release.
