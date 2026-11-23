# Travel eSIM plan snapshots

A dataset of 1,079 travel eSIM packages from 21 providers across 114 destinations, recorded by [eSIMox](https://esimox.com/) between 2026-11-02 and 2026-11-08. Every row keeps the original price and currency, the date it was checked and a link to the provider's official product page.

- Dataset page: https://esimox.com/research/plan-snapshots/
- File: [`data/plan-snapshots.csv`](data/plan-snapshots.csv) (identical to https://esimox.com/data/plan-snapshots.csv)

## What it is, and what it is not

This is the editorial sample behind the eSIMox plan comparison. Directory-only brands are excluded. It is not a complete market census or a live price feed: `checked_at` is the research date of each package, and the date range describes those records, not a price history. Prices change often, so confirm the current offer on the provider's site before relying on a row.

## Columns

| Column | Meaning |
|---|---|
| `plan_id` | Identifier of the recorded package |
| `provider` | Provider identifier (for example `airalo`, `saily`) |
| `destination` | Destination identifier (country or region) |
| `gb` | Total data allowance for fixed-data packages; blank for unlimited-labelled packages |
| `days` | Listed validity in days |
| `type` | `fixed` or `unlimited` |
| `price` | Recorded package price |
| `currency` | Original quote currency (USD, EUR, BRL, SGD, AUD) |
| `hotspot` | `allowed`, `limited` or `unknown`; check the exact package conditions |
| `source_url` | Official product source |
| `checked_at` | Research date of the package (YYYY-MM-DD) |
| `price_per_gb` | `price / gb` for fixed-data packages; blank for unlimited. Not a daily rate or an effective high-speed allowance |
| `price_basis` | Qualifications of the price, such as an undiscounted reference price; blank means none recorded |

## Reading it correctly

- Compare prices only within the same currency and equivalent trip requirements. The sample does not convert currencies or include taxes or renewals.
- Unlimited labels do not remove fair-use or hotspot restrictions.
- No market-average price is calculated here.

## Composition

| | |
|---|---|
| Packages | 1,079 (953 fixed, 126 unlimited) |
| Providers | 21 |
| Destinations | 114 |
| Currencies | USD 838, EUR 229, BRL 6, SGD 3, AUD 3 |
| Check dates | 2026-11-02 to 2026-11-08 |

## License and attribution

The compilation is released under [CC BY 4.0](LICENSE). Please credit "eSIMox (esimox.com)" and link to the dataset page. Provider names, product pages and terms belong to their owners; this export does not grant rights to third-party material.

## Corrections

Found an outdated or wrong row? Open an issue with the `plan_id` and an official source, or write to info@esimox.com.
