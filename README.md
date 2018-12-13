# NSNSD Virtual Environments
A repository to implement versioning of Python virtual environments for specific NPS Natural Sounds and Night Skies Division software tools. The Anaconda `.yml` files  included here allow for rapid creation of identical environments - which will allow smoother, more coordinated use of our tools by many users. 

In order to successfully create these environments, you will need to [download the DOI root certificate to your machine](https://drive.google.com/file/d/0B551gy_Kqih1Y202VlFubnJPcFU/view). Then, tell Anaconda where the certificate is located:

```
>conda config --set ssl_verify "path to DOI root certificate"
```

[More information on secure socket layer encryption.](https://github.com/dbetchkal/soundDB/blob/master/PREREQUISITES.md#sidebar-the-government-is-decrypting-your-secure-internet-connection)

Once python has permissions to access the internet, you can create the virtual environment using the following command:

```
>conda env create -n EnvironmentNameHere -f "path to .yml file"
```


-----

## The Virtual Environments

### NSNSDgeo

A Python 2.7, 64-bit geoprocessing environment that includes `gdal` and `rasterio`

### soundDB

A Python 3.5, 64-bit environment that includes `soundDB` and `iyore`. Keeps `pandas=0.19` to utilize `pandas.Panel4D` objects.

Projects include:

- [rapid access to acoustical metrics, `derivedDataFunctions`](https://github.com/dbetchkal/derivedDataFunctions)
- [loading and parsing data using metadata filters, `metaDig` (*in development*)](https://github.com/dbetchkal/metaDig)

### NightSkies

A Python 2.7, 32-bit environment. *Note: this environment currently requires a separate install of 32-bit Anaconda, and can benefit from Windows batch files to toggle the path environment variable cleanly.* 

Projects include:

- [NSNSD Night Skies CCD Camera Data Reduction Pipeline, `nightskies`](https://github.com/liweihung/nightskies)

### arcpy

A Python 2.7, 64-bit environment that includes `arcpy`. *Note: may require further revisions for full compatability.*

Projects include:

- [DENA Flight Track Data Reduction, `flightsounds`](https://github.com/dan-walsh/flightsounds)
