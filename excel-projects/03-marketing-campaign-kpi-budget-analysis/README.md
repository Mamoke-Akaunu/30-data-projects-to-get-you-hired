# Excel Project 03 — Marketing Campaign KPI & Budget Analysis

**Ebook pages:** 10–11  
**Tool:** Excel (Power Query, Tables, SUMIFS, IF/IFERROR, PivotTables, charts, slicers)  
**Dataset:** [Download the only required CSV — marketing_campaign_data_messy.csv](../../datasets/marketing-campaigns/marketing_campaign_data_messy.csv)  
**Setup and known issues:** [Dataset README](../../datasets/marketing-campaigns/README.md)

## Business scenario

You are a **Junior Marketing Performance Analyst** at an ecommerce company. The marketing manager has records from several digital advertising channels and wants a trustworthy overview of campaign spending, engagement, and conversion efficiency before planning the next budget. The raw campaign export has duplicated rows, inconsistent channel and status labels, missing conversions and invalid expenses.

## Source and scope

One raw CSV with **2,020 rows and 12 columns**. It is not cleaned in advance: that is part of the project. The source has **2,000 unique campaign IDs**, **19 exact duplicate rows**, **101 Channel values labelled N/A**, **200 blank conversion counts**, **19 negative spend values**, **108 end-before-start date records**, and two separate clicks columns. The reliable primary clicks field is `Clicks ` (a trailing space in the source header), while a second `Clicks` column contains entries for only 40 rows. Document which column you use and why. Never double-count those clicks.

## Questions on Page 10 (1–5)

1. **Data-quality audit:** Identify and count exact duplicate rows, repeated campaign IDs, missing conversions, unknown channels, negative spend values and invalid date ranges. Which issues need investigation rather than automatic deletion?
2. **Standardisation:** Clean channel spellings and normalise the `Active` values to Active/Inactive. Investigate the two `Clicks` columns and select a consistent primary click measure.
3. **Campaign inventory:** How many distinct campaigns are there overall and in each cleaned channel? Keep unknown channels in a separate category.
4. **Spend by channel:** After converting valid spend values to numbers and flagging negative spend, which channels account for the greatest share of nonnegative recorded spend? State excluded rows.
5. **Click-through rate:** Calculate each channel's **CTR = total valid clicks ÷ total valid impressions** using compatible records. Which channels have the highest and lowest rates?

## Questions on Page 11 (6–10)

6. **Cost per click:** Compute weighted **CPC = total valid nonnegative spend ÷ total valid positive clicks** by channel. Compare efficient and expensive channels.
7. **Conversion rate:** Compute weighted **conversion rate = total valid conversions ÷ total valid positive clicks** by channel. Exclude missing conversion counts from both numerator and denominator.
8. **Cost per conversion:** Compute **CPA = total valid nonnegative spend ÷ total valid positive conversions** by channel using consistent eligible records. Which channels have the lowest CPA?
9. **Active vs inactive:** Compare campaign counts, valid spend, CTR and CPA between standardised Active and Inactive records. Explain why correlations are not proof of campaign quality.
10. **Management dashboard:** Build an Excel dashboard with spend, clicks, conversions, CTR, CPC and CPA; filters for channel and campaign status; and **three evidence-based budget recommendations or cautions**. Include data-quality warnings.

## Analysis rules

- Do **not** infer sales revenue or compute ROAS/ROI; there is no revenue data.
- `Conversions` missing is **unknown**, not zero.
- Aggregate ratio-of-sums for CTR, CPC and CPA, not the mean of row-level percentages.
- Check denominator validity; use `IFERROR` only after distinguishing missing data from division by zero.
- Do not assume repeated campaign IDs necessarily mean separate duplicated records.
- Refer to monetary spend as **recorded spend** or monetary units unless you have verified consistent currency metadata.

## Submission

- Excel workbook with `Raw_Data`, `Cleaned_Data`, `Data_Quality_Audit`, `Analysis` and `Dashboard` tabs or equivalent Power Query outputs.
- Written answers to all ten questions supported by formulas/PivotTables.
- Dashboard with at least three visuals and at least two slicers.
- Three practical recommendations, the assumptions used, and the counts of records excluded from each KPI.

**Answers and worked solutions appear separately in the ebook; they are intentionally not provided in this public project folder.**

## Licensing

The dataset was described as MIT-licensed by its uploader. Commercial redistribution rights and publisher provenance have not been independently verified.
