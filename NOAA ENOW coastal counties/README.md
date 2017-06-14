# NOAA ENOW Coastal County List

This file contains a list of coastal counties as defined in the NOAA Economics: National Ocean Watch (ENOW) dataset. I downloaded the large dataset from https://coast.noaa.gov/dataregistry and performed a very simple cleanup in R:

    library(tidyverse)
    coastal_counties_cleaned <- coastal_counties %>% 
      filter(GeoScale == "County") %>% 
      select(GeoID, GeoName, StateAbbrv) %>% 
      distinct(GeoID, .keep_all = TRUE) %>% 
      rename(FIPS = GeoID,
             county = GeoName,
             state = StateAbbrv
             )
         

## Variables

**FIPS**: The [FIPS county code](https://en.wikipedia.org/wiki/FIPS_county_code).

**county**: The name of the county.

**state**: The [2-letter state postal abbreviation.](https://en.wikipedia.org/wiki/List_of_U.S._state_abbreviations)