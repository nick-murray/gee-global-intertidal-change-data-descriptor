# Data descriptor for: Murray Global Tidal Wetland Change v1.0 (2022)


#### Citation
Use of any aspect of this study requires full attribution (see licence). 

Please cite the published paper:

Murray, N.J., Worthington, T.A., Bunting, P., Duce, S., Hagger, V., Lovelock, C.E., Lucas, R., Saunders, M.I., Sheaves, M., Spalding, M., Waltham, N.J., Lyons, M.B., 2022. High-resolution mapping of losses and gains of Earth's tidal wetlands. *Science*. 376, 744-749. https://doi.org/10.1126/science.abm9583

#### File description:

This data descriptor describes the Global Intertidal Change data products associated with the paper High-resolution mapping of losses and gains of Earth's tidal wetlands (2022) *Science*. The principal data product is a set of change maps, consisting of 6 raster bands split into single images for publication:

* `"loss", 0-1` - set to 1 for loss locations.
* `"lossYear", 01:19, 3` - integer representing the end year of the time-step of analysis (e.g., 19 = 2017-2019).
* `"lossType, 2,3,5` - integer representing intertidal ecosystem type: Tidal flat (2), Mangrove (3), Tidal marsh (5)).
* `"gain", 0-1` - set to 1 for gain locations.
* `"gainYear",  01:19, 3`  - integer representing the end year of the time-step of analysis (e.g., 19 = 2017-2019).
* `"gainType", 2,3,5` - integer representing intertidal ecosystem type: Tidal flat (2), Mangrove (3), Tidal marsh (5)).

In addition, we provide two images that represent estimated tidal wetland extent:

* `twprobabilityStart, 0-100` - integer which represents the agreement of random forest decision trees for the tidal wetland class in t1 of the analysis, 2001 
* `twprobabilityEnd, 0-100` - integer which represents the agreement of random forest decision trees for the tidal wetland class in t7 of the analysis, 2019 

A full description of the methods, validation, and limitations of the data produced by this software is available in the published paper. For project updates,  frequently asked questions, and Google Earth Engine code examples please refer to the [project website](https://www.globalintertidalchange.org/). 

Code to develop the 6 band change product and two extent bands are available at DOI: 
N. Murray et al., Code for high-resolution mapping of losses and gains of Earth's tidal wetlands v1.0.0 Zenodo (2022) https://doi.org/10.5281/zenodo.5968865

Training data used to develop the extent product is available at DOI: 
N. Murray et al. Intertidal ecosystem training data for mapping Earth's tidal wetlands. Figshare (2022) https://doi.org/10.6084/m9.figshare.19121660

#### User notes and caveates

The high-resolution maps of losses and gains of Earth's tidal wetlands have several known limitations (including commission and omission errors) that are characterised and discussed in detail in the supplementary material of [Murray et al. (2022)](https://doi.org/10.1126/science.abm9583). 

We note three key issues here:

* Any downstream use of these maps should account for data uncertainty and propagate them throughout analyses. Responsible use of spatial data requires propagating known uncertainties, and thus area estimations should not be made directly from the map datasets without reporting associated uncertainty estimates. Many methods are available for this, including probability-sample based (Olofsson et al, 2014) and resample-based (Lyons et al 2018) quantitative approaches. Please refer to supplementary material of Murray et al. (2022) for further information on the source of known uncertainties and the impact they have on the area estimates derived from this product.

* The global intertidal change maps were developed with training data that met strict definitions of intertidal ecosystem type and change (loss, gain and no change) for use at a specific spatial scale. These definitions may not suit the specific needs of other coastal ecosystem monitoring or conservation studies, and we therefore recommend all users to familiarise themselves with the definitions used to develop these maps, as well as the definitions of loss, gain and no change. 

* A minimum mapping unit is applied to the data, please refer to the published paper.

Analyses of these map data should therefore only be conducted with a detailed understanding of appropriate use of the data and careful consideration of uncertainty.


Please see the usage notes on the the Global Intertidal Change website (http://www.globalintertidalchange.org) for further information. 

#### Data
The data generated for this study area available for viewing at the Global Intertidal Change website (http://www.globalintertidalchange.org). 

For analysis, they are made directly available in the Google Earth Engine data catalogue: [Murray Global Tidal Wetland Change v1.0 (1999-2019)](https://developers.google.com/earth-engine/datasets/catalog/JCU_Murray_GIC_global_tidal_wetland_change_2019) using the following code snippet.
`ee.ImageCollection("JCU/Murray/GIC/global_tidal_wetland_change/2019")` 

The data are also available as shards from GCP Cloud Storage and can be downloaded using the `gsutil` command  `gsutil -m cp "gs://gic_exports/gic-2019-v1-0/v1-0-1/*.tif" "PATH-TO-LOCAL-FOLDER"`

#### Licence
These data products are licensed under a Creative Commons Attribution 4.0 International License. [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/)

#### Further information:
For any further information about this project, code or data please follow the Global Intertidal Change website (http://www.globalintertidalchange.org) or contact nicholas.murray@jcu.edu.au.
