# Spotify Audio Features — Six Decade-Labelled Samples

**Used by:** [Excel Project 07 — Spotify Audio Features & Hit/Flop Analysis](../../excel-projects/07-spotify-audio-features-hit-flop/)

## Files
- `dataset-of-60s_sample_1000.csv`
- `dataset-of-70s_sample_1000.csv`
- `dataset-of-80s_sample_1000.csv`
- `dataset-of-90s_sample_1000.csv`
- `dataset-of-00s_sample_100.csv`
- `dataset-of-10s_sample_1000.csv`

All six have 19 shared columns: `track`, `artist`, `uri`, `danceability`, `energy`, `key`, `loudness`, `mode`, `speechiness`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`, `duration_ms`, `time_signature`, `chorus_hit`, `sections`, `target`.

Add a separate decade label during import before appending files. Preserve each original CSV and retain duplicate URIs for investigation, not automatic deletion. The 2000s sample is substantially smaller than the others. `target` is a provided binary sample label, **not** a verified historical hit rate, streams count, sales figure or forecast of commercial success. Treat findings as descriptive only. Check missing data, values outside expected feature ranges and repeat URIs before analyses. Compute duration in minutes from `duration_ms / 60000` when valid.

## Licence and provenance
A GPL-3.0 notice was supplied for a repackaged source, but this does not independently establish permission to redistribute Spotify API-derived metadata commercially. Source rights remain unresolved; confirm permissions prior to publication.
