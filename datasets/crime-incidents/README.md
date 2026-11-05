# Synthetic Crime Incident Records — Verified Sample

**Used by:** [Excel Project 08 — Crime Incident Patterns & Data Quality Analysis](../../excel-projects/08-crime-incident-patterns-data-quality/)

## Download
[**crime_incidents_sample_2999.csv**](crime_incidents_sample_2999.csv) — the sole dataset required for Project 08.

This file contains **2,999 synthetic incident records and 33 columns**. Two pairs of records had been accidentally concatenated in the old `crime_incidents_sample_2000.csv`; these line breaks were repaired and the file renamed to match its actual count. Source field values are otherwise retained for learner cleaning and audit.

## Fields used in the project
- `incident_id`, `crime_type`, `district`, `city`, `state`, `incident_datetime`
- `latitude`, `longitude` — supplied coordinates, not guaranteed to match the text address or represent accurate geography
- `case_status`, `resolution`, `num_arrests`, `severity`, `weapon_used`
- `property_loss_usd`, `reported_online`

Other source fields include synthetic officer, suspect and victim identifiers/names, addresses and phone numbers. These **are not needed for project outputs**. Do not publish individual-level identifiable rows in the dashboard.

## Verified data issues
- **2,999 records**, **33 columns**; **56 repeated incident IDs** (including exact duplicates) in the original sample.
- **202 blank** incident dates, plus dates with mixed formatting (including day–month–year text requiring locale-aware parsing).
- **148 blank latitude** and **170 blank longitude** values; at least **241 invalid or absent latitudes** and **170 invalid or absent longitudes** using valid geographic bounds.
- **99** negative/unparseable nonempty arrest counts; **200** blank arrest counts.
- Mixed spellings and casing in `crime_type`, `district`, `case_status`, `resolution` and `reported_online`.
- **394** blank/NA case statuses; **547** blank/NA resolutions.
- Missing, negative or anomalous `property_loss_usd` values may require explicit treatment.

Retain a `Raw_Data` copy and document whether exact duplicate rows are excluded from specific summaries. **Repeated IDs are not proof that every underlying record is redundant**. Preserve Unknown/Unparseable categories and report denominators.

## Limits
This is **synthetic practice data**, not actual police crime statistics. Incident counts are not rates: no population or exposure denominator is provided. Coordinates may be fabricated, invalid or geographically inconsistent; describe district/city tables as sample distributions, **not validated real-world hotspots**. Case status and resolution are descriptive labels, not justice-system effectiveness measures; avoid causality and enforcement recommendations from synthetic records.

## Rights and provenance
The files are described as synthetic, and a CC0 status was reported by the data uploader; independent confirmation of the original publication and redistribution rights has not been completed.
