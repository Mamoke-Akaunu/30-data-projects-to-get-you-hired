# Excel Project 07 — Spotify Audio Features & Hit/Flop Analysis

**Ebook pages:** 18–19  
**Tool:** Excel — Power Query, Tables, COUNTIFS, MEDIAN, PivotTables, charts and slicers  
**Dataset:** [Six decade-labelled Spotify track samples](../../datasets/spotify-tracks/)  
**Read first:** [Dataset notes and limitations](../../datasets/spotify-tracks/README.md)

## Business scenario
You are a **Junior Music Data Analyst** at a music-insights studio. The editorial team wants to compare audio characteristics of songs labelled `target = 1` and `target = 0` across decade-specific Spotify-derived samples, and assess how attributes vary between the sample groups. Explain that this is descriptive analysis of selected, labelled records rather than a model of commercial success or representative chart data.

## Verified input
Six CSV files: `dataset-of-60s_sample_1000.csv`, `dataset-of-70s_sample_1000.csv`, `dataset-of-80s_sample_1000.csv`, `dataset-of-90s_sample_1000.csv`, `dataset-of-00s_sample_100.csv`, and `dataset-of-10s_sample_1000.csv`. All use the same **19 columns**: track, artist, uri, danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, tempo, duration_ms, time_signature, chorus_hit, sections, target. The 2000s sample is smaller; samples may contain repeated track URIs across periods. The `target` label is not proof of revenue, streams or actual popularity in the population.

## Page 18 — Questions 1–5
1. **Data-quality audit:** Import all six CSV files, add a source-decade label and check missing values, duplicate track URIs, invalid audio-feature ranges and target labels. Which issues require review?
2. **Track inventory:** How many records and distinct track URIs occur in each decade-labelled sample? Explain repeated URIs and why sample sizes differ.
3. **Target distribution:** How many rows are labelled `target = 1` versus `target = 0` in each decade sample? Calculate percentages but do not interpret them as historical hit rates.
4. **Audio features:** Compare median `danceability`, `energy`, `valence` and `acousticness` across target groups using eligible records. Which differences appear most pronounced?
5. **Tempo and duration:** Compare the median `tempo` and `duration_ms` (converted to minutes) by target group and decade. What differences are visible, allowing for the smaller 2000s sample?

## Page 19 — Questions 6–10
6. **Loudness and dynamics:** Compare median `loudness` by decade-labelled sample and target group. Explain that loudness is an audio feature, not a direct measure of success.
7. **Instrumentalness and speechiness:** Compare distributions or documented bands for `instrumentalness` and `speechiness` between target groups. Flag sparse categories.
8. **Audio-feature relationships:** Create scatterplots for `energy` vs `loudness` and `danceability` vs `valence`, using valid records; describe associations without claiming causality.
9. **Decade comparisons:** Compare selected feature medians across the six unevenly sampled decade groups. Explain how sampling and repeated URIs limit any claims about industry-wide trends.
10. **Dashboard:** Create an Excel audio-feature dashboard with decade and target filters, three or more visuals, a data-quality indicator and three carefully qualified insights for music editors.

## Deliverables
Documented workbook with raw import, cleaned table, duplicate audit, analysis and dashboard; answers to all ten questions supported by formulas/PivotTables; recorded denominators and exclusion decisions; descriptive cautions and three qualified insights. Worked solutions belong in the ebook, not this public brief.

## Rights
Spotify-derived source/metadata redistribution rights remain unverified; third-party GPL notice does not establish rights over Spotify data. Confirm publication rights before commercial release.
