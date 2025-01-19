*** This page has sat in private mode for a year, waiting for me to get around to finishing it. I still haven't found a moment yet, but I figure it's better made public in its half finished form, and one day I'll get around to adding the other things I want to add! Find similarly half baked bits of useful things at my Github (mostly in the "Useful Functions" repo, it's mostly spatial stuff)***

​

For a long time I've been meaning to make a page which pulls together various resources (mostly spatial datasets), that I often have cause to access, but forget where to find them. I figure it may be useful for others to also have things collected in one place. This is very much NOT a comprehensive list, nor is it an expression of endorsement for the datasets (though I have used most things listed here). Additions very welcome, send me an email! (Also please let me know if you discover any dead links).

​​

I've vaguely grouped datasets into the following:

Climate Datasets

Land Use & Human Impact Datasets

Polar & Ice

**Climate Datasets**

Climate data can roughly be split into observed (anything we have measured, typically from the 1950s-ish until now), and modelled (either projections of future climate, or models of past climate if we go back further than what we have observations for). All the following data are given in rasters - where the world is divided into grid cells, and a value is given for the each grid cell.



For observed data, observations from weather stations will be combined with models to give estimates for every grid cell across the Earth. This means we have a less confidence in areas with few weather stations (e.g. polar regions), because there are less weather stations to calibrate against.

​

Modelled data are based on General Circulation Models (GCMs) - complex models of the Earth's climate systems. Many teams around the world have built GCMs, meaning there is no one dataset for past and future predictions. Future projections of climate change are all gathered together into something called the Coupled Model Intercomparison Project (CMIP), which compares and summarises the different GCMs. We're currently under CMIP6 - i.e. the 6th phase of the project. CMIP also defines different future 'scenarios' - under different assumptions of how the Earth may warm, mostly based on how well we get our act together and curb greenhouse gas emissions. Under CMIP5 these were called Representative Concentration Pathways (RCPs), with RCP2.6 being a best case scenario and RCP8.5 being a worst case scenario. Under CMIP6 they're now called Shared Socioeconomic Pathways (SSPs), and there are 5 of them, that confusingly aren't numbered to go from best to worst case scenarios. 

​

In addition to standard variables like mean average temperature, annual rainfall, etc, a few of these sources include bioclimatic variables ("bioclim"). These are 19 variables first introduced by Hijmans et al, that were chosen to represent a range of biologically relevant factors. For instance, some of the bioclim variables are coldest temperature of the coldest quarter, seasonal variation in temperature, total rainfall of the driest quarter, etc.

*WorldClim*

TIME PERIOD: 1950 - 2100

TEMPORAL RES: Monthly OR 50yr average (observed), 20 years (future, CMIP6)

​

SPATIAL COVERAGE: Global

SPATIAL RES: 30 seconds (~1km2) to 10 minutes (~18x18km)

​

This is the most commonly used climate data for ecologists (as far as I know). WorldClim offers averaged data from 1950-2000 ("historical"), data for each month from 1960-2018 ("historical monthly") as well as future projections at 20 year averages: 2021-2040, 241-2060, 2061-2080, 2081-2100 ("future"). All of these are offered for a range of variables, and at a range of spatial resolutions. Future data is offered for 25 CMIP6 models and 4 SSPs - it's comprehensive!

​

The older version of WorldClim also offered paleoclimate data at two time steps - the Mid-Holocene (~6000 years ago) and the Last Glacial Maximum (~24,000 years ago), for 10 and 4 CMIP5 models (respectively). But they've stopped this in the latest version, and there are typically better data available (see below).

*Chelsa*

TIME PERIOD: 1980 - 2100

TEMPORAL RES: Monthly (observed), 30 year (future, CMIP6)

​

SPATIAL COVERAGE: Global

SPATIAL RES: 30 seconds (~1km2)

​

