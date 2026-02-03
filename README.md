# Flight Delay Analysis - Atlanta Airport (ATL) 2023

Analysis of 5,000 flight departures to find delay patterns by day of week, hour of day, and passenger volume.

## Goal

- Track late departure rate using 15-minute threshold (FAA standard)
- Find which days and times have the most delays
- Compare delay patterns with passenger volume to find correlations
- Understand patterns that could help with scheduling

## Data

- `flights.csv` - ATL outbound flights sample (5,000 records)
- `us-daily-passengers.csv` - TSA daily passenger counts (2023)

## Key Findings

### Overall
- Total flights: 5,000
- Overall late rate: **19.8%**

### By Day of Week

| Day | Late Rate |
|-----|-----------|
| Sunday | 22.8% (highest) |
| Friday | 22.5% |
| Thursday | 20.8% |
| Saturday | 19.7% |
| Monday | 19.4% |
| Wednesday | 16.9% |
| Tuesday | 15.9% (lowest) |

![Delay by Day](delay_by_day.png)

### By Hour of Day

| Time Period | Late Rate |
|-------------|-----------|
| Morning (5-12) | ~13.8% |
| Afternoon (12-17) | ~18.4% |
| Evening (17-21) | ~27.7% |
| Night (21+) | ~25.8% |

**Finding:** Evening flights are about 2x more likely to be delayed than morning flights. This is because delays build up during the day (cascade effect).

![Delay by Hour](delay_by_hour.png)

### Passenger Volume vs Delays (Extension)

Comparing delay rates with average daily passenger volume:

| Day | Delay Rate | Avg Passengers | Pattern |
|-----|------------|----------------|---------|
| Sunday | 22.8% (highest) | 2.51M (high) | High volume → High delays |
| Friday | 22.5% | 2.55M (highest) | High volume → High delays |
| Tuesday | 15.9% (lowest) | 2.10M (lowest) | Low volume → Low delays |
| Saturday | 19.7% | 2.17M (low) | Low volume → Lower delays |

![Comparison Chart](comparison_chart.png)

**Pattern:** There is a clear correlation between passenger volume and delay rates. Days with more passengers have higher delay rates.

**Why this happens:**
- More passengers = fuller flights = less buffer time
- Busier airports = more congestion = more delays
- Tighter turnaround times when flights are full

## Business Implications

Why morning flights are better:
- Aircraft haven't had delays from earlier flights yet
- Less airport congestion
- Crews are fresh (no timeout issues)

Why Sunday is worst:
- Weekend travel is heavier (high passenger volume)
- Recovery from Saturday operations

**Recommendation:** If you want to minimize delays, fly on Tuesday morning.

## How to Run

1. Install pandas and matplotlib
2. Open `flights-delays-project.ipynb`
3. Run all cells

## Files

- `flights-delays-project.ipynb` - main analysis notebook
- `flights.csv` - flight data
- `us-daily-passengers.csv` - passenger data
- `EXECUTIVE_SUMMARY.md` - one-page summary
- `delay_by_day.png` - delay rate by day chart
- `delay_by_hour.png` - delay rate by hour chart
- `comparison_chart.png` - side-by-side comparison of delays vs passengers

## Context

Completed as part of Python Institute Data Analysis Associate certification.
