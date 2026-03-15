<img src="assets/northflow_logo.png" width="60"/>

**Northflow Technologies** · [northflow.no](https://northflow.no)  
*Institutional scientific discovery infrastructure for climate, space, and critical systems*

---

Northflow Technologies builds institutional scientific discovery infrastructure
across climate, space, and critical systems. These notebooks are our open science
contribution — reproducible, citable workflows powered by climval.
Every notebook runs in your browser with no setup required.

## Notebooks

| Run | Notebook | Description | Stack |
|-----|----------|-------------|-------|
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/era5_station_validation.ipynb) | **groundtruth** — ERA5 Station Validation | Validates ERA5 reanalysis against real weather station observations across 5 climate zones | `climval` · `xarray` · `openmeteo-requests` · `meteostat` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/cmip6_taylor_diagram.ipynb) | **cmip6-taylor** — CMIP6 Multi-Model Intercomparison | 5 CMIP6 models vs ERA5 over Europe with Taylor diagram and metric scorecard | `climval` · `xarray` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/sentinel3_lst_validation.ipynb) | **sentinel3-lst** — Sentinel-3 SLSTR LST Validation | Validates Sentinel-3 Land Surface Temperature against ERA5-Land using EOPF Zarr | `climval` · `xarray` · `zarr` |
| [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/northflowlabs/northflow-notebooks/HEAD?filepath=notebooks/climval_arraylake_integration.ipynb) | **climval-arraylake** — Arraylake Integration | climval validation on Arraylake-stored climate data with version tagging | `climval` · `xarray` · `arraylake` |

## Getting Started

Every notebook runs in Binder — click the badge, wait for the environment, run all cells.

To run locally:
```bash
git clone https://github.com/northflowlabs/northflow-notebooks.git
cd northflow-notebooks
pip install -r requirements.txt
jupyter lab
```

## About climval

[climval](https://github.com/northflowlabs/climval) is an open-source Python library for composable climate model validation. `pip install climval`

## License

Apache 2.0 — see [LICENSE](LICENSE) for details.

---

*[Northflow Technologies](https://northflow.no) · Stavanger, Norway*
