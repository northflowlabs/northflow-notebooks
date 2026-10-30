<a href="https://northflow.no"><img src=".github/assets/northflow-mark.svg" alt="Northflow" width="40" height="40"></a>

# Northflow notebooks

Reproducible climate validation notebooks built on climval. Every notebook reads real data from public sources, with no account needed, and every figure comes from that data.

[Research page](https://research.northflow.no/systems/climval) · [climval](https://github.com/northflowlabs/climval) · [Licence](#licence)

[![Licence: Apache 2.0](https://img.shields.io/badge/licence-Apache%202.0-0e6b63)](LICENSE)

## Notebooks

| Run | Notebook | Description | Stack |
|-----|----------|-------------|-------|
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/era5_station_validation.ipynb) | [**groundtruth**: ERA5 Station Validation](notebooks/era5_station_validation.ipynb) | ERA5 from the NSF NCAR archive against measured Meteostat station hours, daily means of local days, 2 January 2019 to 30 December 2020, in Oslo, Madrid, Nairobi, Toronto and Sydney | `climval` · `xarray` · `meteostat` · `s3fs` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/cmip6_taylor_diagram.ipynb) | [**cmip6-taylor**: CMIP6 Multi-Model Intercomparison](notebooks/cmip6_taylor_diagram.ipynb) | Five CMIP6 historical runs from the Pangeo catalog against ARCO-ERA5, area-weighted monthly climatology, 1985 to 2014, Europe, 36N to 72N | `climval` · `xarray` · `gcsfs` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/sentinel3_lst_validation.ipynb) | [**sentinel3-lst**: Sentinel-3 SLSTR LST Comparison](notebooks/sentinel3_lst_validation.ipynb) | Sentinel-3 LST from the EOPF Zarr samples compared with ARCO-ERA5 skin temperature, 21 May to 10 June 2025, eastern Spain | `climval` · `xarray` · `zarr` · `pystac-client` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/neuralgcm_climval_validation.ipynb) | [**neuralgcm-eval**: NeuralGCM Forecast Validation](notebooks/neuralgcm_climval_validation.ipynb) | Published NeuralGCM forecasts from WeatherBench2 against ARCO-ERA5, area-weighted, 10 start dates in 2020, global, days 1 to 10 | `climval` · `xarray` · `zarr` · `gcsfs` |

## Run them

Click a Binder badge, wait for the environment to build, then run all cells. The notebooks download their data on the first run, and if a source cannot be reached they stop with an error. No substitute data is used.

To run them locally:

```bash
git clone https://github.com/northflowlabs/northflow-notebooks.git
cd northflow-notebooks
pip install -r requirements.txt
jupyter lab
```

## About climval

[climval](https://github.com/northflowlabs/climval) is an open source Python library for climate model validation. Install it with `pip install climval`. These notebooks pin version 0.1.1.

## Data sources and credits

Each notebook ends with its full citations. In short:

- **CMIP6:** we acknowledge the World Climate Research Programme, which, through its Working Group on Coupled Modelling, coordinated and promoted CMIP6. We thank the climate modeling groups for producing and making available their model output, the Earth System Grid Federation (ESGF) for archiving the data and providing access, and the multiple funding agencies who support CMIP6 and ESGF. Model output from MPI-M, EC-Earth Consortium, CNRM-CERFACS, IPSL and MOHC is used under the [CMIP6 Terms of Use](https://pcmdi.llnl.gov/CMIP6/TermsOfUse/TermsOfUse6-2.html) and [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Accessed through the [Pangeo CMIP6 catalog](https://pangeo-data.github.io/pangeo-cmip6-cloud/).
- **ERA5:** contains modified Copernicus Climate Change Service information 2026. Neither the European Commission nor ECMWF is responsible for any use that may be made of the Copernicus information or data it contains. [Hersbach et al. (2020)](https://doi.org/10.1002/qj.3803), [dataset, single levels](https://doi.org/10.24381/cds.adbb2d47), [dataset, pressure levels](https://doi.org/10.24381/cds.bd0915c6). Accessed through [ARCO-ERA5](https://ams.confex.com/ams/103ANNUAL/meetingapp.cgi/Paper/415842) (Carver and Merose, 2023) and the [NSF NCAR ERA5 archive](https://doi.org/10.5065/BH6N-5N20).
- **Sentinel-3:** contains modified Copernicus Sentinel data 2025, processed by ESA, under the [legal notice on Copernicus Sentinel data](https://sentinels.copernicus.eu/documents/247904/690755/Sentinel_Data_Legal_Notice).
- **Station observations:** source Meteostat and its data providers, under [CC BY 4.0](https://dev.meteostat.net/license). The notebook prints the credit line for each station.
- **NeuralGCM:** [Kochkov et al. (2024)](https://doi.org/10.1038/s41586-024-07744-y). No licence file was found for the forecast archive, so no licence is claimed for these forecasts. NeuralGCM's CC BY-SA 4.0 licence covers its trained model weights only.
- **WeatherBench 2:** [Rasp et al. (2024)](https://doi.org/10.1029/2023MS004019). No licence file was found for the WeatherBench 2 forecast archive.
- **Metrics:** [Taylor (2001)](https://doi.org/10.1029/2000JD900719), and [Gupta et al. (2009)](https://doi.org/10.1016/j.jhydrol.2009.08.003) for Kling-Gupta Efficiency.

## Licence

The notebook code is licensed under the [Apache License 2.0](LICENSE). The data keep their own licences, listed above where a licence was found. No licence is claimed for the NeuralGCM forecasts.

Copyright 2026 Northflow Technologies AS
