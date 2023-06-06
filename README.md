# Forest loss computation with Google Earth Engine
Project assignment for the course "Introduction to Google Earth Engine for Advanced Geospatial Analysis" at Politecnico di Milano.

This project is made up of three different scripts that use the [Global Forest Change dataset](https://data.globalforestwatch.org/documents/a400422d410b4c158f499b5dbf7a7c66/explore) and the [Global forest loss due to fire dataset](https://glad.umd.edu/dataset/Fire_GFL).

## [find_most_deforestation](https://code.earthengine.google.com/78312fa0c5709f37baec3de396a14477)
This script computes the total forest loss in a given year in each GAUL level 2 administrative regions, and put the results in a csv file.
By uncommenting the ***forest loss due to fire*** block it is possible to filter out all the area of forest loss that was caused by forest fires in the given year.<br>
***IMPORTANT***: The computation can take a long time (up to one hour). The resulting csv files are provided in this repository.

## [compute_deforestation](https://code.earthengine.google.com/8a2e226cddf49c092b171f991aec8aed)
This script is the actual project assigned by the professors. It analyzes the forest loss of the Cordillera region (Bolivia) in 2021.<br>
It computes:
- Forest loss:
  - The forest area of the region in the year 2000
  - The total forest loss in the region from the year 2000 up untill 2022
  - The forest loss in the region in year 2021
  - The percentage of forest loss that happened in 2021
  - The by-weekly NDVI time series of a manually created area of interest
- Forest fires:
  - The forest loss in the region in the year 2021 that was caused by forest fires
  - The percentage of forest loss in the year 2021 that was caused by forest fires

## [generic_forest_loss](https://code.earthengine.google.com/c0713001f5ecf93b82ca3ae48a397e9e)
This script is a generalization of _compute_deforestation_. 
By editing the ***Input Variables*** block it is possible to select the area of interest and the year of interest to analyze.
