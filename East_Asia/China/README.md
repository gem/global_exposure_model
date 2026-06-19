# 🇨🇳 China Exposure Model

This page provides an overview of the exposure model for China, including national totals, predominant building classes, and subnational distribution.

The exposure model provides an open and harmonised representation of the national building inventory across residential (RES), commercial (COM), and industrial (IND) occupancies, developed within the Global Earthquake Model (GEM) framework.

## ✨ What's New in `v2026.0.0`

- **Unified Framework**: Consistent modelling approach across datasets
- **Standardised Divisions**: First-level administrative divisions carefully reviewed and harmonized
- **Building Classification**: Based on [GEM Building Taxonomy v4.0](https://tools.openquake.org/taxonomy/)
- **Temporal Distribution**: Occupant distribution modelled for different times of day
- **Reference Year**: Building counts, replacement cost and population aligned to 2025
- **Spatial Resolution**: 0.01 degrees (approximately 1×1 km²) grid disaggregation with building-level representations where available
- **Replacement Costs**: Derived from multiple AI-driven models combined with expert judgement
- **Embodied Carbon**: Estimates integrated to support climate impact considerations
- **Versatile Application**: Framework adaptable to various natural hazards beyond seismic risk

For more information, visit the [GEM Global Risk Model documentation](https://docs.openquake.org/global_risk_model/) site.
Spatially disaggregated models are also available and can be accessed by submitting a request through the [GEM License Request page](https://www.globalquakemodel.org/license-request/global-exposure-model).

## 🔎 Quick links

[[_TOC_]]

## National summary

The exposure model includes the distribution of buildings, replacement value, exposed population and embodied carbon. The total exposure includes 244.0 million buildings, USD 41.5 trillion in replacement cost, and 1.4 billion occupants. The figure below shows the spatial distribution of building counts aggregated onto a discrete hexagonal grid at H3 resolution 7. See [Adm0 summary table](summaries/Exposure_Summary_Adm0.csv) for additional national level metrics.

<!-- Map with national buildings -->
![Spatially distributed building exposure](summaries/map_hex.png)

_Figure: Spatial distribution of building counts aggregated onto a discrete hexagonal grid_

<!-- Table with Adm0 summary -->
_Table: National exposure model per occupancy class._

| COUNTRY | OCCUPANCY | BUILDINGS | OCCUPANTS | REPLACEMENT COST (USD) | BUILT-UP AREA (SQM) | EMBODIED CARBON (TON) |
|---|---|---|---|---|---|---|
| China | COM | 35.4 M |  | 8.0 T | 10.7 B | 6.2 B |
| China | IND | 19.2 M |  | 4.9 T | 12.5 B | 7.1 B |
| China | RES | 189.4 M | 1.4 B | 28.6 T | 50.0 B | 19.6 B |

<!-- Figures -->
![National exposure by occupancy class](summaries/adm0_occ.png)

_Figure: Contribution of occupancy classes to total national exposure_

## Building Classes

The exposure model classifies the building stock into a set of representative building classes that capture the predominant construction typologies within the country or region. These classes are defined using the [GEM Building Taxonomy v4.0](https://tools.openquake.org/taxonomy/), which provides a standardized framework for grouping buildings with similar structural characteristics. At a minimum, each class is described by attributes such as the primary construction material, lateral load-resisting system, code level, seismic design level, number of stories, and occupancy type; additional attributes may be included where more detailed information is available. Detailed descriptions and illustrations of taxonomy attributes are available in the [Glossary](https://tools.openquake.org/taxonomy/) tab.

For the complete list of building classes in the country or territory, see [Taxonomy summary table](summaries/Exposure_Summary_Taxonomy.csv). Each building class is linked to a corresponding vulnerability class through a vulnerability mapping, available as `Vulnerability_mapping_CHN.csv`, following the definitions of the [GEM Global Vulnerability Model](https://github.com/gem/global_vulnerability_model).

![Exposure by taxonomy classes](summaries/taxo.png)

_Figure: Predominant building classes ranked by their contribution to the national exposure model_

The figure below shows the distribution of the exposure model aggregated by `MACRO_TAXONOMY`, a simplified classification that groups building classes according to their predominant construction material and structural system. The categories are defined as follows: `ADO|ST|E` (adobe, stone masonry, and earthen construction), `CR+` (reinforced concrete designed and constructed in accordance with building code requirements), `CR-` (reinforced concrete with limited or no code compliance), `HYB` (hybrid construction combining multiple material classes), `MR|MCF` (reinforced or confined masonry), `MUR` (unreinforced masonry), `S` (steel construction), `W` (wood, bamboo, wattle-and-daub construction), and `OT` (other building classes not included in the preceding categories). This aggregation provides a concise overview of the composition of the building stock while preserving the key structural characteristics relevant for seismic risk assessment.

![National exposure by taxonomy](summaries/adm0_taxo.png)

_Figure: National distribution of exposure by macro-taxonomy_


## Subnational summary

The subnational summary aggregates exposure by first administrative level and supports comparison of spatial concentration of assets. For additional information on the exposure, at the first administrative level, see [Adm1 summary table](summaries/Exposure_Summary_Adm1.csv).

The names of the subnational exposure units (first administrative divisions) have been carefully reviewed, harmonized, and are actively maintained by GEM. The source of the administrative boundaries used is available in the [metadata](#metadata) section.

<!-- Map with national buildings -->
![Adm1 building exposure](summaries/map_adm1.png)

_Figure: Number of buildings at the first-level administrative units_

![Subnational exposure by taxonomy](summaries/adm1_taxo.png)

_Figure: Distribution of predominant building classes across first-level administrative units_


## Source Data

The table below provides source data information for the exposure model components.
For information on modelling assumptions, construction practice and building code, visit the [GEM Global Risk Model documentation](https://docs.openquake.org/global_risk_model/) site.

<!-- Table metadata -->
_Table: Exposure model metadata including data sources, versions, and references._

| COMPONENT | DATA_SOURCES | PUBLISHER | DATA_YEAR | UPDATE_YEAR | ADM_LEVEL | VARIABLES | LICENSE | LINKS | NOTES |
|---|---|---|---|---|---|---|---|---|---|
| RES | Sixth National Population Census (2010)<br>Province Housing Data Tables (2010)<br>County Household Data Tables (2010)<br>Township Population Data Tables (2010)<br>1% Population Sampling Survey (2015)<br>National Statistical Yearbook Tables (2017)<br>Province Statistical Yearbook Tables (2017)<br>City Statistical Yearbook Tables (2010-17) | National Bureau of Statistics of China | 2010 | 2025.0 | 4 | Primary construction type<br>Number of storeys<br>Period of construction<br>Settlement type (urban, town, rural) |  | China: http://www.stats.gov.cn/english/Statisticaldata/CensusData/rkpc2010/indexce.htm<br><br>Heilongjiang: http://www.hlj.stats.gov.cn/tjnj/2017nj.zip<br>Shanghai: http://www.stats-sh.gov.cn/html/sjfb/201801/1001529.html<br>Jiangsu: http://www.jssb.gov.cn/2017nj/nj01.htm<br>Zhejiang: http://tjj.zj.gov.cn/tjsj/tjnj/DesktopModules/Reports/14.浙江统计年鉴2017/excel/en/index.html<br>Anhui: http://www.ahtjj.gov.cn/tjjweb/tjnj/2017/cn.html<br>Fujian: http://tjj.fujian.gov.cn/tongjinianjian/dz2017/index-cn.htm<br>Jiangxi: http://www.jxstj.gov.cn/resource/nj/2017CD/indexee.htm<br>Shandong: http://www.stats-sd.gov.cn/tjnj/nj2017/indexee.htm<br>Henan: http://www.ha.stats.gov.cn/hntj/lib/tjnj/2017/indexee.htm<br>Hubei: http://data.hb.stats.cn/PlatForm/Attach/201704/7241_201609280221059.rar<br>Hunan: http://data.hntj.gov.cn/sjfb/tjnj/16tjnj/indexee.htm<br>Guangdong: http://www.gdstats.gov.cn/tjsj/gdtjnj/201711/U020180323391593622005.zip<br>Guangxi: http://www.gxtj.gov.cn/tjsj/tjnj/2017/indexee.htm<br>Hainan: http://stats.hainan.gov.cn/2017nj/indexee.htm<br>Chongqing: http://www.cqtj.gov.cn/tjnj/2017/indexee.htm<br>Sichuan: http://www.sc.stats.gov.cn/tjcbw/tjnj/2016/zk/indexee.htm<br>Guizhou: http://www.gz.stats.gov.cn/tjsj_35719/sjcx_35720/gztjnj_40112/2017/index_26.html<br>Yunnan: http://www.stats.yn.gov.cn/tjsj/tjnj/201701/t20170123_675375.html<br>Shaanxi: http://www.shaanxitj.gov.cn/upload/2018/7/zk/indexee.htm<br>Gansu: http://www.gstj.gov.cn/HdAtt/att/2018/03/20180321111139347.rar<br>Qinghai: http://www.qhtjj.gov.cn/nj/2017/indexce.htm<br>Ningxia: http://www.nxtj.gov.cn/tjsj/ndsj/2017/indexfiles/indexch.htm<br>Xinjiang: http://www.xjtj.gov.cn/sjcx/tjnj_3415/ | Project residential exposure from 2010 to 2020 census using prov census counts |
| IND, COM | Third National Economic Census | National Bureau of Statistics of China | 2014 | 2025.0 | 1 | Establishments by economic activity |  | https://data.stats.gov.cn/english/ |  |
| OCCUPANTS | as for RES | National Bureau of Statistics of China | 2010 | 2025.0 | as for RES |  |  |  | Project residential exposure from 2010 to 2020 census using prov census counts |
| BOUNDARIES | GAUL | GAUL | 2025 |  | 1 | Administrative divisions at level 1 | CC BY 4.0 | https://data.apps.fao.org/catalog/iso/34f97afc-6218-459a-971d-5af1162d318a |  |

## Exposure Model Columns

Definitions and descriptions of the columns in the exposure summary tables.

<details>
  <summary>👀 click to see definitions and descriptions</summary>

| HEADER | DESCRIPTION |
|---|---|
| ASSET_ID | Unique identifier for an asset, which comprises a group of buildings sharing similar attributes and location |
| ID_0 | ISO3 code for the country |
| NAME_0 | English name for the country |
| ID_1 | ID for the first administrative level, matches either the ID used in the national census or in the administrative division boundary vector files, or both |
| NAME_1 | Name of the first administrative level |
| ID_i | ID for the "ith" administrative level |
| NAME_i | Name of the "ith" administrative level |
| LONGITUDE | Geographical longitude cordinate of the asset location. In general, these locations do not represent building-specific geolocations, they represent points as a result of a spatial disaggregation algorithm (and thus still represent aggregated assets) but at a finer resolution. |
| LATITUDE | Geographical latitude cordinate of the asset location. In general, these locations do not represent building-specific geolocations, they represent points as a result of a spatial disaggregation algorithm (and thus still represent aggregated assets) but at a finer resolution. |
| OCCUPANCY | Primary occupancy class (RES: residential; COM: commercial; IND: industrial) |
| OCCUPANCY_TYPE | Detailed occupancy providing a finer classification within the primary OCCUPANCY class, describing the specific functional use of the structure as defined in the GEM taxonomy (e.g., [RES:1] single dwelling; [COM:3C] hotels and motels; [IND:2] light-industry factories). |
| SETTLEMENT | Type of settlement (e.g., URBAN, RURAL, SUBURBAN, URBAN_CENTER) |
| TAXONOMY | Building taxonomy string that is used for mapping vulnerability functions for the asset |
| TAXONOMY_HAZUS | Building taxonomy string compatible with HAZUS classification |
| MACRO_TAXONOMY | High-level classification of building types used in the Global Exposure Model for statistical analysis |
| BUILDINGS | The total number of buildings comprising the asset. A building unit is defined as a permanent, separate, and independent structure designed to serve any activity. For constructions comprising blocks, terraced buildings, or buildings enclosed by common fencing, a building unit refers to the superstructure that is structurally designed to respond independently under seismic loads |
| DWELLINGS | The total number of dwellings comprising the asset.  A dwelling unit is defined as a self-contained residential space within a building designed for habitation by one or more individuals or families. For example, a multi-story residential building is comprised of numerous dwelling units, such as multiple apartments within the same structure. Conversely, in a single-family detached unit, the number of dwelling units and buildings is the same |
| ESTABLISHMENTS | The total number of establishments comprising the asset. An establishment is defined as a single physical location where economic activities occur (e.g., services or industrial operations). An establishment is often characterized by having a specific address, management, and operational control, distinct from other units of the same company or organization. |
| OCCUPANTS_TOTAL | The number of residents in each residential asset |
| OCCUPANTS_DAY | The average number of occupants in each asset during the day-time period |
| OCCUPANTS_TRANSIT | The average number of occupants in each asset during the transit time period |
| OCCUPANTS_NIGHT | The average number of occupants in each asset during the night-time period |
| OCCUPANTS_AVERAGE | The time-averaged number of occupants in each asset (residential, commercial, industrial) |
| AVG_DWL_AREA_SQM | Floor area of a dwelling unit (sqm) |
| TOTAL_AREA_SQM | The total floor area comprising the asset (sqm) |
| COST_PER_AREA_USD | The average building cost (as built) per unit area (in US dollars). It includes the structural and nonstructural components, but not the building contents. |
| COST_PER_AREA_LOCAL | Idem as COST_PER_AREA_USD but using the local currency |
| BLDG_REPL_COST_USD | Cost to construct or replace the building components (structural and nonstructural) of  the asset. It does not  includues the contents. |
| COST_STRUCTURAL_USD | Cost to construct or replace (as built) in US dollars of structural components in each asset |
| COST_NONSTRUCTURAL_USD | Cost to construct or replace  (as built) in US dollars of nonstructural components in each asset |
| COST_CONTENTS_USD | Cost to construct or replace  (as built) in US dollars of contents in each asset |
| TOTAL_REPL_COST_USD | Cost to construct or replace the asset with equal quality and construction in US dollars (including the structural, nonstructural components, and building contents) |
| YEAR | Year of construction or retrofit |
| CARBON_BUILDINGS_TON | The building replacement embodied carbon in Ton CO2e for the asset, including structural and nonstructural components (no building contents) |
</details>

## Other Resources

- [Regional overview](../README.md)
- [Model versions](../CHANGELOG.md)
- [Frequently asked questions](../README.md#frequently-asked-questions)
- [Contributors](../README.md#contributors)
- [How to cite this work](../README.md#publications)
- [License](../README.md#license)