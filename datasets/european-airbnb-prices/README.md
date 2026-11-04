# European Accommodation Prices — Portfolio Dataset

**Primary Excel use:** [Project 02 — Accommodation Pricing & Benchmarking](../../excel-projects/02-accommodation-pricing-benchmarking/)

## Download the dataset

[**accommodation_balanced_sample_2160.csv**](accommodation_balanced_sample_2160.csv) is the **only recommended CSV** for this exercise.

This is a reproducible, deliberately **balanced practice subset** of the user-provided `Aemf1.csv` (41,714 observations), not a representative random sample. It contains **2,160 rows and 19 columns** across nine European cities, with **120 weekday and 120 weekend observations per city**.

## Key columns

- `City`: Amsterdam, Athens, Barcelona, Berlin, Budapest, Lisbon, Paris, Rome or Vienna.
- `Price`: numeric accommodation price; the provided file does not contain a currency column.
- `Day`: Weekday or Weekend category (**not** a booking or calendar date).
- `Room Type`: Entire home/apt, Private room or Shared room.
- `Person Capacity`, `Bedrooms`: size and accommodation capacity.
- `Superhost`, `Guest Satisfaction`, `Cleanliness Rating`: host and satisfaction fields.
- `City Center (km)`, `Metro Distance (km)`: distances in kilometres.

**Data validation:** Sample has nine cities, both Day categories, 19 columns, no blank cells, no exact duplicate rows and prices greater than zero. Price values range approximately **46.40–2,175.61**. The sample contains only **18 Shared room observations**; warn readers that this group's comparisons are less robust.

## Important analytical limits

- There are **no booking dates, booking counts, actual occupancy, financial transactions or realised revenue** in these records.
- Price comparisons describe this balanced **practice sample**; they should not be interpreted as representative market averages.
- Day denotes a **weekday/weekend category**, not a dated time series.
- Use medians and distribution checks alongside means; prices are skewed and may contain high outliers.
- Consider comparing property characteristics **within cities and room types** rather than implying causal effects.

## Reuse and provenance

The uploaded source dataset was reported as CC0 on its distribution page; original source provenance and commercial redistribution authority have **not** been independently verified. This subset preserves the original field spellings, including `Restraunt Index`.
