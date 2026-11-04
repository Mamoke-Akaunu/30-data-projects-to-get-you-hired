# Messy Marketing Campaigns — Dataset Guide

**Use for:** [Excel Project 03 — Marketing Campaign KPI & Budget Analysis](../../excel-projects/03-marketing-campaign-kpi-budget-analysis/).

## Download

**[marketing_campaign_data_messy.csv](marketing_campaign_data_messy.csv)** — the only CSV needed for Excel Project 03.

This is the full **2,020-row, 12-column** user-uploaded file. It is intentionally messy; readers should work from the raw file rather than from a precleaned answer file.

## Fields and common quality issues

- ` Campaign_ID ` and `Clicks ` contain extra spaces in their header names. **Trim column headers** before use.
- The main clicks count is in **`Clicks ` (with trailing space in the original header)** and is populated in all 2,020 rows. The separate `Clicks` column has values in only 40 rows. Do not sum both fields or silently treat them as one column; inspect discrepancies and explicitly select the primary field.
- `Channel` includes spelling variations such as `Facebok`, `Gogle`, `Tik_Tok`, `E-mail`, and `Insta_gram`, plus **101 `N/A` entries**.
- `Active` mixes `Y`, `Yes`, `True`, `1` and `No`, `False`, `0`; standardise to Active / Inactive.
- `Spend` mixes plain numbers and values with a dollar sign, and includes **19 negative spends**. Check for outliers before reporting aggregate costs.
- `Conversions` is blank for **200 records**. Treat this as unknown, not as zero.
- There are **2,000 distinct Campaign_ID values** and 2,020 rows, including **19 exact duplicate rows**. Repeated IDs are not automatically identical records.
- **108 records** have an end date earlier than the start date, based on parsed dates. Check date validity before duration-based calculations.
- Some dates contain a time component; others do not.

## Recommended metrics

Calculate these on transparent, comparable sets of validated rows, with documented exclusions:

- **Click-through rate (CTR):** `SUM(valid clicks) / SUM(valid impressions)`, requiring valid nonnegative clicks and positive impressions.
- **Cost per click (CPC):** `SUM(valid, nonnegative spend) / SUM(valid, positive clicks)` on rows with both values.
- **Conversion rate:** `SUM(valid conversions) / SUM(valid, positive clicks)` on rows with both values.
- **Cost per conversion (CPA):** `SUM(valid, nonnegative spend) / SUM(valid, positive conversions)` on rows with both values.

**Use the ratio of summed numerators and denominators, not an unweighted average of individual campaign ratios.** Show sample sizes and excluded-record counts. If conversions are missing, their rates and CPA must not be computed as zero.

There is **no sales revenue** field: do **not** calculate ROAS or marketing ROI. The source doesn't establish a consistent billing currency for every record. Use neutral monetary units if needed.

## Excel setup

1. Import the CSV using **Data → Get Data → From Text/CSV**.
2. In Power Query, trim headers, resolve which clicks field to use, and apply documented data type / category standardisation.
3. Keep the raw query separate from the cleaned query.
4. Validate dates, costs, clicks, impressions, conversions and duplicate records.
5. Build PivotTables and a management report answering the ten project questions.

**Licence:** Dataset was described as MIT-licensed by its uploader; provenance and redistribution permissions have not been independently verified.
