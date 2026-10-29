<a href="https://northflow.no"><img src=".github/assets/northflow-mark.svg" alt="Northflow" width="40" height="40"></a>

# Northflow notebooks

Reproducible climate validation notebooks built on climval, each one runnable in the browser through Binder.

[Research page](https://research.northflow.no/systems/climval) · [climval](https://github.com/northflowlabs/climval) · [Licence](#licence)

[![Licence: Apache 2.0](https://img.shields.io/badge/licence-Apache%202.0-0e6b63)](LICENSE)

## Notebooks

| Run | Notebook | Description | Stack |
|-----|----------|-------------|-------|
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/era5_station_validation.ipynb) | [**groundtruth**: ERA5 Station Validation](notebooks/era5_station_validation.ipynb) | Validates ERA5 reanalysis against real weather station observations across 5 climate zones | `climval` · `xarray` · `openmeteo-requests` · `meteostat` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/cmip6_taylor_diagram.ipynb) | [**cmip6-taylor**: CMIP6 Multi-Model Intercomparison](notebooks/cmip6_taylor_diagram.ipynb) | 5 CMIP6 models vs ERA5 over Europe with Taylor diagram and metric scorecard | `climval` · `xarray` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/sentinel3_lst_validation.ipynb) | [**sentinel3-lst**: Sentinel-3 SLSTR LST Validation](notebooks/sentinel3_lst_validation.ipynb) | Validates Sentinel-3 Land Surface Temperature against ERA5-Land using EOPF Zarr | `climval` · `xarray` · `zarr` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/climval_arraylake_integration.ipynb) | [**climval-arraylake**: Arraylake Integration](notebooks/climval_arraylake_integration.ipynb) | climval validation on Arraylake-stored climate data with version tagging | `climval` · `xarray` · `arraylake` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/neuralgcm_climval_validation.ipynb) | [**neuralgcm-eval**: NeuralGCM Forecast Validation](notebooks/neuralgcm_climval_validation.ipynb) | Validates NeuralGCM deterministic forecasts against ERA5 across WeatherBench2 headline variables | `climval` · `xarray` · `zarr` · `gcsfs` |

## Run them

Click a Binder badge, wait for the environment to build, then run all cells.

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
