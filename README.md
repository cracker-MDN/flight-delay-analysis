# Flight Delays Ops Monitoring (ATL, 2023)

Operations-style KPI monitoring project using flight departure data to track late-flight rate and weekly trends.

## Goal
Simulate an operations analyst workflow:
- define delay KPIs (late departures > 15 minutes)
- create weekday trend reporting
- produce breakdown tables for monitoring (carrier / destination)

## Data
- `flights.csv` (ATL outbound sample, 2023)
- `departures-check-point.tsv` (supporting file)
- `us-daily-passengers.csv` (TSA passenger volume, 2023)
- `flights.csv`

## Key KPIs
- Late departure flag: `delay_minutes > 15`
- Late rate (% late flights)
- Late rate by weekday (trend view)

## Key Findings (example — update with your final numbers)
- Overall late rate: ~19.8%
- Highest late rate: Sunday (~22.8%) and Friday (~22.5%)
- Lowest late rate: Tuesday (~15.9%)

## How to run
1. Create environment (optional):
   - Python 3.x
   - pandas, matplotlib
2. Open notebook:
   - `flights-delays-project.ipynb`
3. Run all cells.

## Project Structure
- `flights-delays-project.ipynb` — analysis + charts
- `flights.csv` — flight records
- `departures-check-point.tsv` — supporting data
- `us-daily-passengers.csv` — passenger volume reference

## Next Improvements
- Add carrier and destination benchmarking tables to README
- Add anomaly checks (missing values, duplicates, outliers)
- Extend to cancellations / disruption recovery metrics

Context
Completed as part of the Python Institute Data Analysis Associate certification track.
This analysis demonstrates skills relevant to airline operations monitoring, competitor benchmarking, and disruption tracking.
