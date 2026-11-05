# FIFA 21 Player Ratings & Value Analysis — Dataset Notes

**Used by:** [Excel Project 06](../../excel-projects/06-fifa21-player-ratings-value/)

## Selected source and current status

The chosen analysis source is the **original, uncleaned FIFA 21 raw CSV** supplied for Project 06: `fifa21_raw_data(2).csv` (local upload name). Verification of that upload found:

- **18,979 data records and 77 columns**.
- **18,978 distinct player IDs**; one player ID occurs twice. This has **not** been removed.
- Raw fields include `ID`, `Name`, `Nationality`, `Age`, `↓OVA`, `POT`, `Positions`, `BP`, `Value`, `Wage`, `foot`, `PAC`, `SHO`, `PAS`, `DRI`, `DEF`, `PHY`, and `Team & Contract`.
- Height/weight values and monetary labels retain the source formats.

**Do not clean, deduplicate, reformat, or overwrite the selected raw data yet.** Assess the source against the final uploaded questions first. Worked solutions and a cleaned reference are deferred until the question set has been validated and approved.

## Repository file status

The existing repository files `fifa21_raw_sample_1000.csv` and `fifa21_cleaned_sample_1000.csv` are **older, smaller samples** and are not the selected full raw source. Their names do not reflect their actual record counts. Do not append these samples to the full source or use them for full-dataset answers.

**Migration not yet completed:** This README update does **not** mean the new 18,979-record upload has been committed to this GitHub folder. The old samples are retained until the replacement can be verified in the repository, after which irrelevant files can be reviewed for removal.

## Planned analysis process

1. Import the full raw CSV without changing the source.
2. When Pages 16 and 17 are supplied, check whether every question is supported by actual fields and data.
3. Review all ten questions for overlap, and obtain approval for any proposed changes.
4. Only after the questions pass and approval is given, prepare verified answers and any separately authorised cleaned working copy.

## Important interpretation cautions

- The raw file includes multiline quoted cells; import as CSV with proper quote handling.
- Preserve the repeated ID during the initial audit: it is a data-quality finding, not a reason to silently change the source.
- Parse euro-labelled K/M values only in derived analysis columns; do not rewrite the raw values.
- FIFA 21 ratings, values and wages are **game data**, not real-world scouting assessments, transaction prices or verified salaries.
- The source is not guaranteed to be representative of all football players.

## Provenance and redistribution

The source is a third-party FIFA 21 player dataset. Its underlying origin and permissions for public or commercial redistribution remain **unverified**. Public accessibility is not itself a redistribution licence. Obtain appropriate clearance before publishing the full third-party CSV for download.
