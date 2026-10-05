# Partschecker — SpecFinder India

A Python and Streamlit prototype for finding Indian laptops by exact hardware specifications and comparing their listed prices. The first version focuses on laptops; PC components can be added later.

## Run on macOS

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements-project.txt
streamlit run app.py
```

Place `laptops_cleaned.csv` at `data/processed/laptops_cleaned.csv` and the supplemental `smartprix_laptop.csv` at `data/raw/smartprix_laptop.csv` before launching. The app uses the supplemental file automatically when it is present.

## Data source and limits

The project combines the [public Indian laptop specifications dataset](https://github.com/abhinavflac/laptops-specs-dataset) with the [Smartprix laptop specs and prices dataset](https://www.kaggle.com/datasets/souravghosh999/laptop-specifications-and-prices-smartprix). The added Smartprix rows include image URLs and supplement brand, GPU, CPU, RAM, storage, display and price coverage. Both sources are dataset snapshots; they do not provide live cross-store offers or current availability.

Dataset files are kept local and are not included in this repository. Download each CSV from its linked source and use the paths above.
