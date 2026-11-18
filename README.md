# London Air Quality Analysis (2017–2024)

Trends, weather drivers, the COVID-19 lockdown effect, and next-day forecasting of NO₂ and PM₂.₅ in London.

**Data:** hourly NO₂ / PM₂.₅ / O₃ from the London Air Quality Network (Marylebone Road, North Kensington, Bloomsbury) and hourly ERA5 weather from Open-Meteo.

## Key results
- NO₂ roughly **halved** 2017→2023. Marylebone Road reached the UK legal limit in 2024.
- Weather-normalised lockdown effect (23 Mar – 12 May 2020): **NO₂ −46 % kerbside, −32 % background**, O₃ +25 %, no reliable PM₂.₅ reduction.
- Biggest drivers: boundary-layer height (atmospheric mixing), wind and the traffic cycle. Easterly winds bring in PM₂.₅ from the continent.
- Next-day forecast for 2024 (held-out year): NO₂ RMSE 5.4 µg/m³ (−30 % vs persistence), PM₂.₅ RMSE 3.1 µg/m³ (−17 to −18 %).

## Run it
```bash
pip install -r requirements.txt
jupyter notebook london_air_quality.ipynb
```
The raw data is in `data_raw/`. Set `REFETCH = True` in section 2 to download it again from the APIs.

## Files
| File | What |
|---|---|
| `london_air_quality.ipynb` | Main notebook (code, charts, write-up) |
| `london_air_quality.html` | Same notebook as a web page, for sharing |
| `data_raw/` | Raw hourly air-quality and weather CSVs |
| `figures/` | All charts as PNG |
| `london_air_quality_clean.csv` | Merged, cleaned hourly dataset (created when you run the notebook) |
