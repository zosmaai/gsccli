# @zosmaai/gsccli

Google Search Console CLI — Search Analytics, URL Inspection, Sitemaps, Indexing API.

## Install

```bash
npm install -g @zosmaai/gsccli
```

## Quick Start

```bash
# Authenticate (OAuth 2.0)
gsccli auth login --client-secret /path/to/client_secret_*.json

# List verified sites
gsccli sites list

# Top queries for last 28 days
gsccli query top-queries --site sc-domain:example.com --row-limit 10

# Compare two periods
gsccli query compare --site sc-domain:example.com \
  --start-date-a 56daysAgo --end-date-a 28daysAgo \
  --start-date-b 28daysAgo --end-date-b today
```

## Common Commands

```bash
# Top queries
gsccli query top-queries --site sc-domain:example.com --row-limit 10

# Top pages
gsccli query top-pages --site sc-domain:example.com --row-limit 10

# By country
gsccli query by-country --site sc-domain:example.com

# By device
gsccli query by-device --site sc-domain:example.com

# URL inspection
gsccli inspect url --site sc-domain:example.com --url https://example.com/page

# Sitemap list
gsccli sitemaps list --site sc-domain:example.com
```

## Output Formats

```bash
gsccli query top-queries --site sc-domain:example.com -f json
gsccli query top-queries --site sc-domain:example.com -f csv
gsccli query top-queries --site sc-domain:example.com -f table
```

## Release

Tag and push to trigger npm publish:

```bash
git tag v1.x.x && git push origin v1.x.x
```

## Links

- Repo: https://github.com/zosmaai/gsccli
- npm: https://www.npmjs.com/package/@zosmaai/gsccli