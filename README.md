# Shopify ecosystem stats

Counts of live Shopify stores by app, theme, niche and country, from the index behind [insanedev.dev](https://insanedev.dev/shopify/stats/?utm_source=github&utm_medium=dataset&utm_campaign=stats). The index was rebuilt on 29 October 2026 and holds about 950K stores. Apps and themes come from about 766K storefront reads.

The files hold counts only. There are no store domains, names or contacts in them.

Also on Hugging Face: [insanedevhq/shopify-ecosystem-stats](https://huggingface.co/datasets/insanedevhq/shopify-ecosystem-stats).

## Files

| File | What it counts | Rows |
| --- | --- | --- |
| `data/shopify-apps.csv` | Stores per app (our fingerprint list), share of read stores, top 3 countries | 83 |
| `data/shopify-apps.json` | The same, as JSON | 83 |
| `data/shopify-themes.csv` | Stores per theme, themes with 50+ stores | 483 |
| `data/shopify-niches.csv` | Stores per niche keyword | 88 |
| `data/shopify-countries.csv` | Stores per country of the store's address | 214 |
| `data/shopify-app-country.csv` | Stores per app and country, rows with 100+ stores | 1,008 |

## How the numbers are made

- Stores come from public lists of websites (Chrome UX Report, Tranco and Common Crawl). Each domain is checked by DNS for Shopify, then by the store's own public store data. Closed and password-protected stores are left out, and stores behind custom (headless) storefronts aren't counted.
- Apps are detected from a fixed list of fingerprints on the storefront. "Uses Klaviyo" means Klaviyo's code was on the storefront when we read it.
- Themes are the theme name each storefront reports, so custom and renamed themes show up under their own names.
- A store is in a niche when a word in its name, description or domain starts with the niche keyword.
- Country is the country of the store's own address.

The full method is at [insanedev.dev/methodology](https://insanedev.dev/methodology/?utm_source=github&utm_medium=dataset&utm_campaign=stats).

## Updates

The files are regenerated when the index is rebuilt. Each release notes the index build date.

## License

The counts are free to use under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Please credit "insanedev.dev" and link to https://insanedev.dev/shopify/stats/.

## Need store-level lists?

The stores behind these counts, with the e-mails and phones each store publishes, come from [Shopify Store Leads](https://apify.com/insanedev/shopify-store-list?utm_source=github&utm_medium=dataset&utm_campaign=stats) on Apify. It costs $5.50 per 1,000 leads, and the first 25 are free.
