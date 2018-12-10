# NSNSD Virtual Environments
A repository to implement versioning of Python virtual environments for specific NPS Natural Sounds and Night Skies Division software tools. The Anaconda `.yml` files  included here allow for rapid creation of identical environments - which will allow smoother, more coordinated use of our tools by many users. 

## NSNSDgeo

A Python 2.7, 64-bit geoprocessing environment that includes `gdal` and `rasterio`

## soundDB

A Python 3.5, 64-bit environment that includes `soundDB` and `iyore`. Keeps `pandas=0.19` to utilize `pandas.Panel4D` objects.

## NightSkies

A Python 2.7, 32-bit environment. *Note: this environment currently requires a separate install of 32-bit Anaconda, and can benefit from Windows batch files to toggle the path environment variable cleanly.* 

## arcpy

A Python 2.7, 64-bit environment that includes `arcpy`. *Note: may require further revisions for full compatability.*
