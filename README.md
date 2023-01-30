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

> The v2023.0.0 release for the GEM's global exposure model is available! 🥳 🚀

This repository hosts the exposure information for the world.
It includes figures, summaries and data for each country, for the region (see [Region and country list](#-region-and-country-list)), and for the world.

<img src="./World/World_Exposure.gif" alt="Exposure summary" width="600" >

*Global Exposure Model*

<img src="./World/World_Exposure_Taxonomies.gif" alt="Exposure macrotaxonomy" width="600" >

*Global Exposure Model macro-taxonomy*


### Available information
**At country level:**
- Summary of exposure model at national level
- Exposure model at the first administrative level
- Summary of the exposure model aggregated per building class (taxonomy)
- Figures for building counts, total replacement cost, and built up area disaggregated per occupancy type, macrotaxonomy at national level and at the first administrative level
- Folder with mapping-schemes used to associate building counts to different building classes

**At regional level:**
- Metadata for each country in the region
- Summary of regional counts and summaries per macrotaxonomy
- Figures for building counts, total replacement cost, and built up area disaggregated per occupancy type and macrotaxonomy

**At global level:**
In the [World](./World) folder you can find
- Maps for building counts, total replacement cost, and built up area
- Maps for main construction material
- World summaries and charts for different exposure metrics
- Charts for top 20 countries with larger concentration of exposure


# 🚀 Model versions  

Each version of the model that is released can be accessed by changing from the `main` branch to the `tag` of a given version.
The `main` branch could contain the work-in-progress of the next version of the model.

| Version   | Release Notes                                                            |
|-----------|--------------------------------------------------------------------------|
| v2018.0.0 | Original version within the larger 2018 Global Risk Model release.       |
| [v2022.0.0](https://github.com/gem/global_exposure_model/tree/v2022.0.0) | Improvements of the global exposure model, compared with the v2018.0.0, include: <ul><li>Building counts and replacement costs updated to 2021 values (include updates in dwelling and establishment counts, mapping schemes, average area, number of stories, replacement cost, code and expected ductility level).</li><li>Reviewed non-resisential models to improve spatial distribution</li></ul> |
| [v2023.0.0](https://github.com/gem/global_exposure_model/tree/v2023.0.0) | Minor revision relative to `v2022.0.0`: Population distributed across day, night, and transit time periods. Few country specific updates.|


# 🌍 Region and country list

<p align="center">
  <img src="./World/World_Regions.png" alt="World regions" width="600">
</p>

The following regions and countries are covered in this repository. 

| REGION                    | COUNTRIES |
|---------------------------|-----------|
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



# 📚 Publications

Please cite the work as follows:
Yepes-Estrada, C., Calderon, A., Costa, C., Crowley, H., Dabbeek, J., Hoyos, M., Martins, L., Paul, N., Rao, A., Silva, V. (2023). Global Exposure Modeling for Earthquake Risk Assessment. Under review in Earthquake Spectra.
<!-- ---

!!!TO BE ADDED!!!

[![DOI:10.1177/8755293019899953](http://img.shields.io/badge/DOI-10.1177/8755293019899953-2874A6.svg)](https://doi.org/10.1177/8755293019899953)

--- -->


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
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg


# 🤔 Frequently asked questions 

### Which version am I seeing? How to change the version?
By default you will see the files in the repository in the  `main` branch. Each version of the model that is released can be accessed is marked with a `tag`. By changing the tag version at the top of the repository, you can change see the files for a given version.

Note that the `main` branch could contain the work-in-progress of the next version of the model.

### How do I download the data for a given version?
For each version, a related zip file is available in the [release section](https://github.com/gem/global_exposure_model/releases).

### Where can I find additional information on the defined building classes?

The building classes defined within this exposure model follow the GEM Taxonomy convention. Please refer to the [GEM Taxonomy Glossary](https://taxonomy.openquake.org/) for additional details on taxonomy substrings.

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
[^17]: Yepes-Estrada, C., Silva, V., Valcárcel J, Acevedo, A., Tarque, N., Hube, M., Coronel, G., Santamaría, H. (2017). Modelling the Residential Building Inventory in South America for Seismic Risk Assessment. Earthquake Spectra, 33(1), 299-322. doi :10.1193/101915eqs155dp.
