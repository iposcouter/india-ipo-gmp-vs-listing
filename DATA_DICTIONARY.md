# Data dictionary — ipo_gmp_vs_listing_2026.csv

| Column | Type | Tag | Definition |
|---|---|---|---|
| `id` | int | — | Row number in listing-date order |
| `ipo_name` | text | Confirmed | Company name as listed |
| `segment` | text | Confirmed | `Mainboard` or `SME` |
| `exchange_sme` | text | Confirmed | `NSE SME` or `BSE SME` for SME issues; blank for mainboard (listed on NSE and BSE) |
| `issue_price_inr` | number | Confirmed | Final issue price (₹) from the RHP/prospectus |
| `gmp_low_inr` / `gmp_high_inr` | number | Reported (unofficial) | Lowest and highest grey-market premium quoted on `gmp_observed_date`. Equal when a single value was quoted. Blank if excluded |
| `gmp_mid_inr` | number | Calculated | Midpoint of the low and high GMP |
| `gmp_observed_date` | date (YYYY-MM-DD) | Reported | Date of the last GMP reading before listing. For ranges, the last day of the observation window (see `notes`) |
| `gmp_implied_price_inr` | number | Calculated | `issue_price_inr + gmp_mid_inr` |
| `listing_date` | date | Confirmed | First trading day |
| `listing_open_inr` | number | Confirmed | Listing-day opening price (NSE/BSE quote page) |
| `open_vs_issue_pct` | % | Calculated | `(listing_open / issue_price − 1) × 100` |
| `open_vs_gmp_implied_pct` | % | Calculated | `(listing_open / gmp_implied_price − 1) × 100`. Negative means it opened below what GMP implied |
| `day1_close_inr` | number | Confirmed / Reported | Day-1 closing price; blank if not recorded |
| `day1_close_vs_issue_pct` | % | Calculated | `(day1_close / issue_price − 1) × 100` |
| `day1_close_source_note` | text | — | `reported` = media figure, not exchange-confirmed; `BSE` = BSE quote page |
| `gmp_direction_held` | Yes/No | Calculated | **Yes** if GMP mid > 0 and open > issue price, or GMP = 0 and open = issue price. Otherwise **No** |
| `excluded_from_gmp_stats` | yes/no | — | `yes` = left out of GMP statistics (conflicting quotes) |
| `notes` | text | — | Row-specific caveats |

Percentages are rounded to 2 decimals in the CSV. The live web page rounds to 1 decimal, so two rows differ by 0.05 points from rounding only.
