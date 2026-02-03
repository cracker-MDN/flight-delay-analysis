# Executive Summary: Flight Delay Analysis
## Atlanta Airport (ATL) — 2023

---

### Overview

Analysis of **5,000 flight departures** from Hartsfield-Jackson Atlanta International Airport (world's busiest) to identify delay patterns and provide actionable insights for operational planning.

**Methodology:** Flights classified as "late" if actual departure exceeds scheduled time by more than 15 minutes (FAA industry standard).

---

### Key Metrics

| Metric | Value |
|--------|-------|
| Total Flights Analyzed | 5,000 |
| Overall Late Rate | **19.8%** |
| Late Flights | 992 |
| Average Delay | 11.5 minutes |

---

### Top Findings

#### 1. Time of Day is the Strongest Predictor

| Time Period | Delay Rate | vs. Average |
|-------------|------------|-------------|
| Morning (5:00–12:00) | **13.8%** | -6.0 pts ✅ |
| Afternoon (12:00–17:00) | 18.4% | -1.4 pts |
| Evening (17:00–21:00) | **27.7%** | +7.9 pts ❌ |
| Night (21:00–5:00) | 25.8% | +6.0 pts |

**Insight:** Evening flights are **2x more likely** to be delayed than morning flights. The "delay cascade" effect means problems accumulate throughout the day.

#### 2. Day of Week Patterns

| Day | Delay Rate | Ranking |
|-----|------------|---------|
| **Tuesday** | **15.9%** | Best ✅ |
| Wednesday | 16.9% | 2nd |
| Monday | 19.4% | 3rd |
| Saturday | 19.7% | 4th |
| Thursday | 20.8% | 5th |
| Friday | 22.5% | 6th |
| **Sunday** | **22.8%** | Worst ❌ |

**Insight:** Sunday has ~44% more delays than Tuesday. Weekend leisure travel and recovery from Saturday operations contribute to higher delay rates.

#### 3. Carrier Performance

| Carrier | Delay Rate | Volume |
|---------|------------|--------|
| 9E (Endeavor Air) | 7.1% | 311 flights |
| Delta (DL) | 18.4% | 3,258 flights |
| Southwest (WN) | 27.7% | 553 flights |
| Frontier (F9) | 38.9% | 126 flights |

**Insight:** Budget carriers show significantly higher delay rates. Delta, as ATL's dominant carrier, performs slightly below average.

---

### Recommendations

| Situation | Recommendation |
|-----------|----------------|
| Critical travel | Book **Tuesday morning** flights (lowest delay risk) |
| Avoid if possible | **Sunday evening** flights (highest delay probability) |
| Carrier choice | Major carriers (DL, UA, AA) outperform budget options |
| Buffer planning | Add extra time for afternoon/evening connections |

---

### Operational Implications

1. **Morning flights start fresh** — no accumulated delays from earlier flights
2. **Delays cascade** — one late departure affects subsequent flights
3. **Sunday recovery** — weekend operations need additional resources
4. **Peak hour stress** — 17:00–21:00 shows concentrated delay risk

---

### Data Sources

- Flight data: ATL outbound sample, 2023 (5,000 records)
- Delay threshold: 15 minutes (FAA standard)
- Tools: Python (Pandas, Matplotlib)

---

*Analysis demonstrates skills in: operational KPI monitoring, temporal pattern analysis, data visualization, and data-driven insights for decision support.*

**GitHub:** [github.com/cracker-MDN/flight-delay-analysis](https://github.com/cracker-MDN/flight-delay-analysis)
