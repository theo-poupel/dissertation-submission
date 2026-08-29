# Dissertation submission code

This repository contains the reproducibility materials for an MSc dissertation examining the timing of air-quality policies and changes in PM2.5 concentrations in Paris, with Lyon and Marseille used as French comparators.

The notebooks retain their executed outputs so that the reported calculations can be inspected without downloading the full source data. Re-running the complete analysis requires the public data described in `data/README.md`.

## Repository contents

The analysis notebooks remain in the repository root because their relative paths assume that location.

| File | Purpose | Required for the main reported analysis |
|---|---|---|
| `01_eea_exploration.ipynb` | Exploratory review of EEA PM2.5 metadata and observations | No |
| `01b_scouting.ipynb` | Exploratory station, NO2 and London scouting | No |
| `02_geodair_validation.ipynb` | Validation of the French PM2.5 files and the Paris wind-response comparison | Yes |
| `03_paris_panel.ipynb` | Paris station-panel and composition diagnostics | Yes |
| `04_french_comparators.ipynb` | French comparator trends and station selection | Yes |
| `05_normalisation_validation.ipynb` | Meteorological normalisation and validation | Yes |
| `06_batch.ipynb` | Main estimates, sensitivities and reported result tables | Yes |
| `download_era5.ipynb` | Downloads the ERA5 files required by notebooks 02 and 05 | Data preparation |

The main reported sequence is therefore 02, 03, 04, 05 and 06. Notebooks 01 and 01b document exploratory work that informed the final design.

## Software setup

The reported run used Python 3.12. A minimal environment is provided rather than a machine-specific export containing every transitive package.

Using Conda from the repository root:

```bash
conda env create -f environment.yml
conda activate dissertation-submission
jupyter lab
```

Alternatively, using an existing Python 3.12 environment:

```bash
python -m pip install -r requirements.txt
jupyter lab
```

## Data setup

Raw Geod'Air, EEA, ERA5 and vehicle-fleet files are not stored in the Git history because of their combined size. Their sources, required filenames and expected directories are recorded in `data/README.md`.

The included `data/meta/stations.csv` is the France-only subset of the EEA station metadata used by the analysis. It contains the same columns required by the notebooks while avoiding the 112 MB global metadata file.

ERA5 access requires a Climate Data Store account and local API configuration. Credentials must not be committed to this repository. Follow the official CDS API instructions and then run `download_era5.ipynb` from the repository root.

## Running the analysis

1. Create the software environment.
2. Arrange the source data exactly as described in `data/README.md`.
3. Run `download_era5.ipynb` if the ERA5 files are not already present.
4. Restart the kernel before each analysis notebook.
5. Run notebooks 02 to 06 in numerical order using `Run All`.

Notebook 05 is the most computationally intensive stage. It creates the derived files in `data/interim`. Notebook 06 reads those files and writes the final tables to `results/reported`.

All stochastic procedures use fixed seeds. The weather-model validation uses the settings recorded in notebook 05, and the final block-bootstrap analyses use the settings recorded in notebook 06.

## Reported outputs

The definitive small output tables, run metadata and text results package are stored in `results/reported`. The `results/quarantine` directory is intentionally excluded because it contains non-reported diagnostic runs.

The lead diagnostics in notebook 06 bound the interpretation of the mechanism estimates. The presence of a confidence interval excluding zero is not, by itself, treated as evidence of a causal policy effect when the corresponding lead test rejects comparability.

## Reproducible release

The repository is named `dissertation-submission`. The dissertation should link to its fixed `v1.0` release, rather than relying only on the changing `main` branch. The release tag fixes the exact notebooks, environment description and reported tables supplied to the examiner.
