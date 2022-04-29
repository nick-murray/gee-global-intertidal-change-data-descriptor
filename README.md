# Data descriptor for: Murray global tidal wetland change (2022)

#### File description:

This data descriptor describes the Global Intertidal Change data products associated with the paper High-resolution mapping of losses and gains of Earth's tidal wetlands (2022) *Science*. The principal data product is a set of change maps, consisting of 6 raster bands split into single images for publication:

* `"loss", 0-1` - integer representing loss (1).
* `"lossYear", 01:19, 3` - integer representing the end year of the time-step of analysis (e.g., 19 = 2017-2019).
* `"lossType, 2,3,5` - integer representing intertidal ecosystem type: Tidal flat (2), Mangrove (3), Tidal marsh (5)).
* `"gain", 0-1` - integer representing gain (1).
* `"gainYear",  01:19, 3`  - integer representing the end year of the time-step of analysis (e.g., 19 = 2017-2019).
* `"gainType", 2,3,5` - integer representing intertidal ecosystem type: Tidal flat (2), Mangrove (3), Tidal marsh (5)).

In addition, we provide two tidal wetland extent images:

* `gic_s1_probability, 0-100` - integer which represents the agreement of random forest decision trees for the tidal wetland class in t1 of the analysis, 2001 
* `gic_s1_probability, 0-100` - integer which represents the agreement of random forest decision trees for the tidal wetland class in t7 of the analysis, 2019 

A full description of the methods, validation, and limitations of the data produced by this software is available in the published paper. For project updates,  frequently asked questions, and Google Earth Engine code examples please refer to the [project website](https://www.globalintertidalchange.org/). 

Code to develop the 6 band change product and two extent bands are available at DOI: 
N. Murray et al., Code for high-resolution mapping of losses and gains of Earth's tidal wetlands v1.0.0 Zenodo (2022) https://doi.org/10.5281/zenodo.5968865

Training data used to develop the extent product is available at DOI: 
N. Murray et al. Intertidal ecosystem training data for mapping Earth's tidal wetlands. Figshare (2022) https://doi.org/10.6084/m9.figshare.19121660

#### Citation
Use of any aspect of this study requires full attribution (see licence). 

Please cite the published paper:

Murray, N.J., Worthington, T.A., Bunting, P., Duce, S., Hagger, V., Lovelock, C.E., Lucas, R., Saunders, M.I., Sheaves, M., Spalding, M., Waltham, N.J., Lyons, M.B., 2022. High-resolution mapping of losses and gains of Earth's tidal wetlands. *Science*. [paper link](https://doi.org/10.1126/science.abm9583)


#### User notes and caveates
There are several important considerations about the use of these data products, including:

* The data products only cover the area between 60 degrees North and 60 degrees south. Refer to the extent of the tidal wetland probability analysis for the full analysis extent.
* Although the models developed to predict the distribution and change of tidal wetland extent and their component ecosystems, like all remotely sensed datasets there are unavoidable ommission and commission errors. These are described in detail and quantified in the published paper. We recommend any use of the data propagates the errors associated with map uncertainty through any downstream analyses.
* The datasets were developed with careful consideration of the definitions of loss and gain and the scale at which the definitions apply. Please refer to the published paper to best understand what is represented in these data products.
* A minimum mapping unit is applied to the data, please refer to the published paper.
* Please contact the corresponding author of the published paper to request any additional data from the study (such as probability layers for the years between t1 and t7)

#### Data
The datasets generated for this study area available for viewing at the Global Intertidal Change website (http://www.globalintertidalchange.org). 

For analysis, they are made directly available in the Google Earth Engine data catalogue (Murray Global Tidal Wetland Change). 

The dataset are also available as shards from GCP Cloud Storage and can be downloaded using the `gsutil` command  `gsutil -m cp "gs://gic_exports/gic-2019-v1-0/*.tif" "PATH-TO-LOCAL-FOLDER"`

#### Licence
These data products are licensed under a Creative Commons Attribution 4.0 International License. [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/)

#### Further information:
For any further information about this project, code or data please follow the Global Intertidal Change website (http://www.globalintertidalchange.org) or contact nicholas.murray@jcu.edu.au.
