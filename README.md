# Oceanhack

Copernicus OceanHack is funded by the EU’s Copernicus Programme and has been organised through a partnership of EUMETSAT, the Copernicus Marine Environment Service, and the Estonian Environment Agency.

The event is a one-of-a-kind gathering of data scientists, web/app developers, UX and UI designers, visionaries/space enthusiasts, marketing wizards and business developers, project managers and field experts to create solutions to 
problems that currently affect the Baltic Sea, and beyond to help people in their daily lives in this beautiful region. 

More info at

http://garage48.org/events/copernicus-oceanhack

![EventBanner](https://github.com/wekeo/Oceanhack/blob/master/coverocean.jpg)

 # Table of contents
1. [Challenge](#challenge)
2. [Dataset offering](#datasets)  
3. [Platform offering](#platform)
4. [Solution Domains](#solution)
5. [Background](#bg)
6. [Data Access](#data)
7. [Useful Links](#useful)

# Challenge: Hack the Atmosphere! <a name="challenge"></a>
Urban air pollution poses a significant threat to human health and the quality of life of millions of people worldwide. Nine out of ten people are estimated to breathe air containing high levels of pollutants, causing around 7 million deaths every year. More than 90% of air pollution-related deaths occur in the developing world. Many of these areas have no surface air-quality monitoring networks and rely mainly on modelling and satellite information. Besides air pollution, there are other aspects of atmospheric composition that can affect health: UV radiation, which strongly depends on the stratospheric ozone layer, is another example.
Urban air pollution poses a significant threat to human health and the quality of life of millions of people worldwide. Nine out of ten people are estimated to breathe air containing high levels of pollutants, causing around 7 million deaths every year. More than 90% of air pollution-related deaths occur in the developing world. Many of these areas have no surface air-quality monitoring networks and rely mainly on modelling and satellite information. 

Your challenge is to create solutions that help people in their daily lives to reduce their exposure to pollutants and UV radiation. To solve this challenge, you are encouraged to use Copernicus atmospheric monitoring data.

Various approaches are welcome: Create new solutions or add atmosphere-smart features to existing solutions. Propose innovative data visualisations for academic purposes or for raising awareness around the atmospheric environment. Mobile, web apps, platforms or hardware - it’s your call how to improve the quality of life for many!

### Dataset offering <a name="datasets"></a>
An overview of the complete set of datasets available for this event is listed below

|  Product | Source | Used for   | Geo Coverage  | Time Coverage   |  Resolution |  Format | HTTP Access  |
| ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ | ------------ |
|PMAP Aerosol Optical Depth - particles in the atmosphere | Metop | Air pollution (basis for PM10, PM2.5 etc) | Global | April 2016 - onwards.  Aim 2017 onwards. (14 per day). January 2017 until December 2017 | 5x40km and 10x40km | NetCDF | [GOME-PMAP](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=01-GOME_PMAP)|
|NO2, Aerosols Index | Metop GOME-2 and IASI | Air pollution monitoring, volcanic eruptions, forest fires | Global | 2016 onwards | 40x80km | NetCDF/ HDF5 | [Aerosols-Index](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=07-Aerosols_Index/) |
| NO2, CO, O3 |	Sentinel-5p Tropomi	| Air pollution monitoring | Global	| July 2018 onwards | 5x5km and 7x5km | NetCDF |  [Sentinel-5P](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=03-Sentinel_5p-Tropomi/) |
|UV index (corrected for clouds with ECMWF data) | Metop (AC SAF) | UV - risk of harm | Global | June 2007 until May 2017 | 250 x 250 | PNG/HDF5 | [UV-Index](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=02-UV_Index-AC_SAF/)|
|Dust RGB |	Meteosat Second Generation (geo orbit) | Dust storms - health and transport problems |Atlantic and Indian Ocean	| Available from 28th September 2018 | 4km | GeoTiff/ PNG | [Dust-RGB](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=04-Meteosat-Dust_RGB) |
|Ash RGB | Meteosat Second Generation (geo orbit) |	Volcanic ash - aviation, health etc. | Atlantic and Indian Ocean | Available from 28th September 2018 | 4km | GeoTiff/ PNG | [Ash-RGB](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=05-Meteosat-Ash_RGB)|
| SmartSMEAR Aerosols, gases, meteo, fluxes, soil,... | SMEAR |	Research | Finland |	1996 onwards depending on station and measured parameter | Point observations, no geospatial data | txt/csv, hdf5 | <a href="https://avaa.tdata.fi/web/smart/smear/api" target="_blank">SmartSMEAR</a>|
|Regional forecasts/ analyses of PM, O3, NO2, SO2 | CAMS | European air pollution | Europe | 2018 | Point data (as used in Euronews air quality forecasts), gridded data @ ~10km	| CSV ([details](https://github.com/OpenDataHack2018/Available-Open-Data/blob/master/CAMS-regional-air-quality.md), NetCDF (gridded data) | [Air-Pollution](http://atmoshack.obs.eu-de.otc.t-systems.com/?prefix=06-CAMS-AirPollution)|
|Global total ozone column | CAMS |	Total ozone columns | Global | 2003-present. Reanalysis from 2003 until 2016 | ~40km | NetCDF, GRIB |[CAMS Reanalysis data](https://confluence.ecmwf.int/display/CKB/How+to+download+the+CAMS+Reanalysis+data+via+the+ECMWF+Web+API)|
|Global ozone (Metop GOME-2 instrument)| EUMETSAT/DLR |	Ozone O3, nitrogen dioxide NO2 and sulphur dioxide SO2 | Global | Daily | - | WMS |[Latest](https://geoservice.dlr.de/web/maps/metop:gome2.tc.latest), [Daily](https://geoservice.dlr.de/web/maps/metop:gome2.tc.daily)|
|Global UV forecasts | CAMS | UV index | Global | 2003-present. NRT from 2016 June onwards, Reanalysis from 2003 to 2016 |~40km	| NetCDF | [CAMS](https://atmosphere.copernicus.eu/) |
|Global fire emissions | CAMS |	Wildland fire emission estimates | Global |	2003-present | ~10km | NetCDF | [CAMS](https://atmosphere.copernicus.eu/) |
|Air Quality stations | European Environmental Agency | NO2, O3, PM10, PM2.5, CO - additional depending on countries | Europe |       2013-present | in-situ | CSV | [EEA Airbase website](http://discomap.eea.europa.eu/map/fme/AirQualityExport.htm) |
|Sentinel_5p Monthly maps | Temis Service | NO2 | Global |  02/2018-present | 0,125 degrees | ascii | [Temis KNMI website](http://temis.nl/airpollution/no2col/no2month_tropomi.php) |


### Platform offering <a name="platform"></a>
WEkEO platform [wekeo.eu](https://www.wekeo.eu/) provides access to Copernicus datasets and cloud based processing resources. Get to know the capabilities of WEkEO from [here](https://www.wekeo.eu)

You will be offered VM access by participating on the Oceanhack [here](https://www.wekeo.eu/advanced_user)


### Useful Links <a name="useful"></a>

[How to Visualize NetCDF data - YouTube Video](https://www.youtube.com/watch?v=XqoetylQAIY)

CAMS: https://atmosphere.copernicus.eu/

Example notebook: https://gist.github.com/erget/467dba7082d31d73b20f3b5e90e740af

GDAL: http://www.gdal.org/

Jupyter: https://jupyter.org/

Scipy stack, including matplotlib and numpy: https://www.scipy.org/

Info on netCDF tool: https://www.unidata.ucar.edu/software/netcdf/

QGIS: https://www.qgis.org/en/site/

Xarray: http://xarray.pydata.org/en/stable/

Scitools: https://scitools.org.uk/
