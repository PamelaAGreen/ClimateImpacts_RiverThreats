
<b>Climate Impacts on Water Security Threats and Green/Gray Infrastructure Threat Reduction Capacity</b>

Title: Climate Impacts on Water Security Threats and Green/Gray Infrastructure Threat Reduction Capacity Author: Pamela A. Green
Date: February 13, 2023

This code has been modified from original code developed between March 11 and December 31, 2022 by Pamela Green, Senior Research Associate, CUNY Advanced Science Research Center, New York, NY. Code has been updated to be generically applicable to any raster water balance model output although end user will need to ensure all raster data are in a consistent resolution and projection.

The following global data for River Threats and Green/Gray Engineering Threat Rediction Capacity were downloaded from https://www.water-sustainable-infrastructure.com/index.html and downscaled to 6-minute resolution.

Green-Gray water threat indicators from Vörösmarty et al 2021

    Ti: Incident threat (for years 2000, 2030, 2050, 2080)
    TRnat: Threat reduced by existing natural capital (for years 2000, 2030, 2050, 2080)
    TReng: Threat reduced by engineering (for years 2000, 2030, 2050, 2080)

Vörösmarty, Charles J., Ben Stewart-Koster, Pamela A. Green, Edward L. Boone, Martina Flörke, Günther Fischer, David A. Wiberg, et al. “A Green-Gray Path to Global Water Security and Sustainable Infrastructure.” Global Environmental Change 70 (September 1, 2021): 102344. https://doi.org/10.1016/j.gloenvcha.2021.102344.

TerraClimate multi-decadal climate forecasts for contemporary and future climate conditions were downloaded via the TerraClimate website and downscaled to 6-minute using the Jupyter Notebook script TerraClimate_Downscaling_Runoff+Discharge.ipynb in the WaterBalanceModel_TimeSeries repository located at https://github.com/PamelaAGreen/WaterBalanceModel_TimeSeries.

    Contemporary (Runoff, Precipitation, actual Evapotranspiration, monthly totals), units = mm, years 1985-2015
    +2C Climate Futures (Precipitation, actual Evapotranspiration, monthly totals), units = mm, years 1985-2015
    +4C Climate Futures (Precipitation, actual Evapotranspiration, monthly totals), units = mm, years 1985-2015

Qin, Y., Abatzoglou, J.T., Siebert, S. et al. Agricultural risks from changing snowmelt. Nat. Clim. Chang. 10, 459–465 (2020). https://doi.org/10.1038/s41558-020-0746-8.

Contemporary and Future Climate:

Contemporary and future Climate Variability indicators, ClimVarcontemp and ClimVarfuture, were developed using intra- and inter annual variability in available water resources from the TerraClimate multi-decadal discharge flow datasets. The ClimVarcontemp and ClimVarfuture indicators are ranked on a continuous 0-1 scale of low to high climate variability threat identifying areas most vulnerable to large shifts in water availability due to seasonality (intra-annual) and longer term (30-year inter-annual) climate patterns.

Datasets produced:

    ClimVarcontemp : Global gridded 6-min resolution climate variability indicator scores ranked 0-1 for contemporary time period
    ClimVarfuture+2C : Global gridded 6-min resolution climate variability indicator scores ranked 0-1 for future (2080, +2C climate run) time period
    ClimVarfuture+4C : Global gridded 6-min resolution climate variability indicator scores ranked 0-1 for future (2080, +4C climate run) time period

Population and Downstream Population for contemporary and future years downloaded via CIESIN website and processed via routing algorithms using the CUNY WBM RGIS system.

Contemporary Population (2020):

    Center for International Earth Science Information Network - CIESIN - Columbia University. 2018. Gridded Population of the World, Version 4 (GPWv4): Population Density, Revision 11. Palisades, NY: NASA Socioeconomic Data and Applications Center (SEDAC).

Future Population (2030, 2050, 2080):

    Gao, J. 2020. Global 1-km Downscaled Population Base Year and Projection Grids Based on the Shared Socioeconomic Pathways, Revision 01. Palisades, New York: NASA Socioeconomic Data and Applications Center (SEDAC). https://doi.org/10.7927/q7z9-9r69. Accessed April 2022

