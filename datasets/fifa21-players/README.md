# FIFA 21 Player Ratings — Raw and Cleaned Samples

**Used by:** [Excel Project 06 — FIFA 21 Player Ratings & Value Analysis](../../excel-projects/06-fifa21-player-ratings-value/)

## Dataset files
- [fifa21_raw_sample_1000.csv](fifa21_raw_sample_1000.csv) — unstandardised source sample for cleaning practice.
- [fifa21_cleaned_sample_1000.csv](fifa21_cleaned_sample_1000.csv) — comparison/reference sample with separate `Club`, `Contract` and `Best Position` fields.

**Use the raw sample for the exercise**; consult the cleaned sample only to validate parsing rules and document differences. These are **alternative versions of player data**, not tables to append or join indiscriminately. File names reflect the original sample labels; verify record counts and uniqueness when importing.

## Fields available
Player `ID`, `Name`, `Nationality`, `Age`, overall rating `↓OVA`, potential `POT`, `Positions`, `Value`, `Wage`, `Release Clause`, technical attributes, height, weight, and preferred foot/foot fields. Raw data combines team and contract details in `Team & Contract`; the cleaned sample provides `Club` and `Contract`. Monetary fields contain currency symbols and abbreviated magnitudes (`K`, `M`) and should be parsed only with documented assumptions.

## Quality cautions
- IDs, names and positions need validation; preserve the original values in a `Raw_Data` query.
- The raw file includes multiline quoted text; use a proper CSV importer rather than splitting by newlines.
- Do not assume cleaned values are authoritative: compare transformations, missing values and mismatches.
- `Value`, `Wage`, and `Release Clause` are **game estimates**, not verified transfer fees, market prices, or employment salaries.
- Missing or unparsable monetary fields should stay unknown rather than being forced to zero.
- Ratings and attribute comparisons describe the FIFA 21 game dataset, not real player ability or professional scouting outcomes.
- This is a selected sample, not all FIFA 21 players.

## Licence and provenance
The sample was described as CC0 by a republisher, but the underlying SoFIFA / EA data rights and suitability for commercial redistribution remain **unverified**. Confirm rights before distributing commercially.
