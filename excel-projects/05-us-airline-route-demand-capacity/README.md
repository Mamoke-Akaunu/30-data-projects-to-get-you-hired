# Excel Project 05 — U.S. Airline Route Demand & Capacity Analysis

**Ebook pages:** 14–15  
**Tool:** Excel — Power Query, Tables, SUMIFS/COUNTIFS, PivotTables, charts and slicers  
**Dataset:** [Download the one required CSV](../../datasets/us-airline-routes/airline_routes_sample_1199.csv)  
**Read first:** [Dataset notes and limitations](../../datasets/us-airline-routes/README.md)

## Business scenario

You are a **Junior Network Planning Analyst** supporting a regional aviation research team. Your manager wants a descriptive view of the routes, airports, passenger volumes and recorded seat capacity in a selected historical U.S. domestic route sample. The team needs a reproducible, clearly qualified analysis that does not mistake repeated route-month records for individual flights or claim that the sample represents today's market.

## Verified input

One 15-column CSV with **1,199 observations**, spanning **1990–2008**. The published file repairs five accidentally joined record lines from the original sample, without changing source values.

- 45 exact duplicate rows, deliberately kept for a documented audit.
- 457 repeated origin–destination–month keys; do **not** assume all are errors, because the source lacks an airline-level identifier.
- 115 rows with zero `Seats`; 2 rows with zero `Flights`.
- Some airport-coordinate fields are `NA`.
- Source contains no fare, revenue, airline name, flight-level punctuality or modern demand indicators.

## Page 14 — Questions 1–5

1. **Data quality:** Audit exact duplicates, repeated origin–destination–month keys, zero seats/flights and missing airport coordinates. Which records need review, and which should remain in the analysis?
2. **Route inventory:** How many distinct directional origin–destination pairs appear in the sample? Compare route-pair counts with total records, and explain why repeated monthly entries are not unique routes.
3. **Origin airports:** Which five origin airports have the highest recorded passenger totals in the sample? Show passenger totals and eligible record counts.
4. **Destination airports:** Which five destination airports have the highest recorded passenger totals? Compare their ranking with the origin-airport ranking and highlight sample coverage limitations.
5. **Seat-use proxy:** For routes with valid positive seat counts, compute `sum(Passengers) / sum(Seats)` by origin airport. Which airports have the highest ratio among groups with meaningful recorded volume? Report exclusions.

## Page 15 — Questions 6–10

6. **Flights by route:** Rank directional routes by total recorded flights, excluding invalid flight records and distinguishing flight volume from record count.
7. **Passengers per flight:** Compute `sum(Passengers) / sum(Flights)` for eligible positive-flight records by route. Where do larger recorded aircraft loads appear?
8. **Distance bands:** Group routes by the source `Distance` values into documented bands. How do passenger volume and the seat-use proxy compare across bands? State any unverified distance-unit assumption.
9. **Historical coverage:** Group records by year and compare descriptive passenger totals and number of observed routes. Explain why uneven sample coverage cannot support claims about national industry growth.
10. **Dashboard:** Build an Excel route-planning snapshot with origin, destination and year filters, at least three visuals, data-quality indicators and three evidence-based recommendations or cautions.

## Deliverables

- Excel workbook with raw data, cleaned table, audit, analysis and dashboard worksheets or equivalent Power Query outputs.
- Transparent handling of exact duplicates and repeated route-month keys, with counts of eligible and excluded records.
- Answers to all ten questions using PivotTables/formulas and clearly labelled visuals.
- Three qualified findings; no unsupported inference about fares, revenue, airline profitability or current U.S. air travel.

**Answers:** Provided separately in the ebook solutions, not in this starter brief.

## Provenance

A CC0 status was reported by a data uploader, but underlying source redistribution rights have not been independently verified.
