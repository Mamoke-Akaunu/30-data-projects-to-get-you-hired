# U.S. Domestic Airline Routes — Verified Sample

**Used by:** [Excel Project 05 — U.S. Airline Route Demand & Capacity Analysis](../../excel-projects/05-us-airline-route-demand-capacity/)

## Download the dataset

[**airline_routes_sample_1199.csv**](airline_routes_sample_1199.csv) — the **only required CSV** for this project.

This is a historical, selected sample of **1,199 route records** across **1990–2008**, with **15 columns**. It is not a census of U.S. flights, routes or airlines. The file name describes the actual number of records.

## Data dictionary

- `Origin_airport`, `Destination_airport` — origin and destination airport codes; direction matters.
- `Origin_city`, `Destination_city` — city/state labels.
- `Passengers`, `Seats`, `Flights` — reported route-record volume/capacity measures.
- `Distance` — source distance measure; verify units before making distance-unit claims.
- `Fly_date` — first day of a calendar month indicating a historical observation period, **not an individual flight date**.
- `Origin_population`, `Destination_population` — supplied population context, not a yearly series to be inferred.
- `Org_airport_lat`, `Org_airport_long`, `Dest_airport_lat`, `Dest_airport_long` — airport coordinates, with some missing `NA` values.

## Verified file quality

- **1,199 records and 15 columns**, after repairing five accidentally concatenated lines in the previously published `airline_routes_sample_1000.csv`; no substantive values were changed.
- **45 exact duplicate rows** retained deliberately for audit.
- **457 records** share an origin–destination–month key with an earlier record; these are **not necessarily duplicates** or errors. No airline or other source-level identifier is present.
- **115 rows have zero seats** and **2 have zero flights**; exclude invalid denominators when computing seat occupancy or passengers per flight.
- Missing coordinate values: **6 origin latitude**, **6 origin longitude**, **1 destination latitude**, and **1 destination longitude**.
- Covers **1990–2008**, unevenly; do not describe this sample as current airline demand or a representative time series.
- `Passengers / Seats` is a **sample seat-use proxy**, not a verified airline load factor for the industry; use the ratio of eligible totals, not a simple mean of row percentages.
- Do not infer fares, revenue, profitability, airline identity or individual flight performance: none of those fields is supplied.

## Handling and analysis

Import the CSV with Excel Power Query. Keep an untouched `Raw_Data` query. Audit duplicates without automatically removing all repeated route-month keys; document any exact-row deduplication decisions. Standardise airport and location text only where justified, parse month and year from `Fly_date`, and exclude zero-seat rows from any seat-use denominator. State the eligible record count for each KPI.

## Licence and provenance

The source was described as CC0 by an uploader, but original collection details and redistribution permission have **not been independently verified**. Verify redistribution rights before commercial publication.
