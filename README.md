# Indian Express daily digest (web scraping, 2022)

A small Python notebook I wrote in 2022 to build a personal daily reading list from the web edition of *The Indian Express*.

It visits a handful of sections (UPSC current affairs, Opinion, Explained, Science, Business: Economy and Banking & Finance), collects each article's title, summary, publish date and link, keeps only the day's articles, and saves them to a single CSV:

```
Nov-19-2026 IE extracts.csv
```

## How it works

1. Request each section page and parse it with BeautifulSoup.
2. Collect article links from the section's main content block.
3. Visit each article and pull the title, synopsis and publish date.
4. Clean the dates with pandas and keep articles published today.
5. Combine all sections into one table and write it to CSV.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook indian_express_daily_digest.ipynb
```

## Status

This is an archived learning project. News sites change their page structure often, so the CSS selectors written in 2022 may no longer match the live site, and the notebook may need updating before it runs cleanly.

For personal use only. Article content belongs to *The Indian Express*; please respect the site's terms of use and don't redistribute scraped text.
