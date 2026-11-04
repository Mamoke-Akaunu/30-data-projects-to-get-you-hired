# Excel Project 02 — European Accommodation Pricing & Benchmarking

**Ebook pages:** 8–9 (two-page project brief)  
**Tools:** Excel Tables, formulas, PivotTables, charts, conditional formatting and slicers  
**Dataset:** [Balanced European accommodation pricing sample — 2,160 observations](../../datasets/european-airbnb-prices/accommodation_balanced_sample_2160.csv)  
**Dataset documentation:** [Read the source README](../../datasets/european-airbnb-prices/README.md)

## Business scenario

You are a **Junior Market Research Analyst** advising an accommodation platform that wants to benchmark advertised property prices in nine European cities. Compare pricing by city, weekday/weekend category, room type, accommodation size, distance to city centre and host characteristics. Present meaningful insights and data limitations.

## What you receive

One CSV, `accommodation_balanced_sample_2160.csv`: **2,160 rows, 19 columns**, with 120 weekday and 120 weekend observations for **each** of Amsterdam, Athens, Barcelona, Berlin, Budapest, Lisbon, Paris, Rome and Vienna.

This is **deliberately balanced**, not a representative random market sample. It has no missing cells or exact duplicate rows and all prices are positive. There are only 18 shared-room observations, so subgroup results may be unstable.

**Important:** The source has no dates, actual bookings, occupancy or realised income. You are analysing *listed prices*, **not revenue**, market share or longitudinal price trends. Currency is not specified in the sample schema; don't invent a currency.

## Questions — Page 8 (1–5)

1. **Data validation:** Check `Price`, `Person Capacity`, `Bedrooms`, `Day` and `Room Type` for blanks, invalid values, duplicates and unusually high prices. Document any records flagged as outliers.
2. **City coverage:** How many sampled accommodation records are there for each city, and how many are labelled Weekday versus Weekend?
3. **Price benchmarking:** Which cities have the highest and lowest **median** listed prices? Compare the mean with the median and discuss differences.
4. **Weekday vs weekend:** What is the difference between Weekday and Weekend median prices within each city?
5. **Room type:** How do the median listed prices of Entire home/apt, Private room and Shared room vary between cities? Flag small sample groups.

## Questions — Page 9 (6–10)

6. **Capacity:** How does listed price vary by `Person Capacity`? Calculate a price-per-person-capacity indicator for records with valid positive capacity.
7. **Location:** Create documented city-centre distance bands (for example, 0–2 km, >2–5 km, >5 km). Within each city, how do median prices change across those bands?
8. **Superhost:** Within comparable city and room-type groups, how do Superhost and non-Superhost listings differ in median listed price and average guest satisfaction? This is descriptive, not proof of a causal effect.
9. **Price variability:** Which city and room-type combinations show the widest price spread (for example, using the interquartile range)? Explain the impact of extreme values.
10. **Dashboard:** Create an Excel accommodation-price benchmarking dashboard with filters for City, Day and Room Type, at least three visuals and three justified recommendations or cautions.

## Submission

- An Excel workbook importing the provided CSV as a structured Table.
- Cleaned/validated analysis sheet with documented flags and any derived fields.
- PivotTables and charts answering Questions 1–10.
- A summary dashboard with slicers and a short business-interpretation paragraph.
- A concise note about **balanced sample selection**, **scarce Shared rooms**, the lack of actual booking/revenue data and any price outliers.

**Do not publish solutions here:** worked answers will be included in the ebook's separate Excel Solutions section.

## Rights

CC0 was claimed for the source upload. Underlying provenance and redistribution authority remain unverified.
