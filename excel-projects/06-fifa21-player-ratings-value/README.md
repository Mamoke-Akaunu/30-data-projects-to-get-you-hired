# Excel Project 06 — FIFA 21 Player Ratings & Value Analysis

**Ebook pages:** 16–17  
**Tool:** Excel — Power Query, Tables, IF/IFERROR, COUNTIFS, PivotTables, charts and slicers  
**Dataset notes:** [FIFA 21 Players](../../datasets/fifa21-players/README.md)

## Business scenario

You are a **Junior Sports Data Analyst** building a FIFA 21 game-data comparison report for a football gaming editorial team. Your manager wants to understand the distribution of player ratings, potential development, positions and in-game estimated values. Produce a reproducible snapshot distinguishing game attributes from real-world player ability, contracts or scouting outcomes.

## Current workflow — awaiting question-page upload

The selected source is the **full original uncleaned raw CSV** supplied by the project owner, not the older 111-row sample. The supplied source has **18,979 records, 77 columns and 18,978 unique player IDs**; the repeated ID is intentionally left untouched for now.

The full raw CSV has **not yet replaced** the smaller repository sample files. Do not interpret the old repository CSV filenames as proof that they contain 1,000 records or that the new file is already online. See [dataset status](../../datasets/fifa21-players/README.md).

**Hold point:** Do not clean, deduplicate, change the question graphics, calculate worked solutions or delete data files until the question pages are uploaded and reviewed and the corresponding step is approved.

## Provisional questions from the earlier draft (not yet revalidated against the selected full source)

### Page 16 — Questions 1–5

1. **Data quality:** Import the raw CSV and audit repeated player IDs, missing values, height/weight units, embedded team/contract text and unparseable money labels. What needs review?
2. **Player inventory:** How many distinct player IDs appear? Summarise counts by nationality and documented primary or best-position category, with Unknown where needed.
3. **Overall ratings:** Which players have the highest `↓OVA` ratings? Compare median overall rating by position group and note small samples.
4. **Potential growth:** Calculate `POT − ↓OVA` and compare its distribution across documented age bands. Which age groups show the largest game-defined potential gaps?
5. **Estimated value:** Convert parsable `Value` labels into a consistent numeric unit. Which position groups have the highest median in-game estimated values? Report missing/unparsable values.

### Page 17 — Questions 6–10

6. **Wage comparisons:** Convert parsable in-game `Wage` labels and compare medians by position group. Explain why these figures are not verified employment salaries.
7. **Preferred foot:** Compare player counts and median overall ratings by preferred-foot category, keeping missing or unfamiliar labels separate.
8. **Skill profiles:** For documented position groups, compare FIFA attribute medians (such as `PAC`, `SHO`, `PAS`, `DRI`, `DEF` and `PHY`) and discuss why overall rating alone is insufficient.
9. **Rating–value relationship:** Plot overall rating versus parsed estimated value, optionally distinguishing age groups. Describe apparent patterns and outliers without claiming causality or real-world pricing.
10. **Dashboard:** Build an Excel player-comparison dashboard with position, nationality and age-band filters, at least three visuals, data-quality indicators and three qualified game-data insights.

## Deliverables after validation

- Excel workbook containing raw import, documented cleaning steps (only when authorised), analysis and a dashboard.
- Answers to all ten approved questions, independently checked.
- Notes on duplicates, outliers, grouping rules, missing values and game-data limitations.

**Answers:** Reserved for the ebook solutions section, after all ten questions are validated and approved.

## Publication caution

Underlying rights for FIFA/EA-derived third-party player data, including public/commercial redistribution, have not been independently established. Check permissions before publishing the full raw dataset as a downloadable repository file.
