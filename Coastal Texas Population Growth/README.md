# Coastal Texas Population Projections, 2050

This file contains population growth projections for coastal Texas, taken from a Hoque et al. (2014). I copied the variables manually into a csv, cleaned the data using R, and exported this csv file.

## Variables

**county**: The county name. These are coastal counties as [defined by NOAA](https://www.census.gov/geo/landview/lv6help/coastal_cty.pdf) and include "counties that meet one of the following criteria: 1) at least 15 percent of a county’s total land area is located within the Nation’s coastal watershed; or 2) a portion of or an entire county accounts for at least 15 percent of a coastal cataloging unit."

**coastline**: Whether or not the county actually has any coastline

**population_2010**: The population in 2010, per Hoque et al. (2014)

**no_migration**: The estimated population size in the year 2050, assuming no net migration. This estimate is based on demographic trends alone.

**same_migration**: The estimated population size in the year 2050, assuming the same rate of migration as was seen in 2000–2010.

**percent_growth_no_migration**: The percentage growth in population size by 2050 under the no migration scenario, rounded to the nearest tenth of a percent. Numbers less than 100 represent a net loss in population, numbers greater than 100 represent a net gain in population.

**percent_growth_same_migration**: The percentage growth in population size by 2050 under the unchanged migration rate scenario, rounded to the nearest tenth of a percent. Numbers less than 100 represent a net loss in population, numbers greater than 100 represent a net gain in population.

**percent_change_no_migration**: The change in population size by 2050 under the no migration scenario expressed as a percentage gained or lost, rounded to the nearest tenth of a percent.

**percent_change_same_migration**: The change in population size by 2050 under the unchanged migration scenario expressed as a percentage gained or lost, rounded to the nearest tenth of a percent.

**net_gain_no_migration**: The change in population size by 2050 under the no migration scenario expressed as number of people gained or lost.

**net_gain_same_migration**: The change in population size by 2050 under the unchanged migration scenario expressed as number of people gained or lost.

## Reference
Hoque, M. N., McNeil, C., and J. Granato. 2014. *Projections of the Population of Texas and Counties in Texas by Age, Sex, and Race/Ethnicity from 2010 to 2050*. University of Houston Hobby Center for Public Policy. Accessed January 20, 2017 at [http://www.uh.edu/class/hobby/_docs/research/population/2014%20PPRLE-SV2.pdf](http://www.uh.edu/class/hobby/_docs/research/population/2014%20PPRLE-SV2.pdf).