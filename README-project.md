# SpecFinder India

A student prototype for finding and comparing laptops by budget and hardware requirements.

## Features

- Start with a simple profile for gaming at college, study and everyday use, or a custom specification search.
- Choose a budget, graphics level, processor tier, and minimum RAM using beginner-friendly descriptions.
- Open **Know more** to filter by brand, exact GPU and processor family, storage, screen size, laptop category, and model name.
- View laptop matches as image-ready cards, open **View details** for a closer look, or use the full comparison table and price chart.
- Add product photos under `assets/laptops/`; see [the photo guide](assets/laptops/README.md) for filename examples. Until then, the app shows a laptop illustration placeholder.

## Run on macOS

From this project folder:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements-project.txt
streamlit run app.py
```

## Dataset

Place the existing `laptops_cleaned.csv` at `data/processed/laptops_cleaned.csv` and the Smartprix CSV at `data/raw/smartprix_laptop.csv`. The app loads and normalizes the Smartprix rows automatically when that file exists. The Smartprix dataset adds product image URLs alongside more specifications, prices and Apple/RTX listings.

The data files are kept out of Git by `.gitignore`. Preserve the original data and attribution. The first source README describes its dataset as CC0, while that repository's `LICENSE` file says MIT; check with the author if you need to redistribute it. The supplemental file is from Kaggle's Smartprix laptop specs and prices dataset.

## Known limitations

- The combined list has 1,939 rows (992 original plus 947 Smartprix); it is not a complete catalogue of every laptop on the market. Similar model listings from each source are retained.
- The CSV has no store name or product-page URL. The app compares listed prices from the dataset and does not show live cross-store offers.
- RTX 3050 is present in both sources. The gaming preset now starts at the entry gaming GPU tier; use the study or custom profile for MacBooks, which are not gaming-category laptops.
- Ratings are shown as the source's 0–100 score.

## Project area for evaluation

Web Scraping / data analysis. The dataset source reports collecting product listings from Indian e-commerce websites. This student prototype focuses on cleaning structured fields and building a useful specification search interface.
