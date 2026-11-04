# Excel Project 06 — FIFA 21 Player Ratings & Value Analysis

**Ebook pages:** 16–17  
**Tool:** Excel — Power Query, Tables, IF/IFERROR, COUNTIFS, PivotTables, charts and slicers  
**Dataset:** [FIFA 21 raw and cleaned samples](../../datasets/fifa21-players/)  
**Read first:** [Dataset notes and rights limitations](../../datasets/fifa21-players/README.md)

## Business scenario

You are a **Junior Sports Data Analyst** building a FIFA 21 game-data comparison report for a football gaming editorial team. Your manager wants to understand the distribution of player ratings, potential development, positions and in-game estimated values. Produce a reproducible snapshot that clearly distinguishes game attributes from real-world player ability, contracts or scouting outcomes.

## Verified scope

The repository provides two CSV variants, `fifa21_raw_sample_1000.csv` and `fifa21_cleaned_sample_1000.csv`. The columns include player ID, overall rating (`↓OVA`), potential (`POT`), age, positions, nationality, value and wage labels, and technical attributes. The raw sample includes `Team & Contract`; the comparison sample splits club and contract. Treat the two as alternate versions, **not additional unique players**.

## Page 16 — Questions 1–5

1. **Data quality:** Import the raw CSV and audit repeated player IDs, missing values, mixed height/weight formats, embedded team/contract text and unparsable money labels. What needs review?
2. **Player inventory:** How many distinct player IDs appear in the sample? Summarise counts by nationality and documented primary or best-position category, with Unknown where needed.
3. **Overall ratings:** Which players have the highest `↓OVA` ratings? Compare median overall rating by position group and note small samples.
4. **Potential growth:** Calculate `POT − ↓OVA` and compare its distribution across documented age bands. Which age groups show the largest game-defined potential gaps?
5. **Estimated value:** Convert parsable `Value` labels (such as €67.5M and €560K) into a consistent numeric unit. Which position groups have the highest median in-game estimated values? Report missing/unparsable values.

## Page 17 — Questions 6–10

6. **Wage comparisons:** Convert parsable in-game `Wage` labels and compare medians by position group. Explain why these figures are not verified employment salaries.
7. **Preferred foot:** Compare player counts and median overall ratings by preferred-foot category, keeping missing or unfamiliar labels separate.
8. **Skill profiles:** For documented position groups, compare relevant FIFA attribute medians (such as `PAC`, `SHO`, `PAS`, `DRI`, `DEF` and `PHY`) and discuss why overall rating alone is insufficient.
9. **Rating–value relationship:** Plot overall rating versus parsed estimated value, optionally distinguishing age groups. Describe apparent patterns and outliers without claiming causality or real-world pricing.
10. **Dashboard:** Build an Excel player-comparison dashboard with position, nationality and age-band filters, at least three visuals, data-quality indicators and three qualified game-data insights.

## Deliverables
- Documented Excel workbook with raw import, cleaned table, audit, analysis and dashboard.
- Validation notes comparing raw and reference-cleaned fields, not a blind replacement of source records.
- Formulas/PivotTables answering all ten questions and a dashboard with at least three visuals.
- Notes on excluded records, small groups, parsing assumptions, sampling and game-data limitations.

**Answers:** In the ebook solutions section, not the public starter brief.

## Provenance
The underlying FIFA game-data/SoFIFA and EA rights are not independently verified. Check commercial redistribution permissions before publication.
