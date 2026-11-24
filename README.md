# India IPO: Grey Market Premium (GMP) vs Actual Listing Price — 2026

A row-level dataset comparing the **last unofficial grey market premium (GMP)** quoted before listing with the **actual NSE/BSE listing open and day-1 close** for Indian mainboard and SME IPOs.

- **Version:** v2026.11 (data as of 12 Nov 2026; 26 listings, 21 Oct – 11 Nov 2026)
- **Maintainer:** IPO Scouter research desk ("Arjun Mehta" is the desk's disclosed editorial pen name)
- **Live tracker (updated after every listing):** https://iposcouter.com/ipo-gmp-vs-listing-price/
- **Licence:** CC BY 4.0. Free to use, including commercially, with attribution: *"Source: IPO Scouter (iposcouter.com)"* and a link to the live tracker.

## Headline numbers (v2026.11)

| Measure | Value |
|---|---|
| Listings covered | 26 (25 with usable GMP; 1 excluded for conflicting quotes) |
| Opened **below** the GMP-implied price | 12 of 25 |
| Opened **within ±5%** of the GMP-implied price | 16 of 25 |
| Median gap, listing open vs GMP-implied price | 0.0% |
| GMP direction held (see definition) | 16 of 25 (64%) |
| Day-1 close **below** listing open | 11 of 19 listings with a recorded close |

## Files

| File | What it is |
|---|---|
| `ipo_gmp_vs_listing_2026.csv` | One row per IPO listing |
| `DATA_DICTIONARY.md` | Column definitions, units and calculation rules |
| `CHANGELOG.md` | Version history |

## Method

1. **GMP** is an *unofficial* grey-market quote recorded in IPO Scouter coverage from public grey-market trackers on the date shown. It is not an exchange figure, and it is not a forecast. Where trackers quoted a range, both ends are kept and the **midpoint** is used for calculations.
2. **Listing open** and **day-1 close** come from NSE and BSE quote pages. Two day-1 closes are marked *reported* where the exchange figure could not be confirmed.
3. All percentages are **calculated** by IPO Scouter: `(price / issue price − 1) × 100` and `(listing open / GMP-implied price − 1) × 100`, where `GMP-implied price = issue price + GMP midpoint`.
4. **Excluded:** EAAA India Alternatives, because the grey-market quotes conflicted (about ₹10 to ₹65).
5. Sahajanand Medical Technologies uses a GMP taken during bidding, because two trackers could not confirm a post-close figure.

## Limitations

- GMP is informal and thinly traded, especially for SME issues. Treat it as a sentiment reading, not a price.
- The sample is small (26 listings over three weeks) and mixes mainboard and SME issues. It will grow with each monthly version.
- Most mainboard rows don't record the exchange (the issue listed on both NSE and BSE).

## Disclaimer

This dataset is for research and education. It is **not investment advice** and contains no buy, sell or apply recommendations. IPO Scouter is an independent website and is **not registered with SEBI** as an investment adviser or research analyst.

## Citation

> IPO Scouter (2026). *India IPO: GMP vs Actual Listing Price, v2026.11.* https://iposcouter.com/ipo-gmp-vs-listing-price/
