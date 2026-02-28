# mm-2d-calendar (Private)

Myanmar 2D Calendar historical dataset (2012–present).  
Source-of-truth repo for year-split JSON files.

> NOTE (Private Repo):
> This repository is private, so public clients (mobile/web apps) cannot fetch `raw.githubusercontent.com` or CDN URLs without authentication.
> Recommended: publish JSON snapshots to your own public API/hosting (VPS) for app/web consumption.

## Data Layout

- `data/{year}.json`
  - Example: `data/2026.json`, `data/2027.json` (auto-created when year changes)

## JSON Schema (per year)

```json
{
  "year": 2026,
  "timezone": "Asia/Yangon",
  "days": {
    "YYYY-MM-DD": {
      "09:30": { "modern": "00", "internet": "00" },
      "12:01": { "twod": "00", "set": "1,234.56", "value": "12,345.67" },
      "14:00": { "modern": "00", "internet": "00" },
      "16:30": { "twod": "00", "set": "1,234.56", "value": "12,345.67" }
    }
  }
}
