# NYC Airbnb Market Analysis

Exploratory data analysis of 11 months of InsideAirbnb data (listings + reviews) to answer:
**what does NYC Airbnb activity reveal about broader economic and regulatory trends in the city?**

## Business questions

- **H1 — Geographic concentration:** Is review-based booking demand concentrated in a small number of neighborhoods?
- **H2 — Regulatory impact:** Did NYC's Local Law 18 (enforced Sept 2023) restructure the short-term rental market?
- **H3 — Pricing trend:** Did nightly prices rise faster than inflation, and where?

## Key findings

- Brooklyn and Manhattan account for the large majority of review activity; the Bronx and Staten Island are a small share despite large residential populations.
- Local Law 18 has functionally reshaped the market — **85% of listings now require a 30+ night minimum stay**, pushing most of the market out of the traditional short-term rental model.
- Citywide median nightly price rose **9.9% over 11 months**, roughly 3x the general inflation rate, led by the Bronx and Queens.
- Two bonus analyses build a neighborhood-level demand/supply "opportunity score" to flag where market pressure may shift next.

## Approach

- Loaded and concatenated 11 monthly snapshots of listings and reviews.
- Cleaned the data: deduplicated reviews across overlapping monthly snapshots, filtered to the analysis window, split listings into an "all listings" set and a "priced listings" set (since missing price only matters for price analysis), capped unrealistic price outliers.
- Answered each hypothesis with targeted aggregation and visualization, then extended into two bonus opportunity-scoring analyses.

## Data

Source: [InsideAirbnb](http://insideairbnb.com/get-the-data/) NYC monthly snapshots (listings + reviews). Data files are not included in this repo — download the relevant months and place them in a local `data/` folder as `listings (1).csv` ... `listings (11).csv` and the equivalent `reviews` files.

## Stack

Python, pandas, NumPy, Matplotlib, Seaborn

## Run it

```bash
pip install -r requirements.txt
jupyter notebook nyc_airbnb_market_analysis.ipynb
```
