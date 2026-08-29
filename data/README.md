# Data sources and expected layout

The raw source files are not tracked in Git because they total more than 2 GB. This document records the sources and paths expected by the notebooks.

All commands and notebooks should be run from the repository root.

## Included metadata

`data/meta/stations.csv` is a France-only subset of the EEA station metadata downloaded through the `airbase` client. It contains 18,387 rows and 70 columns and includes every station used in the final analysis.

SHA-256: `b96a354abdcbf2af10319bf85ca64d7d1ecd381e4425c22748eb7b5511125bc1`

Source: [EEA Air Quality Download Service](https://www.eea.europa.eu/en/datahub/datahubitem-view/778ef9f5-6293-4846-badd-56a29c70880d)

The exploratory notebook can refresh the global metadata file. Refreshing is unnecessary for reproducing the submitted analysis because the included France-only subset contains all required fields and records.

## Geod'Air PM2.5 files

Source: [Geod'Air](https://www.geodair.fr/), the French national air-quality database. Geod'Air also documents its [data API](https://www.geodair.fr/donnees/api).

Each hourly file used in the reported run was exported as a separate calendar-year query using interface bounds from 01 January at 01:00 to 31 December at 23:00. In the resulting CSV files, the parsed `Date de début` labels run from 00:00 to 22:00. Boundary hours were not imputed. A boundary check confirmed that the omitted hour could not change the pass or fail status of any Paris, Lyon or Marseille station-month under the 75% capture rule.

Keep the original quoted, semicolon-separated CSV format. The notebooks expect the following layout:

```text
Donnee_pm2.5_paris/
└── Donnees_hourly_yearly/
    ├── pm2.5_paris_2013_hourly.csv
    ├── ...
    ├── pm2.5_paris_2025_hourly.csv
    └── pm2.5_paris_2013_2025_yearly.csv

Donnee_pm2.5_lyon/
├── pm2.5_lyon_2013_hourly.csv
├── ...
├── pm2.5_lyon_2025_hourly.csv
└── pm2.5_lyon_2013_2025_yearly.csv

Donnee_pm2.5_marseille/
├── pm2.5_marseille_2013_hourly.csv
├── ...
├── pm2.5_marseille_2025_hourly.csv
└── pm2.5_marseille_2013_2025_yearly.csv

Donnee_pm2.5_petitecouronne/
├── pm2.5_petitecouronne_2013_hourly.csv
├── ...
├── pm2.5_petitecouronne_2025_hourly.csv
└── pm2.5_petitecouronne_2013_2025_yearly.csv
```

The Petite Couronne export is used only for the descriptive surrounding-area analysis. The other three city folders are required for the main analysis.

## ERA5 meteorological data

Source: [ERA5 hourly data on single levels](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview), Copernicus Climate Change Service.

Configure the CDS API using the [official instructions](https://cds.climate.copernicus.eu/how-to-api). Do not place the API key in the repository. Run `download_era5.ipynb` to create `data/raw/era5` and the filenames used by notebooks 02 and 05.

Notebook 02 uses combined Paris wind files for 2013-2024. Notebook 05 uses separate wind components, 2 m temperature, boundary-layer height and a land-sea mask for Paris, Lyon and Marseille for 2013-2025.

## Vehicle-fleet data

Source: [Parc de vehicules routiers](https://www.data.gouv.fr/datasets/parc-de-vehicules-routiers), Service des donnees et etudes statistiques.

Place the June 2026 communal file at:

```text
data/dose/raw/parc_communal_2026-06.csv
```

Notebook 06 reads the private-car rows, Crit'Air categories and communal or arrondissement codes for Paris, Lyon and Marseille. The original file is about 221 MB and is therefore not included in the repository.

## Optional EEA scouting data

Notebooks 01 and 01b use optional EEA Parquet downloads:

```text
data/raw/FR/
data/raw_no2_hist/FR/
data/raw_no2_verified/FR/
data/raw_london/GB/
data/london_meta.csv
```

These files document exploratory station and comparator scouting. They are not required to reproduce the reported estimates in notebook 06.

## Generated files

Notebook 05 creates files under `data/interim`, including meteorological tables, cross-validation summaries, normalised station series, the validation package and the surrounding-area panel. These files are excluded from Git because they are generated from the source data.

Notebook 06 creates the definitive small tables under `results/reported`. Those reported files are retained in the repository.
