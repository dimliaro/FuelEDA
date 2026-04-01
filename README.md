# Fuel EDA — Hyundai i20

Exploratory data analysis of personal fuel fill-up records for a Hyundai i20, tracked via the [Fuelio](https://www.fuelio.net/) app from November 2022 onwards.

## Dataset

`Fuelio_fill_ups.csv` — 68 fill-up records with the following columns:

| Column | Description |
|---|---|
| `Date` | Fill-up date |
| `Odometer_km` | Odometer reading at fill-up |
| `Liters` | Litres added |
| `Full_Tank` | Whether tank was filled to full |
| `Cost_EUR` | Total cost in euros |
| `Price_Per_Liter_EUR` | Fuel price per litre |
| `Consumption_l100km` | Fuel consumption (l/100km) |
| `Fuel_Type` | Unleaded 95 or 98 |
| `Location` | Fill-up location (partial) |
| `Notes` | Miscellaneous notes |

## Analysis

The notebook `i20_Fuel_EDA.ipynb` covers 11 questions:

1. **Fuel price over time** — price per litre for each fill-up
2. **Price by fuel type** — Unleaded 95 vs 98 separated
3. **Consumption over time** — l/100km trend by fuel type
4. **Fuel type comparison (box plot)** — no meaningful difference in consumption
5. **Cost of Unleaded 98** — ~€0.10/L more expensive with no efficiency gain (~€3.30 wasted per fill-up)
6. **Km between fill-ups** — median ~465 km, one 3135 km outlier from missed recordings
7. **Distribution of km between fill-ups** — histogram, most fill-ups every 350–550 km
8. **Monthly fuel cost** — total spend per month over time
9. **Consumption by season** — summer has lower consumption due to highway driving
10. **Cumulative fuel cost** — running total spend since Nov 2022
11. **Days between fill-ups** — median ~14 days (roughly every 2 weeks)

## Setup

```bash
pip install pandas matplotlib seaborn
jupyter notebook i20_Fuel_EDA.ipynb
```