CHELSA can be viewed as an alternative to WorldClim, that possibly has more accurate precipitation estimates. It's not quite as user friendly, and doesn't provide future data for as many CMIP6 models as WorldClim does, but otherwise is fairly comparable. It also has excellent paleodata availability (see below).

​

Current data can be downloaded here, and CMIP6 future data here (the main website is a bit behind and "future" takes you to CMIP5 [at the time of writing this, Nov 2022]). Some of these files are available as netcdf, see here for some tips + code on how to read this in. 

*Paleoview*

TIME PERIOD: 21,000 years before present - 1950

TEMPORAL RES: Down to 20 years



SPATIAL COVERAGE: Global

SPATIAL RES: 2.5° (~275x275km)

​

This is very high temporal resolution paleoclimate data (down to 20 year time steps), as modelled from one climate model (CCSM3). The spatial resolution is quite coarse however - 275x275km grid cells. The data team have provider an app to download their data where you can choose the temporal resolution you want (i.e. what they will average the climate data over).

​

The data is only offered for general climate variables, not bioclim variables - though you can calculate these yourself. You can also spatially downscale the climate data yourself if you want, though it's a bit of a faff.

​

Download the latest version from GitHub here.

*Chelsa TRACE21k*

TIME PERIOD: 21,000 years before present - 1990

TEMPORAL RES: 100 years

​

SPATIAL COVERAGE: Global

SPATIAL RES: 30 seconds (~1km2)

​

The addition to the CHELSA dataset (above) that covers the time since the Last Glacial Maximum. Its at a high temporal resolution (100 year time steps), and at a much higher spatial resolution than PaleoView. Like PaleoView, it's based off the CCSM3 GCM, but it is also coupled to an ice-sheet model which (I think) improves its accuracy. 

*Beyer et al 2020*

TIME PERIOD: 120,000 years before present - 2000 

TEMPORAL RES: 2000 years (120,000 - 22,000ybp), 1000 years (22,000ybp - now)

​

SPATIAL COVERAGE: Global

SPATIAL RES: 0.5° (~55x55km)

​

Though at a lower temporal resolution, this dataset goes back much further in time than the previous two. It also includes cloud cover, and some land use estimates such as biome, net primary productivity, and leaf area index. It's downloadable as one netcdf, use this function to extract what you want.

*Kaufman*

*Shakun*

**Land use and human presence**

These datasets all capture aspects of how humans have impacted the Earth's surface, or how strong human presence is. 

*HYDE*

TIME PERIOD: 10,000 BCE (i.e. ~12,000 years before present) - 2015

TEMPORAL RES: 1000 years to 0AD (i.e. 2000 years ago), 100 years to 1700, 10 years to 2000, 1 year to 2015

​

SPATIAL COVERAGE: Global

SPATIAL RES: 5 minutes (~10x10km)

​

History database of the Global Environment (or HYDE) is a dataset that covers land-use across the Earth according to a range of metrics. It's currently [as of Nov 2022] on version 3.2 (downloadable here - the read me file is great). As a summary of human impact, you can download "anthrome" layers, where each gridcell is a categorical value that ranges from urban through village to wild. You can also download layers where each gridcell is a numeric value representing the proportion of land in the cell that is different types of farmland, or where the value represents the amount of built up area, or the total population in the grid cell. 

*KK10*

TIME PERIOD: 8000 years before present - 1850

TEMPORAL RES: Yearly

​

SPATIAL COVERAGE: Global

SPATIAL RES: 5 minutes (~10x10km)

​

This is an alternative dataset to HYDE that has much higher temporal resolution, but less available variables. It also, as far as I can tell, hasn't been updated since its initial release. Impressively, the authors of HYDE and KK10 released a paper together comparing their models, generally KK10 has higher estimates of human land use than HYDE - it's very difficult to verify which is more accurate (though this is a fun paper that I've only skim read that uses pollen records and seems to indicate that they better match the spatial patterns of KK10, but the land use intensity of HYDE).

*Worldpop*

*Human foorprint*
