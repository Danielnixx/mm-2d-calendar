# mm-2d-calendar

Myanmar 2D Calendar historical dataset (2012–present).

## Data Structure

All data is stored year-wise:

data/{year}.json

Example:
data/2026.json
data/2027.json

## JSON Format

```json
{
  "year": 2026,
  "timezone": "Asia/Yangon",
  "days": {
    "2026-02-27": {
      "09:30": { "modern": "37", "internet": "30" },
      "12:01": { "twod": "41", "set": "1,539.04", "value": "51,341.96" },
      "14:00": { "modern": "57", "internet": "97" },
      "16:30": { "twod": "64", "set": "1,528.26", "value": "104,314.15" }
    }
  }
}
