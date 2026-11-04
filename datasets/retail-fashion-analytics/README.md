# Retail Fashion Analytics

**Recommended Excel starter dataset:** [Project 01 — Sales Performance Analysis](project-01/)

The Project 01 folder contains a relationally matched, **1,200-transaction sample** from the user-supplied Retail Fashion Analytics source files. Its `README.md` explains the joins, source-quality issues and calculation assumptions. Start there, not with independently sampled files.

## Project 01 files

- [sales.csv](project-01/sales.csv) — 1,200 transactions
- [products.csv](project-01/products.csv) — 1,183 related products
- [customers_part_01.csv](project-01/customers_part_01.csv), [part 02](project-01/customers_part_02.csv), [part 03](project-01/customers_part_03.csv) — 1,118 unique matching customers in three files to append
- [store_data.csv](store_data.csv) — complete original store dimension (5 rows)

The parent folder also preserves the originally uploaded full `customer_data.csv`, which contains an email column not necessary for Project 01. The Project 01 customer extracts omit that field.

## Important analytical limits

The dataset includes product list prices, costs, quantity and discounts, but no actual transaction selling price or refund amount. Calculate **estimated sales value** and **estimated gross margin**, not audited revenue/profit. Returns are represented by flags.

## Licence

The original dataset was described by its uploader as MIT licensed. The underlying publication and redistribution rights have not been independently verified.