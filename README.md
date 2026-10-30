<a href="https://northflow.no"><img src=".github/assets/northflow-mark.svg" alt="Northflow" width="40" height="40"></a>

# Northflow notebooks

Reproducible climate validation notebooks built on climval. Every notebook reads real data from public sources, with no account needed, and every figure comes from that data.

[Research page](https://research.northflow.no/systems/climval) · [climval](https://github.com/northflowlabs/climval) · [Licence](#licence)

[![Licence: Apache 2.0](https://img.shields.io/badge/licence-Apache%202.0-0e6b63)](LICENSE)

## Notebooks

| Run | Notebook | Description | Stack |
|-----|----------|-------------|-------|
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/era5_station_validation.ipynb) | [**groundtruth**: ERA5 Station Validation](notebooks/era5_station_validation.ipynb) | ERA5 from Open-Meteo against Meteostat station observations, daily, 2015 to 2020, in Oslo, Madrid, Nairobi, Toronto and Sydney | `climval` · `xarray` · `meteostat` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/cmip6_taylor_diagram.ipynb) | [**cmip6-taylor**: CMIP6 Multi-Model Intercomparison](notebooks/cmip6_taylor_diagram.ipynb) | Five CMIP6 historical runs from the Pangeo catalog against ARCO-ERA5, monthly climatology, 1985 to 2014, Europe | `climval` · `xarray` · `gcsfs` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/sentinel3_lst_validation.ipynb) | [**sentinel3-lst**: Sentinel-3 SLSTR LST Validation](notebooks/sentinel3_lst_validation.ipynb) | Sentinel-3 LST from the EOPF Zarr samples against ARCO-ERA5 skin temperature, May and June 2025, eastern Spain | `climval` · `xarray` · `zarr` · `pystac-client` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/neuralgcm_climval_validation.ipynb) | [**neuralgcm-eval**: NeuralGCM Forecast Validation](notebooks/neuralgcm_climval_validation.ipynb) | Published NeuralGCM forecasts from WeatherBench2 against ARCO-ERA5, 10 start dates in 2020, global, days 1 to 10 | `climval` · `xarray` · `zarr` · `gcsfs` |

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

[climval](https://github.com/northflowlabs/climval) is an open source Python library for climate model validation. Install it with `pip install climval`.

## Licence

The notebooks are licensed under the [Apache License 2.0](LICENSE).

Copyright 2026 Northflow Technologies AS
