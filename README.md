# mm-2d-calendar

Myanmar 2D Calendar historical dataset (2012–present).

This repository stores year-wise JSON files containing official 2D calendar data.
Data is structured for direct consumption by mobile and web applications.

---

## Repository Structure

All data is stored by year:

data/{year}.json

Available years:

- data/2012.json
- data/2013.json
- data/2014.json
- data/2015.json
- data/2016.json
- data/2017.json
- data/2018.json
- data/2019.json
- data/2020.json
- data/2021.json
- data/2022.json
- data/2023.json
- data/2024.json
- data/2025.json
- data/2026.json
- data/2027.json (created automatically when year changes)

---

## JSON Format

Each year file follows this structure:

{
  "year": 2026,
  "timezone": "Asia/Yangon",
  "days": {
    "YYYY-MM-DD": {
      "09:30": { "twod": "00" },
      "12:01": { "twod": "00", "set": "1,234.56", "value": "12,345.67" },
      "14:00": { "modern": "00", "internet": "00" },
      "16:30": { "twod": "00" }
    }
  }
}

---

## Rules

- Date format: YYYY-MM-DD
- Only fields with existing data are included
- Weekend or holiday dates may be missing
- 2D values are stored as 2-digit strings
- set and value are stored as strings (comma preserved)
- Year rollover rule:
  - 2026 data → data/2026.json
  - 2027 data → data/2027.json
  - Never append new year data to previous year file

---

## Historical Notes

For years 2012–2022:
- 09:30 contains only { "twod": "00" }
- 16:30 contains only { "twod": "00" }
- No modern, internet, set, or value fields exist for those years.

For years 2023 onward:
- 09:30 → modern + internet
- 12:01 → twod + set + value
- 14:00 → modern + internet
- 16:30 → twod (+ set/value when available)
