# Excel Project 02 — Customer Insights & Segmentation

**Project pages:** 8–9 in the ebook.  
**Tool:** Microsoft Excel (Power Query, COUNTIFS/SUMIFS/AVERAGEIFS, PivotTables, charts).  
**Business scenario:** You are a Junior Customer Insights Analyst at a fashion retailer. Management wants to understand the customer mix, where purchases originate, how spending differs by customer group and which patterns merit further investigation.

## Dataset: use these three existing CSVs

All three are in the [validated Retail Fashion Project 01 data folder](../../datasets/retail-fashion-analytics/project-01/):

1. [customers.csv](../../datasets/retail-fashion-analytics/project-01/customers.csv) — **1,118** customer records, IDs, ages, gender and city.
2. [sales.csv](../../datasets/retail-fashion-analytics/project-01/sales.csv) — **1,200** source transaction records, dates, customer IDs, quantities, discount and return flags.
3. [products.csv](../../datasets/retail-fashion-analytics/project-01/products.csv) — **1,183** source product records with prices and costs. Needed only to estimate sales value.

**Do not download the store file for Project 02.** It is not used here. These three linked CSV files are the complete input bundle, not independent random samples.

## Relationships and verified limitations

- `sales.customer_id` → `customers.customer_id`
- `sales.product_id` → `products.product_id`
- Sales with a **blank customer ID: 51**. Sales with a **missing product record: 2**.
- Sales with missing discount: **53**.
- Customer age range in this sample: **16–69**. Do not apply a grouping scheme that excludes under-18s.
- `gender` has **16** entries marked `???`; classify as **Unknown**, not Female/Male.
- Sample includes only **30 customers appearing in two or more sales** (and just one with 3+). Repeat-buyer shares describe **this sample only**, not a retailer-wide retention rate.
- The `returned` field is an event flag; it does not provide actual refunds.
- No verified transaction selling price, so calculate **estimated sales value**, not actual revenue.

## Estimation rules

`Estimated sales value = quantity × list_price × (1 − discount)`

Compute only where quantity and list price are valid, a product matches, and discount is a valid number from 0 to 1. **Blank discounts are unknown; never automatically treat them as zero.** Exclude missing customer IDs from named customer/age/gender analyses but show their count separately.

For each metric, document the denominator: e.g. customer counts, transactions, or transactions with valid estimated sales value. Avoid implying a share calculated from this sample is representative of all customers.

## The ten questions

**Page 8 — Q1–5**

1. Which customer attributes contain missing, invalid or inconsistent values?
2. Create documented age bands (<18, 18–24, 25–34, 35–44, 45–54, 55+) and standardise unrecognised gender values as Unknown.
3. How are identified customers distributed across age bands, gender categories and cities?
4. What proportion of transactions can be linked to an identified customer, and how many distinct customers made purchases?
5. Which customer cities have the most transactions and highest valid estimated sales value?

**Page 9 — Q6–10**

6. How does average estimated transaction value differ across age bands?
7. How do purchase quantities differ by gender category, including Unknown where applicable?
8. How many identified customers appear in more than one transaction in this sample, and what share is that of identified customers?
9. How does the share of transactions flagged as returned vary by customer age band? Clearly state the denominator.
10. Create an Excel customer insights dashboard with age and city filters, at least three visuals and three evidence-based recommendations.

## Expected submission

- Cleaned and documented Excel workbook with source tabs or Power Query import steps.
- An analysis table/data model and PivotTables or formulas supporting all ten questions.
- A one-page customer insights dashboard.
- A short note of three key findings and the limitations of the sample.

**Solutions are in the ebook, not this public starter repository.**

## Provenance

These three files are derived from the supplied Retail Fashion Analytics dataset. The uploader described the original as MIT-licensed, but source provenance and redistribution rights have not been independently verified.