All datasets listed above have been resampled from their native formats to 6-minute resolution GeoTIFF raster format using a standard reprojection and warping utility (GDAL Warp). Reprojected climate forcing data from TerraClimate were converted to 6-minute resolution discharge flow via routing algorithms using the CUNY WBM RGIS system.

Water Threat and Threat Reduction Impact Indicators:

The contemporary and future Climate Variability indicators (ClimVarcontemp and ClimVarfuture) were applied to the human water security and green-gray water threat indicator from Vörösmarty et al 2021 (Ti, TRnat, TReng) to create indicators measuring the impact of climate variability on (a) human water security threat (Climate Impacted Ti), (b) green infrastructure condition (Climate Impacted TRnat), and (c) gray infrastructure condition (Climate Impacted TReng) for contemporary and future (year 2080, +2C and +4C climate run) conditions. These indicators were ranked on a continuous 0-1 scale of low to high threats and threat reduction capacity.

Datasets produced:

    Climate Impacted Ticontemp : Global gridded 6-min resolution indicator scores measuring water security threats impacted by climate variability, ranked 0-1 for contemporary time period
    Climate Impacted Tifuture+2C: Global gridded 6-min resolution indicator scores measuring water security threats impacted by climate variability, ranked 0-1 for future (2080, +2C climate run) time period
    Climate Impacted Tifuture+4C: Global gridded 6-min resolution indicator scores measuring water security threats impacted by climate variability, ranked 0-1 for future (2080, +4C climate run) time period
    Climate Impacted TRnatcontemp: Global gridded 6-min resolution indicator scores measuring threat reduction by natural capital impacted by climate variability, ranked 0-1 for contemporary time period
    Climate Impacted TRnatfuture+2C: Global gridded 6-min resolution indicator scores measuring threat reduction by natural capital impacted by climate variability, ranked 0-1 for future (2080, +2C climate run) time period
    Climate Impacted TRnatfuture+4C: Global gridded 6-min resolution indicator scores measuring threat reduction by natural capital impacted by climate variability, ranked 0-1 for future (2080, +4C climate run) time period
    Climate Impacted TRengcontemp: Global gridded 6-min resolution indicator scores measuring threat reduction by engineering impacted by climate variability, ranked 0-1 for contemporary time period
    Climate Impacted TRengfuture+2C: Global gridded 6-min resolution indicator scores measuring threat reduction by engineering impacted by climate variability, ranked 0-1 for future (2080, +2C climate run) time period
    Climate Impacted TRengfuture+4C: Global gridded 6-min resolution indicator scores measuring threat reduction by engineering impacted by climate variability, ranked 0-1 for future (2080, +4C climate run) time period

Casting Water Flow, Threats and Threat Reduction in Terms of Water Resource Areas Supporting Downstream Populations

We use the contemporary and future Climate Impacted Ticontemp/future , Climate Impacted TRnatcontemp/future and Climate Impacted TRengcontemp/future described above to map population downstream of water source areas under the four climate impacts. We map the geography of population downstream of water source areas under low, moderate, and high scores for each of the indicators under contemporary and year 2080 (+2C and +4C) conditions.

The following steps were carried out to develop the indicators for this analysis:

    Aggregating Monthly Data to Annual values
    Creating Coefficient of Variation for Annual TerraClimate Discharge
    Creating Coefficient of Variation for Monthly TerraClimate Discharge (LTM and for each year)
    Created CDF of Annual and Monthly CVs, Inter- and Intra- Annual variability indicators
    Combine Inter- and Intra- Annual variability indicators into single Climate Vulnerability indicator
    Calculate Adjusted Water Threat and Threat reduction indicators by applying Climate Vulnerability Indicator
    Apply CDF calculation to Adjusted Water Threat and Threat Reduction indicators
    Calculate downstream population under adjusted CV, Ti, TRnat and TReng for 2020 and future year
    Overlay Extremely Dry and Extremely Wet Drought Analysis with results
    Aggregate to global, continental, and administrative unit levels

