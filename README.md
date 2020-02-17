# R---Tidying-and-Analysis
## Living Planet Index Report Tidying and Analysis
### Source: 
For this assignment, I have used dataset obtained from the website [Living Planet Index](http://www.livingplanetindex.org/projects?main_page_project=LivingPlanetReport&home_flag=1).

### Background and Charateristics of the Dataset
The Living Planet is a comprehensive study of trends in global biodiversity and the health of the planet based on population trends of vertebrate species from terrestrial, freshwater and marine habitats.The period covered by this report is from 1950 to 2016 and has data for over 2805 unique species belonging to  11 different classes. In addition to the population data, each time series is assigned to a system–terrestrial, freshwater and marine–based on both the location of the monitored population and the habitat the species mostly relies on. Analysis has been done for the complete dataset with focus on the African region.

### Variables
Below is the list of variable available in this dataset.  
1. **ID**:	Unique identifier  
2. **Binomial**:	Binomial Nomenclature i.e. the formal naming system of living things used by scientists  
3. **Reference**:	Reference for the binomial  
4. **Class**:	Contains 8 different Animal Kingdom classes  
5. **Order**:	Taxonomic rank used for classification of organisms and recognized by the nomenclature codes  
6. **Family**: Taxonomic rank, classified between genus and order  
7. **Genus**: 	Taxonomic rank for bilogical classification, comes above species and below family  
8. **Species**:	Basic unit of classification and a taxonomic rank of an organism, as well as a unit of biodiversity  
9. **Subspecies**:	a taxonomic category that ranks below species, usually a fairly permanent geographically isolated race  
10. **Common_name**:	name commonly used by general public to refer to a particular species  
11. **Location**:	exact location of the species  
12. **Country**:	Country where the species is found  
13. **All_countries**:	List of countries where the species is found  
14. **Region**:	Region where the species is found  
15. **Latitude**:	Latitude of the location  
16. **Longitude**:	Longitude of the location  
17. **Specific_location**:	value is 0 or 1  
18. **temperate_or_tropical**:	temperate has value 1 and tropical has value 2  
19. **System**:	provides information if the system is terrestial,marine or freshwater  
20. **T_realm**:	terrestial realm data  
21. **T_biome**:	terrestial biome data  
22. **FW_realm**:	freshwater realm data  
23. **FW_biome**:	freshwater biome data  
24. **M_realm**:	marine realm data  
25. **M_ocean**:	marine ocean data  
26. **M_biome**:	marine biome data  
27. **Units**:	units of measurement of population  
28. **Method**:	method of sampling  
29-95. **1950-2016**:	Years for which data is available  

### Data Wrangling: Tidy Principle
There are 3 Tidy Principles.  
1. Each variable must have its own column.  
2. Each observation must have its own row.  
3. Each value must have its own cell.    

This dataset breaks the second one - Within the table, each year is a separate column. Since each observation must have its own row, I consolidated them into a single year column using "Gather" from tidyr package. I also used dplyr package to do some data manipulation. For plotting I have used packages ggplot, ggthemes,rworldmap 

