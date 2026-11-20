# Wilmar brand and market database

This repository is being used to build a sourced, country-by-country catalogue of Wilmar group and associated-company brands, their product groups, and brand/trademark image assets.

## Where the records are

- [`data/brand_market_products.csv`](data/brand_market_products.csv) — one row per brand × country/market × product-group relationship. This is the main country-level lookup table.
- [`data/brands.csv`](data/brands.csv) — one row per brand, with relationship/ownership and image-asset tracking fields.

Open the files in GitHub or download them and import into Excel, Google Sheets, Airtable, or a database. CSV files are used so they are easy to review and migrate.

## Coverage and evidence

The initial dataset is a **starter inventory, not a complete global trademark register**. It contains brand/market/product information found in the supplied company websites and related official portfolio pages. A parent company’s presence in a country, or its statement that it exports to a number of countries, is not treated as proof that every brand is sold in every such country. Country-specific rows are included only where the cited source supports the association; broader or uncertain associations are explicitly marked for validation.

The `verification_status` field distinguishes source-backed starting records from entries that need an exact brand-to-product or market confirmation. `source_url` links to the source used. Check the source before treating any record as legal proof of trademark ownership, registration, or availability. “Available” here means marketed/listed in a market, not that a trademark is legally available for registration.

## Brand/trademark images

The `brand_asset_url` field is intentionally blank until a direct image from an authorized official source is identified. `asset_status` tracks that work. Do not assume that a logo image on a company website is licensed for reuse; capture the official asset URL and usage/permission details before republication.

## Suggested next steps

1. Confirm the country list and whether the scope is consumer-facing brands only, or also B2B/ingredient and subsidiary brands.
2. Validate each brand-country-product relationship against the relevant local company or brand page.
3. Add official logo/image URLs and, if required, trademark registration number, jurisdiction, owner, class, and registration status from authoritative trademark registries.
4. Add a `last_checked` date whenever a record is reviewed.

## Sources used for this starter

- Yihai Kerry: https://yihaikerry.net/about and https://yihaikerry.net/en/
- Delta Wilmar: https://www.deltawilmar.com/en/ and https://www.deltawilmar.com/wp-content/uploads/2017/04/eng-catalogue.pdf
- AWL Agri Business: https://www.awl.in/our-brands/ , https://www.awl.in/food-essential/ , https://www.awl.in/fmcg/ , https://www.awl.in/about-us/
- Goodman Fielder: https://goodmanfielder.com/brands/
- Wilmar International: https://www.wilmar-international.com/our-businesses/food-products/consumer-products and https://www.wilmar-international.com/our-businesses/food-products/overview

The CSV `source_url` fields provide the closest relevant source for each row.
