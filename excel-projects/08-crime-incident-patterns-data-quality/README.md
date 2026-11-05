# Excel Project 08 — Crime Incident Patterns & Data Quality Analysis

**Ebook pages:** 20–21  
**Tool:** Excel — Power Query, Tables, COUNTIFS, IF/IFS, PivotTables, charts and slicers  
**Dataset:** [Download the one verified CSV](../../datasets/crime-incidents/crime_incidents_sample_2999.csv)  
**Read first:** [Dataset notes and limitations](../../datasets/crime-incidents/README.md)

## Business scenario
You are a **Junior Public Safety Data Analyst** preparing a quality-controlled practice report from synthetic incident records for an operations-training team. The manager wants descriptive comparisons of incident categories, reporting periods, district/city labels and case-status outcomes while documenting duplicates, invalid coordinates and incomplete records. This is **not evidence of real crime rates, real geographic hotspots or police effectiveness**.

## Verified input
The corrected CSV has **2,999 records and 33 columns**. The published file fixes two accidental joins between records and renames a misleading 2,000-row filename. It retains 56 duplicate incident IDs / exact duplicate records and messy fields for auditing; synthetic names, phone numbers and addresses are not needed in the analysis.

## Page 20 — Questions 1–5
1. **Data quality:** Audit repeated `incident_id` values, exact duplicates, missing or unparseable `incident_datetime`, invalid coordinates, negative `num_arrests`, and inconsistent categories. Which rows need review rather than silent deletion?
2. **Incident categories:** Standardise documented `crime_type` variants and count records by standardised category. Which five categories have the most records in the selected synthetic sample?
3. **Reporting periods:** Parse valid `incident_datetime` values using documented date-format rules. Compare incident counts by month and day of week. How many rows were excluded for missing or uncertain dates?
4. **Area comparison:** Standardise `district` labels and count records by district and city. Which labels have the most records? Why are these sample counts not validated geographic hotspots or crime rates?
5. **Case status:** Standardise `case_status` and `resolution` labels, retain Unknown, and compare status counts and percentages across standardised crime categories. What descriptive differences appear?

## Page 21 — Questions 6–10
6. **Arrest-count quality:** For `num_arrests`, separate valid nonnegative counts from missing/invalid values. Compare total valid recorded arrests and the percentage of records with positive arrests across crime categories; report exclusions.
7. **Severity patterns:** Standardise `severity` labels into explicitly documented groups; compare incident counts and case-status mix by group, keeping Unknown separate.
8. **Reported online:** Normalise `reported_online` to Yes, No and Unknown, and compare proportions by crime category and district. Do not interpret the indicator as a digital-reporting adoption rate for a real population.
9. **Property-loss distributions:** For valid nonnegative `property_loss_usd`, compare median reported losses by crime category and city. Show excluded, missing and negative values, and avoid presenting sample totals as real economic impact.
10. **Dashboard:** Create an Excel synthetic-incident dashboard with crime-category, district and year filters, at least three visuals, an audit/exclusion indicator and three carefully qualified operational data-quality insights.

## Deliverables
- Excel workbook with `Raw_Data`, `Cleaned_Data`, `Data_Quality_Audit`, `Analysis` and `Dashboard` (or equivalent Power Query outputs).
- Documented standardisation, date parsing and eligibility rules; counts of excluded records.
- Formula/PivotTable-backed answers to Questions 1–10 and at least three dashboard visuals.
- Three qualified insights with clear synthetic-data and nonrepresentativeness cautions; no individual-level identifying information in outputs.

**Answers:** Kept in the ebook's solutions section, not the starter repository.
