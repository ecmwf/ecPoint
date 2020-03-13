# ecPoint

## Project Overview
ecPoint is a post-processing system that uses conditional verification concepts to compare NWP model outputs against point observations, and thereby anticipate weather-dependant sub-grid variability and biases at grid scale.  
The main ecPoint outputs are provided in grib files and consist of:
1. bias corrected rainfall forecasts at point scale (probabilistic forecast, provided in the form of percentiles).
2. bias corrected rainfall forecasts at grid scale (quatitative, in mm, with the same number of members as the raw ensemble).
3. diagnosed "weather type" indicators (provided for each ensemble member, for each grid box).

## Repository Content
1. ecPoint code (written in an ECMWF proprietary language called "Metview")
2. Calibration "mapping function" files (computed using [ecPoint-Calibrate](https://github.com/esowc/ecPoint-Calibrate/tree/master))

## Getting Started

### Prerequisites

**Metview**   
Information about Metview and how to install it can be found [here](https://confluence.ecmwf.int/display/METV/Metview) and in the [Metview-Python GitHub](https://github.com/ecmwf/metview-python) repository. 
Versions from Metview 5 are required.

**Test Data**  
Before running ecPoint, the user might want to download the test data, available from Zenodo at the following link: 10.5281/zenodo.3708501

### Running ecPoint (in series)
```sh
$ vi InParam.mv # Modify the input parameters as needed
$ metview -b ecPoint.mv # execute code in batch mode
```
N.B: depending on the chosen settings, ecPoint might take a long time to run in series. In such a case, the user might consider parallel running.

## Versioning
ecPoint uses the [SemVer](https://semver.org/) standard for versioning. The available ecPoint versions are provided [here](https://github.com/ecmwf/ecPoint/releases).
