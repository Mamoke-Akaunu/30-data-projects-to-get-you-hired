# Excel Project 01 — Sales Performance Analysis

This is a **relationally matched source-data subset** for the first project in *30 Data Projects to Get You Hired*. The dataset files were selected using transaction IDs and their actual matching product/customer IDs, unlike the earlier independent samples.

## Files

- `sales.csv` — **1,200 transactions** from the provided Retail Fashion sales data.
- `products.csv` — **1,183 matching product records** extracted from the full original product table.
- `customers_part_01.csv`, `customers_part_02.csv`, `customers_part_03.csv` — together **1,118 matching customers**, with the email field intentionally removed. **Append these three files into one customer table in Excel Power Query**, before joining to sales.
- [`store_data.csv`](../store_data.csv) — **five original stores**, retained in the parent folder.

## Relationships

`sales.product_id = products.product_id`

`sales.customer_id = customers.customer_id`

`sales.store_id = stores.store_id`

## Verified source issues

Of 1,200 sales transactions:
- **2** have no matching product record.
- **51** have a blank customer ID.
- **0** nonblank customer IDs lack a matching customer record.
- **8** have no matching store record.
- **53** have a missing discount.

These issues are retained intentionally for Question 1 and Question 2. The separate old files named `sales_sample_3000.csv` and `products_sample_3000.csv` in the parent folder **should not be used together**, because their product keys were selected independently.

## Financial assumptions

The source contains product `list_price` and `cost_price`, **not verified transaction selling prices**.

- **Units sold:** sum valid numeric nonnegative `quantity` values.
- **Estimated sales value:** `quantity * list_price * (1 - discount)`, only when quantity, product match, list price and numeric discount from 0 to 1 are valid. Do **not** assume that a blank discount is 0; flag or exclude it and disclose this.
- **Estimated gross contribution:** estimated sales value minus `quantity * cost_price`.
- **Estimated gross margin:** estimated gross contribution divided by estimated sales value where positive.

The `returned` field is a flag, not a refund amount or refund date. Some products have list prices below cost: investigate them rather than silently correcting them. Interpret financial results as **estimates**, not audited revenue or accounting profit.

## Excel workflow

1. Download this folder's sales, products and all three customer part files, plus the linked store CSV.
2. Import them into Excel via **Data → Get Data → From Text/CSV**.
3. Append the three customer part files, then join sales to products, customers and stores by IDs.
4. Keep unmatched transactions visible in the quality audit.
5. Answer the ten project questions and build a presentation-ready PivotTable dashboard.

**Licence note:** The source uploader claimed MIT licensing. We have not independently verified the original publication's redistribution rights.