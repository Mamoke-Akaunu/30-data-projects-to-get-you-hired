# Technology Job Market — Anonymised Job Posting Sample

**Used by:** [Excel Project 04 — Technology Job Market & Data Careers Analysis](../../excel-projects/04-technology-job-market-data-careers/)

## Download the dataset

[**job_postings_anonymized_sample.csv**](job_postings_anonymized_sample.csv) — the **only CSV** used in the project.

It contains **2,000 source records and 10 columns**, derived from the user-uploaded LinkedIn-style job-postings dataset. The public sample omits hiring-person names, profile URLs, job descriptions, company IDs and redundant blank columns.

## Columns

- `job_ID` — source posting identifier; repeated values require investigation.
- `job` — unstandardised title, which may contain employer, seniority, location, compensation text or remote labels.
- `location` — free-text place, not a reliably normalised city/state/country hierarchy.
- `company_name` — employer name.
- `work_type` — On-site, Remote, Hybrid or blank.
- `full_time_remote` — mixed employment type and seniority, such as `Full-time · Associate`.
- `no_of_employ` — text combining company employee-count band and sometimes industry.
- `no_of_application` — mixed numeric values and invalid tokens (`hours`, `days`, etc.).
- `posted_day_ago` — relative posting age as strings such as `8 hours` or `26 minutes`.
- `alumni` — source text sometimes containing an alumni count.

## Verified sample issues

- **2,000 rows**, **1,504 distinct job IDs** and **16 exact duplicate rows**.
- **974 rows** contain nonnumeric `no_of_application` values; do not treat these as valid application counts or zero.
- **51 rows** have missing `work_type`.
- **6 missing job titles**, **6 missing locations** and **8 missing company names**.
- The data covers **many technology roles**. A basic, explicitly documented title classifier identified 107 Data Analyst/BI, 145 Data Engineer, 85 Business Analyst, 12 Data Scientist and 7 Machine Learning rows, with most records classified as Other Technology.
- Only the job title is available for role classification. **The public sample does not support a reliable analysis of requested technical skills** because detailed job requirements were intentionally removed.
- `posted_day_ago` lacks the collection date. Convert relative units for descriptive grouping only; do **not** infer current hiring trends or actual posting dates.
- This is a selection from scraped platform records, **not a representative census** of the technology job market.

## Recommended approach

Use Excel Power Query to preserve a `Raw` query, clean and standardise fields, investigate repeated IDs, and create your own role-family and location categories. Parse `no_of_employ` only where patterns are interpretable. Show unknown or invalid values separately.

Report the denominator used for each analysis. Distinguish **record counts** from **distinct job IDs** and mark application-count summaries as based only on valid numeric values.

## Licence and privacy

Open Data Commons DbCL 1.0 was cited for the uploaded dataset, but the origin and redistribution rights of underlying LinkedIn-sourced content have not been independently verified. The public sample excludes unnecessary personal profile information, although that does not by itself establish commercial redistribution rights.
