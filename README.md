# Yellow Key: open / closed switch

The site www.yellowkey.co.il reads `status.json` from this repo. Edit it to
open or close the site right now, without touching the site itself. The site
follows within about 5 minutes.

## How to change it (from your phone)

1. Open in the browser: https://github.com/AntonP210/yellowkey-status/edit/main/status.json
2. Delete what's there and paste one of the examples below, with today's date.
3. Press **Commit changes**, then **Commit changes** again.

## Examples

Open now, until 14:00 today:

```
{ "mode": "open", "date": "2026-11-08", "until": "14:00" }
```

Open now, until the end of the day:

```
{ "mode": "open", "date": "2026-11-08" }
```

Closed now (for example, a sick day), until the end of the day:

```
{ "mode": "closed", "date": "2026-11-08" }
```

Closed now, reopening at 20:00 today:

```
{ "mode": "closed", "date": "2026-11-08", "until": "20:00" }
```

Back to the regular hours:

```
{ "mode": "auto" }
```

## Good to know

- `date` is the day the change applies to (year-month-day). On any other day
  the site ignores it and goes back to the regular hours, so a forgotten
  "open" never carries into the next day.
- `until` (optional) is the time the change ends. Without it, it ends at
  midnight.
- If the file has a mistake, the site simply keeps to the regular hours.
- This only changes the website. Your hours on Google Maps and in your ads stay
  separate.
