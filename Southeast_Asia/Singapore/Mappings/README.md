# Notes about the development of the exposure model for Singapore
The exposure model for Singapore is not based on census data, but instead pulls together building-level information from multiple sources:

- The dataset of public residential buildings is available through the Housing and Development Board (HDB), including building height, number of units, presence of commercial units, and year of construction.
- The private residential housing stock comprises terrace houses, detached houses, semi-detached houses, bungalows, condos, and apartments, and the dataset of private residential buildings along with the number of dwelling units in each building is available through the Urban Redevelopment Authority of Singapore (URA). Year of construction and specific dwelling type is not known.
- The public industrial buildings are managed by the Jurong Town Corporation (JTC), and this building inventory is available.
- The HDB also manages a few public commercial buildings.
- All public industrial buildings that were previously managed by the HDB have now been transferred to JTC and are accounted for in the above dataset.
- The remaining (privately managed) commercial and industrial buildings are obtained through the postal codes database of Singapore — given that each building is assigned a unique postal code, the occupancy class of these buildings is inferred using the 2019 Master Plan for Singapore
- The Building Construction Authority (BCA) run an annual survey of energy efficiency of buildings in Singapore, and buildings participating in the survey report the exact gross floor area. For the buildings included in the BCA energy efficiency datasets, the exact gross floor area is used in the exposure model.
- For buildings with known footprints, the total floor area is estimated simply as the footprint area times the number of stories. The total industrial floor area available in Singapore is known (see chart below), so that's used to estimate the floor areas of the private industrial buildings. Floor areas of private commercial buildings are currently estimated based on an average value per commercial building – this can be improved if a complete building footprints layer for Singapore becomes available.
- Average replacement costs for different occupancy classes are based on Rider Levett Bucknall (2021) and Arcadis (2021).

![SGP-Industrial](https://user-images.githubusercontent.com/1707414/214595075-dd7088b5-0373-453a-9c3e-317b022a13e1.png)

![RLB_-_2021_-_Singapore_Building_Costs](https://user-images.githubusercontent.com/1707414/214595104-60410f57-b439-4076-80e5-191b8c54c391.png)
