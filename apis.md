# Python API's
Because almost all of the above data sources have API's using the SDMX standard, most of the API's can be accessed using the readers provided 
by packages developed by the Pandas team. There are two options. The first is the [pandas-datareader](https://pypi.org/project/pandas-datareader/) package. Pandas datareader provides access to FED, World Bank, OECD, EUROSTAT from the above list. See https://pandas-datareader.readthedocs.io/en/latest/remote_data.html for more data sources. 

The second option is the PandaSDMX package, which allows to read in data from API's using the SDMX format. For more information see https://pandasdmx.readthedocs.io/en/v1.0/ and https://pypi.org/project/pandaSDMX/.  Data sources that are supported are (among others):  EUROSTAT, ECB, IMF, OECD. Note that the disadvantage may be that although every data source accessible through PandaSDMX uses the SDMX format, there may be differences between data providers. See for example here: https://pandasdmx.readthedocs.io/en/latest/sources.html#data-source-limitations. Another thing to mention is that probably PandaSDMX is a bit more involved as it requires the user to specify elements of queries manually. So this basically means that the user should know something about the way the actual API is structured. 


| Data Source  | Package name                                                                                                                                                                         |
|:------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| CBS          | [cbsodata](https://pypi.org/project/cbsodata/)                                                                                                                                       |
| OECD         | NA                                                                                                                                                                                   |
| FED          | [FRB](https://pypi.org/project/FRB/), [datapungi_fed](https://pypi.org/project/datapungi_fed/), [fredapi](https://pypi.org/project/fredapi/), [fred](https://pypi.org/project/fred/) |
| IMF          | [datapungi_imf](https://pypi.org/project/datapungi_imf/)                                                                                                                             |
| EUROSTAT     | [eurostat](https://pypi.org/project/eurostat/)                                                                                                                                       |
| ECB (PUBLIC) | NA                                                                                                                                                                                   |
| WORLDBANK    | [wbdata](https://pypi.org/project/wbdata/), [wbpy](https://pypi.org/project/wbpy/), [world-bank-data](https://pypi.org/project/world-bank-data/)                                     |
| WTO          | [wto](https://pypi.org/project/wto/)                                                                                                                                                 |
| GLEIF        | [pygleif](https://pypi.org/project/pygleif/), [leipy](https://pypi.org/project/leipy/)                                                                                               |
| EUREX        | NA                                                                                                                                                                                   |
                                                                                                                                                                                                                    

# R API's
Because almost all of the above data sources have API's using the SDMX standard, most of the API's can be accessed using packages that support SDMX format. Two R packages that can be used for reading SDMX format are [readsdmx](https://cran.r-project.org/web/packages/readsdmx/index.html) and [rsdmx](https://cran.r-project.org/web/packages/rsdmx/index.html). 


|  Data Source | Package name                                                                   |  
|:------------:|:------------------------------------------------------------------------------:|
| CBS          | [cbsodataR](https://cran.r-project.org/web/packages/cbsodataR/cbsodataR.pdf)   |
| OECD         | [OECD](https://cran.r-project.org/web/packages/OECD/index.html)                |         
| FED          | [fredr](https://www.rdocumentation.org/packages/fredr/versions/0.1)            |       
| IMF          | [imfr](https://cran.r-project.org/web/packages/imfr/imfr.pdf)                  |           
| EUROSTAT     | [eurostat](https://cran.r-project.org/web/packages/eurostat/index.html)        |      
| ECB (PUBLIC) | [ecb](https://cran.r-project.org/web/packages/ecb/index.html)                  |           
| WORLDBANK    | [WDI](https://cran.r-project.org/web/packages/WDI/WDI.pdf)                     |              
| WTO          | NA                                                                             |
| GLEIF        | NA                                                                             |                                                                 
| EUREX        | NA                                                                             |                                                                 
