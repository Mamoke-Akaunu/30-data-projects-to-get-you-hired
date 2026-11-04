# Excel Project 04 — Technology Job Market & Data Careers Analysis

**Ebook pages:** 12–13  
**Tool:** Excel — Power Query, Tables, IF/COUNTIFS, PivotTables, charts, slicers  
**Dataset:** [Download the one required CSV](../../datasets/linkedin-jobs/job_postings_anonymized_sample.csv)  
**Read first:** [Dataset notes, columns and source limitations](../../datasets/linkedin-jobs/README.md)

## Business scenario

You are a **Junior Workforce Insights Analyst** at a careers advisory organisation. Your manager wants a descriptive snapshot of technology job advertisements, with a special focus on data-related roles. The team needs to see the mix of role families, work arrangements, employers and job locations, while documenting that the source is a biased sample with messy job titles and invalid application counts.

## Verified input

One CSV, `job_postings_anonymized_sample.csv`, with **2,000 records and 10 columns**.

- **1,504** distinct job IDs and **16** exact duplicate rows.
- **974** nonnumeric values in `no_of_application` (examples: `hours` and `days`).
- **51** blank work types; **6** blank job titles, **6** blank locations and **8** blank company names.
- Descriptive title-keyword classifications in the sample (before any cleaning/deduplication): **107** Data Analyst/BI, **145** Data Engineer, **85** Business Analyst, **12** Data Scientist, **7** Machine Learning, and **1,644** Other Technology.
- The public file omits full job descriptions and has **no structured skills column**. Therefore this project is about **role families and hiring patterns**, not a trustworthy ranking of required skills or salaries.
- `posted_day_ago` is relative to an unknown collection date, not a usable posting timestamp.

## Page 12 — Questions 1–5

1. **Data quality:** Audit the 2,000 records for repeated job IDs, exact duplicates, blank job titles/locations/work types, and invalid application counts. Which records need review?
2. **Role classification:** Clean job titles and use clearly documented title keywords to classify Data Analyst/BI, Data Engineer, Data Scientist, Machine Learning, Business Analyst and Other Technology. How many rows belong to each class?
3. **Role mix:** What share of the sample is data-related versus Other Technology? Show both counts and percentages, with the sample caveat.
4. **Work arrangements:** Among data-related records, what proportions are Remote, Hybrid, On-site and Unknown? Do not confuse `work_type` with the mixed `full_time_remote` field.
5. **Geography:** Which location labels or interpretable countries have the most data-related records? Show Unknown/Unparseable separately rather than guessing.

## Page 13 — Questions 6–10

6. **Employers:** Which employers appear most often in each data-related role family, using documented rules for repeated IDs?
7. **Company size:** Extract employee-count bands from `no_of_employ` where possible. How does the mix of company sizes differ between role families?
8. **Application counts:** Among postings with a valid numeric `no_of_application`, compare median application counts by role family and work arrangement. Report how many records were excluded.
9. **Posting-age categories:** Convert clear `posted_day_ago` values in minutes/hours/days to a common approximate day measure, flag unparseable entries and compare descriptive recency bands. Do **not** infer calendar dates or current labour-market trends.
10. **Dashboard:** Create an Excel snapshot dashboard with role, location and work-arrangement filters, at least three visuals, a data-quality indicator and three carefully qualified insights for career advisers.

## Deliverables

- A documented Excel workbook with raw import, cleaned table, validation audit and role-family classification.
- PivotTables / formulas answering all ten questions, plus a recruiter-facing dashboard.
- Brief notes describing the sample selection, invalid application-count records, title-based classification limits and the absence of structured skill data.

**Answers:** Kept in the ebook's Excel Solutions section, not here.

## Provenance

The dataset was originally described as Open Data Commons DbCL 1.0. The upload source and underlying platform-derived redistribution rights are unverified. Public sample excludes hiring-person details and long job descriptions.
