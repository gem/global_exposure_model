# Global Exposure Model

<div align='center'>

<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5b/Global_Earthquake_Model_Logo.png/440px-Global_Earthquake_Model_Logo.png" alt="GEM Foundation" width="300"/>
</p>

<a href='https://hazard.openquake.org/gem/'>
<img src='https://img.shields.io/badge/Global_Hazard_Model-green?style=for-the-badge'>
</a>

<a href='https://docs.openquake.org/vulnerability/'>
<img src='https://img.shields.io/badge/Global_Vulnerability_Model-gray?style=for-the-badge'>
</a>

<a href='https://www.globalquakemodel.org/gem-maps/global-earthquake-risk-map'>
<img src='https://img.shields.io/badge/Global_Risk_Model-orange?style=for-the-badge'>
</a>

<a href='LICENSE.txt'>
<img src='https://img.shields.io/badge/LICENSE-blue?style=for-the-badge'>
</a>

</div>

# ✨ Overview

> The v2023.1.1 release for the GEM's global exposure model is available! 🥳 🚀

This repository hosts the exposure information for the world.
It includes figures, summaries and data for each country or territory, for the region (see [Region, country and territory list](#-region-country-and-territory-list)), and for the world.

<img src="./World/World_Exposure.gif" alt="Exposure summary" width="600" >

*Global Exposure Model*

<img src="./World/World_Exposure_Taxonomies.gif" alt="Exposure macrotaxonomy" width="600" >

*Global Exposure Model macro-taxonomy*

### Available information

**At country and territory level:**
- Summary of exposure model at the national level
- Exposure model at the first administrative level
- Summary of the exposure model aggregated per building class (taxonomy)
- Figures for building counts, total replacement cost, and built-up area disaggregated per occupancy type, macrotaxonomy at the national level and at the first administrative level
- In the `_Metadata` regional folder, files are available for the mapping schemes used to associate building counts to different building classes

**At regional level:**
- Metadata for each country in the region
- Summary of regional counts and summaries per macrotaxonomy
- Figures for building counts, total replacement cost, and built-up area disaggregated per occupancy type and macrotaxonomy

**At global level:**
In the [World](./World) folder you can find
- Maps for building counts, total replacement cost, and built-up area
- Maps for main construction material
- World summaries and charts for different exposure metrics
- Charts for the top 20 countries and territories with a larger concentration of exposure


# 🚀 Model versions  

Each version of the model that is released can be accessed by changing from the `main` branch to the `tag` of a given version.
The `main` branch could contain the work-in-progress of the next version of the model.

| Version   | Release Notes                                                            |
|-----------|--------------------------------------------------------------------------|
| v2018.0.0 | Original version within the larger 2018 Global Risk Model release.       |
| [v2022.0.0](https://github.com/gem/global_exposure_model/tree/v2022.0.0) | Improvements of the global exposure model, compared with the v2018.0.0, include: <ul><li>Building counts and replacement costs updated to 2021 values (include updates in dwelling and establishment counts, mapping schemes, average area, number of stories, replacement cost, code and expected ductility level).</li><li>Reviewed non-residential models to improve spatial distribution</li></ul> |
| [v2023.0.0](https://github.com/gem/global_exposure_model/tree/v2023.0.0) | Minor revision relative to `v2022.0.0`: Population distributed across day, night, and transit time periods. Few country-specific updates.|
| [v2023.1.0](https://github.com/gem/global_exposure_model/tree/v2023.1.0) | Exposure models corresponding to the official June 2023 GEM release of the Global Risk Model. Specific modifications include:<ul><li>Canada updated the replacement costs to end-2022 values using the building construction price indexes (BCPI) from StatCan and updated the population and dwelling counts to 2023 Q1 estimates.</li><li>Ecuador and Argentina updated mapping for adobe building, now are assigned only when adobe material is specifically reported in census information. Ecuador also incorporates the urban model for metropolitan Quito.</li><li>Italy changed the masonry unit types used in residential construction</li><li>Switzerland updated floor areas and costs considering the ERM-CH23 model.</li><li>Turkey updated after M7.8_Kahramanmaras-Gaziantep earthquake (destroyed buildings removed and changes in mapping schemes).</li><li>USA major model update considering USACE NSI 2022, HAZUS 6.0, and FEMA P-366 / April 2023.</li><li>Specific countries and territories updated building taxonomies for consistency.</li><li>Minor adjustment to ensure consistency in boundary names.</li><li>Minor adjustments in taxonomy strings for additional GEM vulnerability functions.</li></ul>|
| [v2023.1.1](https://github.com/gem/global_exposure_model/tree/v2023.1.1) | Add exposure files at Adm1 level for all countries and territories (based on models v2023.1.0) |

# 🌍 Region, country and territory list

<p align="center">
  <img src="./World/World_Regions.png" alt="World regions" width="600">
</p>

The following regions, countries and territories are covered in this repository. 

| REGION                    | COUNTRIES AND TERRITORIES |
|---------------------------|---------------------------|
| Africa                    | Algeria, Angola, Benin, Botswana, Burkina_Faso, Burundi, Cameroon, Cape_Verde, Central_African_Republic, Chad, Comoros, Congo, Democratic_Republic_of_the_Congo, Djibouti, Egypt, Equatorial_Guinea, Eritrea, Eswatini, Ethiopia, Gabon, Gambia, Ghana, Guinea, Guinea_Bissau, Ivory_Coast, Kenya, Lesotho, Liberia, Libya, Madagascar, Malawi, Mali, Mauritania, Mauritius, Morocco, Mozambique, Namibia, Niger, Nigeria, Rwanda, Sao_Tome_and_Principe, Senegal, Seychelles, Sierra_Leone, Somalia, South_Africa, South_Sudan, Sudan, Tanzania, Togo, Tunisia, Uganda, Zambia, Zimbabwe |
| Caribbean_Central_America | Anguilla, Antigua_and_Barbuda, Aruba, Bahamas, Barbados, Belize, British_Virgin_Islands, Cayman_Islands, Costa_Rica, Cuba, Dominica, Dominican_Republic, El_Salvador, Grenada, Guadeloupe, Guatemala, Haiti, Honduras, Jamaica, Martinique, Montserrat, Nicaragua, Panama, Puerto_Rico, Saint_Kitts_and_Nevis, Saint_Lucia, Saint_Vincent_and_the_Grenadines, Trinidad_and_Tobago, Turks_and_Caicos_Islands, US_Virgin_Islands |
| Central_Asia              | Kazakhstan, Kyrgyzstan, Tajikistan, Turkmenistan, Uzbekistan |
| East_Asia                 | China, Hong_Kong, Japan, Macao, North_Korea, South_Korea, Taiwan |
| Europe                    | Albania, Andorra, Austria, Belarus, Belgium, Bosnia_and_Herzegovina, Bulgaria, Croatia, Cyprus, Czechia, Denmark, Estonia, Finland, France, Germany, Gibraltar, Greece, Hungary, Iceland, Ireland, Isle_of_Man, Italy, Kosovo, Latvia, Liechtenstein, Lithuania, Luxembourg, Malta, Moldova, Monaco, Montenegro, Netherlands, North_Macedonia, Norway, Poland, Portugal, Romania, Serbia, Slovakia, Slovenia, Spain, Sweden, Switzerland, Turkey, Ukraine, United_Kingdom |
| Middle_East               | Afghanistan, Armenia, Azerbaijan, Bahrain, Georgia, Iran, Iraq, Israel, Jordan, Kuwait, Lebanon, Oman, Pakistan, Palestine, Qatar, Saudi_Arabia, Syria, United_Arab_Emirates, Yemen |
| North_America             | Canada, Mexico, United_States_of_America |
| North_Asia                | Mongolia, Russia |
| Oceania                   | American_Samoa, Australia, Cook_Islands, Fiji, Guam, Kiribati, Marshall_Islands, Micronesia, Nauru, New_Caledonia, New_Zealand, Niue, Northern_Mariana_Islands, Palau, Papua_New_Guinea, Samoa, Solomon_Islands, Tonga, Tuvalu, Vanuatu |
| South_America             | Argentina, Bolivia, Brazil, Chile, Colombia, Ecuador, French_Guiana, Guyana, Paraguay, Peru, Suriname, Uruguay, Venezuela |
| South_Asia                | Afghanistan, Bangladesh, Bhutan, India, Nepal, Pakistan, Sri_Lanka |
| Southeast_Asia            | Brunei, Cambodia, Indonesia, Laos, Malaysia, Myanmar, Philippines, Singapore, Thailand, Timor_Leste, Vietnam |

# Explanation of exposure model content

## Definition of column headers

Each exposure `csv` contains the following column headers, as briefly defined below

- **ASSET_ID**: Unique identifier for an asset, which comprises a group of buildings sharing similar attributes and location
- **ID_1**: ID for the first administrative level, matches either the ID used in the national census or in the administrative division boundary vector files, or both
- **NAME_1**: Name of the first administrative level
- **ID_2**: ID for the second administrative level
- **NAME_2**: Name of the second administrative level
- ⋮
- **LONGITUDE**, **LATITUDE**: Geographical coordinates assigned to the asset for risk calculations. In general, these locations do not represent building-specific geolocations, but are either aggregated at a representative point for the lowest administrative level or are the result of the spatial disaggregation algorithm (and thus still represent aggregated assets, but at a finer resolution)
- **OCCUPANCY**: The primary occupancy class: Res for residential, Com for commercial, and Ind for industrial
- **TAXONOMY**: Building taxonomy string that is used for mapping vulnerability functions for the asset
- **BUILDINGS**: The total number of buildings comprising the asset
- **TOTAL_AREA_SQM**: The total floor area comprising the asset (sq.m.)
- **COST_PER_AREA_USD**: The average replacement cost per unit area (in 2021 US$/sq.m., including the structural and nonstructural components, but not the building contents) 
- **TOTAL_REPL_COST_USD**: The total replacement cost for the asset (in 2021 US$, including the structural, nonstructural components, and building contents) 
- **COST_STRUCTURAL_USD**: The cost of structural components in each asset
- **COST_NONSTRUCTURAL_USD**: The cost of nonstructural components in each asset
- **COST_CONTENTS_USD**: The cost of contents in each asset
- **OCCUPANTS_PER_ASSET**: The number of residents in each residential asset
- **OCCUPANTS_PER_ASSET_DAY**: The average number of occupants in each asset (residential, commercial, industrial) during the day time period
- **OCCUPANTS_PER_ASSET_TRANSIT**: The average number of occupants in each asset (residential, commercial, industrial) during the transit time period
- **OCCUPANTS_PER_ASSET_NIGHT**: The average number of occupants in each asset (residential, commercial, industrial) during the night time period
- **OCCUPANTS_PER_ASSET_AVERAGE**: The time-averaged number of occupants in each asset (residential, commercial, industrial) 

## Where can I find additional information on the defined building classes?

The building classes defined within this exposure model follow the GEM Taxonomy v3.2 convention. Please refer to the [GEM Taxonomy Glossary](https://taxonomy.openquake.org/) for additional details on taxonomy substrings and the `Taxonomy_tables_v3.2.xlsx` available [here](https://github.com/gem/gem_taxonomy/tree/master).

# 👨‍👩‍👧‍👦 Related datasets and resources

Users interested in the global exposure model might find the following GEM Foundation products useful:

* [Global Exposure Model](https://www.globalquakemodel.org/product/global-exposure-model)
* [Global Seismic Risk Map](https://www.globalquakemodel.org/products/global-seismic-risk-map)
* [Global Seismic Hazard Map](https://www.globalquakemodel.org/product/global-seismic-hazard-map)
* [Global Vulnerability Model](https://www.globalquakemodel.org/product/global-vulnerability-model)
* [OpenQuake engine](https://www.globalquakemodel.org/product/openquake-engine)

# 📚 Publications

Please cite the work as follows:
Yepes-Estrada, C., Calderon, A., Costa, C., Crowley, H., Dabbeek, J., Hoyos, M., Martins, L., Paul, N., Rao, A., Silva, V. (2023). Global Building Exposure Model for Earthquake Risk Assessment. _Earthquake Spectra_. doi:[10.1177/87552930231194048](https://doi.org/10.1177/87552930231194048)

Repository [![DOI](https://zenodo.org/badge/587390618.svg)](https://zenodo.org/badge/latestdoi/587390618)

### Regional and national model references

- Africa: Paul et al. (2022)[^13]
- Australia: Dunford and Power (2014)[^6]
- Canada: Journeay et al. (2022)[^9]
- Central America: Calderon et al. (2022)[^3]
- Central Asia: Pittore et al. (2020)[^14]
- China: Ma et al. (2021)[^10]
- Costa Rica: Calderon et al. (2019)[^2]
- Europe: Crowley et al. (2020)[^4]
- GED4GEM: Gamba et al. (2012)[^8]
- India: Rao et al. (2020)[^15]
- Iran: Motamed at al. (2019)[^11]
- Middle East: Dabbeek and Silva (2020)[^5]
- New Zealand: Abbott et al. (2020)[^1]
- Pacific Island Countries: PCRAFI initiative[^12]
- South America: Yepes-Estrada et al. (2017)[^17]
- Turkey: Rao et al. (2021)[^16]
- United States: FEMA (2017)[^7]

# 🌟 Contributors 

The authors are grateful for the input from dozens of local and international experts. A list of contributors can be found at https://www.globalquakemodel.org/risk-model-contributors.

# License
[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa], which requires:

* Attribution (you must give appropriate credit, provide a link to the license, and indicate if changes were made)
* Non-commercial (you may not use the material for commercial purposes)
* ShareAlike (derivatives created must be made available under the same license as the original)

If your use case deviates from the requirements of the offered license, but still want to explore the use of the data, please contact us at license@globalquakemodel.org  

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

Any deviation from these terms incurs license infringement. For commercial use of the data contained within this work, a specific license agreement must be made tailored to your use case, in such instance please contact GEM at product@globalquakemodel.org.

# 🤔 Frequently asked questions 

### Which version am I seeing? How to change the version?
By default, you will see the files in the repository in the  `main` branch. Each version of the model that is released is marked with a `tag`. By changing the tag version at the top of the repository, you can see the files for a given version.

Note that the `main` branch could contain the work-in-progress of the next version of the model.

### How do I download the data for a given version?
For each version, a related zip file is available in the [release section](https://github.com/gem/global_exposure_model/releases).

### Administrative regions 

The exposure models typically use the names of the administrative regions available in each country's census information, when available. However, depending on the available source data and base year for which the models are derived, the number of first-level administrative divisions and their names may differ from the _current_ divisions and names for each country. GEM does not provide associated boundary files.

### Where can I find the models at the highest available resolution?

Please contact us at product@globalquakemodel.org


# References:
[^1]: Abbott, E., Horspool, N., Gerstenberger, M., Huso, R., Van Houtte, C., McVerry, G., Canessa, S. (2020). Challenges and opportunities in New Zealand seismic hazard and risk modelling using OpenQuake. Earthquake Spectra, 36, 210-225. doi:10.1177/8755293020966338.
[^2]: Calderon, A., Silva, V. (2019). Probabilistic seismic vulnerability and loss assessment of the residential building stock in Costa Rica. Bulletin of Earthquake Engineering 17, 1257–1284. Doi: 10.1007/s10518-018-0499-1.
[^3]: Calderón, A., Silva V, Avilés, M., Méndez, R., Castillo, R., Gil, J., López, M. (2022). Toward a uniform earthquake loss model across Central America. Earthquake Spectra, 38(1):178-199. doi:10.1177/87552930211043894.
[^4]: Crowley, H., Despotaki, V., Rodrigues, D., Silva, V., Toma-Danila, D., Riga, E., Karatzetzou, A., Fotopoulou, S., Zugic, Z., Sousa, L., Ozcebe, S., Gamba, P. (2020). Exposure model for European seismic risk assessment. Earthquake Spectra, 36(1_suppl), 252–273. doi: 10.1177/8755293020919429.
[^5]: Dabbeek, J., Silva, V. (2020). Modelling the residential building stock in the Middle East for multi-hazard risk assessment. Natural Hazards 100, 781–810. doi: 10.1007/s11069-019-03842-7.
[^6]: Dunford, M., Power, L. (2014). National Exposure Information System (NEXIS) Building Exposure - Statistical Area Level 1 (SA1). Geoscience Australia, Canberra, Australia. doi: 10.4225/25/5420C7F537B15.
[^7]: FEMA, Federal Emergency Management Agency (2017). FEMA P-366: Hazus® Estimated Annualized Earthquake Losses for the United States.
[^8]: Gamba, P., Cavalca, D., Jaiswal, K., Huyck, C., Crowley, H. (2012). The GED4GEM Project: Development of a Global Exposure Database for the Global Earthquake Model Initiative. Proceedings of the 15th World Conference on Earthquake Engineering, Lisbon, Portugal.
[^9]: Journeay, M., LeSueur, P., Chow, W., Wagner, C.L. (2022). Physical exposure to natural hazards in Canada: An overview of methods and findings. GEOLOGICAL SURVEY OF CANADA, OPEN FILE 8892. Available at https://doi.org/10.4095/330012.
[^10]: Ma, J., Rao, A., Silva, V., Lui, K., Wang, M. (2021). A township-level exposure model of residential buildings for mainland China. Nat Hazards 108, 389–423. https://doi.org/10.1007/s11069-021-04689-7
[^11]: Motamed, H., Calderon, A., Silva, V., Costa, C. (2019). Development of a probabilistic earthquake loss model for Iran. Bulletin of Earthquake Engineering 17, 1795–1823. doi: 10.1007/s10518-018-0515-5.
[^12]: [Pacific: Catastrophe Risk Assessment and Financing Initiative - PCRAFI](https://pcric.org/)
[^13]: Paul, N., Silva, V., Amo-Oduro, D. (2022). Development of a uniform exposure model for the African continent for use in disaster risk assessment. International Journal of Disaster Risk Reduction, Volume 71, ISSN 2212-4209. doi: 10.1016/j.ijdrr.2022.102823.
[^14]: Pittore, M., Haas, M., Silva, V. (2020). Variable resolution probabilistic modelling of residential exposure and vulnerability for risk applications. Earthquake Spectra, 36(1_suppl), 321-344. doi:10.1177/8755293020951582
[^15]: Rao, A., Dutta, D., Kalita, P., Ackerley, N., Silva, V., Raghunandan, M., Ghosh, J., Ghosh, S., Brzev, S., Dasgupta, K. (2020). Probabilistic seismic risk assessment of India. Earthquake Spectra, 36(1_suppl), 345–371. doi: 10.1177/8755293020957374.
[^16]: Rao, A., Calderón, A., Silva, V., Martins, L., Paul, N. (2021). Earthquake Risk Assessment and Retrofit Scenarios for Turkey. Report for the World Bank.
[^17]: Yepes-Estrada, C., Silva, V., Valcárcel J, Acevedo, A., Tarque, N., Hube, M., Coronel, G., Santamaría, H. (2017). Modelling the Residential Building Inventory in South America for Seismic Risk Assessment. Earthquake Spectra, 33(1), 299-322. doi:10.1193/101915eqs155dp.
