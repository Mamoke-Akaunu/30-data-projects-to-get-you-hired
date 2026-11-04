# Excel Project 01 — Sales Performance Analysis

**Tool:** Excel  
**Project:** Analyse retail sales, product categories, stores, customer age groups and estimated gross margins.

## Download these four files

| File | Rows | What it contains |
|---|---:|---|
| [sales.csv](sales.csv) | 1,200 | Transactions, dates, product/store/customer keys, quantities, discounts and return flags |
| [products.csv](products.csv) | 1,183 | Matching product records, categories, list prices and costs |
| [customers.csv](customers.csv) | 1,118 | Matching customer ages, genders and cities |
| [stores.csv](stores.csv) | 5 | Store names and regions |

**These four CSV files are the complete data bundle for Project 01.** No other dataset is needed. Download the CSVs into the same folder on your computer.

## Join keys

- `sales.product_id` → `products.product_id`
- `sales.customer_id` → `customers.customer_id`
- `sales.store_id` → `stores.store_id`

Use **Power Query merges**, **XLOOKUP** or Excel's **Data Model** to relate these tables. Do not match rows by their positions.

## Data-quality issues intentionally retained

Of the **1,200** transactions:

- **2** do not match a product.
- **51** have blank customer IDs.
- **8** do not match a store.
- **53** have a blank discount.

These are genuine issues from the supplied source, intentionally kept for the first two project questions. Identify unmatched rows before calculations; do not silently delete them.

## Calculation rules for Questions 3–10

The files do **not** contain a verified transaction selling-price or actual refund amount. Accordingly, use **estimates**, not audited revenue or accounting profit.

- **Units sold:** Sum non-negative, valid numeric quantities.
- **Estimated sales value:** `quantity × list_price × (1 − discount)` on transactions where the product matches and all required values are valid, including discounts between 0 and 1.
- **Estimated gross contribution:** Estimated sales value − `quantity × cost_price`.
- **Estimated gross margin %:** Estimated gross contribution ÷ estimated sales value, only when estimated sales value is greater than zero.
- **Unknown discounts:** Treat blanks as unknown; do not automatically interpret blanks as zero. Explain exclusions.
- **Returns:** `returned` is just a flag. Do not infer a refund amount or reverse sales automatically.
- **Age groups:** Create explicit bands from customer ages, such as 18–24, 25–34, 35–44, 45–54, 55+.
- **Time periods:** Convert transaction dates to Excel dates before grouping by month and year.

Some products have costs above list price. Keep those values visible and discuss the resulting estimated negative margins.

## How to get started

1. Download all **four CSV files** linked above.
2. Open Excel and import each file using **Data → Get Data → From Text/CSV**.
3. Check the four datasets for missing values, invalid entries and unmatched IDs.
4. Build a validated analysis table or Excel Data Model using the keys above.
5. Answer **Questions 1–10** in the ebook, create PivotTables and build a management-ready dashboard.
6. Save your completed workbook and a brief summary of three actionable findings.

The ebook contains the worked solutions. This folder provides **starter data only**.

## Provenance and rights

This linked sample was prepared from the uploaded Retail Fashion Analytics data. The uploader reported an MIT licence, but the original publishing source and redistribution rights have not been independently verified.
