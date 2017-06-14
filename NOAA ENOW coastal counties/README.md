# NOAA ENOW Coastal County List

This file contains a list of coastal counties as defined in the NOAA Economics: National Ocean Watch (ENOW) dataset. These are coastal counties that meet the following 2 criteria:

1. They have a coastline bordering the open ocean or the Great Lakes or
2. The contain coastal high hazard areas (V-zones)

In addition, ENOW made the two changes to the dataset:
1. Removed counties with no relevant economic activity
2. Added counties that are not shore-adjacent but do have significant levels of ocean/Great Lakes-dependent economic activity.

I downloaded the large dataset from https://coast.noaa.gov/dataregistry and performed a very simple cleanup in R, removing extraneous columns and filtering out three counties in Alaska that no longer exist:

    library(tidyverse)
    coastal_counties_cleaned <- coastal_counties %>% 
      filter(GeoScale == "County") %>% 
      select(GeoID, GeoName, StateAbbrv) %>% 
      distinct(GeoID, .keep_all = TRUE) %>% 
      rename(FIPS = GeoID,
             county = GeoName,
             state = StateAbbrv) %>%
      filter(FIPS != 02201,
             FIPS != 02232,
             FIPS != 02280
             ) 
         

## Variables

**FIPS**: The [FIPS county code](https://en.wikipedia.org/wiki/FIPS_county_code).

**county**: The name of the county.

**state**: The [2-letter state postal abbreviation.](https://en.wikipedia.org/wiki/List_of_U.S._state_abbreviations)