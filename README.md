# Yellow Key: open / closed switch

The site www.yellowkey.co.il reads `status.json` from this repo. Edit it to
open or close the site right now, without touching the site itself. The site
follows within about 5 minutes.

## איך משנים (מהטלפון)

1. פותחים בדפדפן: https://github.com/AntonP210/yellowkey-status/edit/main/status.json
2. מוחקים את מה שכתוב ומדביקים אחת מהדוגמאות למטה, עם התאריך של היום.
3. לוחצים **Commit changes** ושוב **Commit changes**.

## דוגמאות

פתוח עכשיו, עד 14:00 היום:

```
{ "mode": "open", "date": "2026-11-08", "until": "14:00" }
```

פתוח עכשיו, עד סוף היום:

```
{ "mode": "open", "date": "2026-11-08" }
```

סגור עכשיו (למשל ביום מחלה), עד סוף היום:

```
{ "mode": "closed", "date": "2026-11-08" }
```

סגור עכשיו ונפתחים ב־20:00 היום:

```
{ "mode": "closed", "date": "2026-11-08", "until": "20:00" }
```

חזרה לשעות הרגילות:

```
{ "mode": "auto" }
```

## חשוב לדעת

- `date` הוא התאריך שבו השינוי חל (שנה-חודש-יום). ביום אחר האתר מתעלם ממנו
  וחוזר לשעות הרגילות, כך ש"פתוח" שנשכח לא נשאר למחרת.
- `until` (לא חובה) הוא השעה שבה השינוי נגמר. בלעדיו, הוא נגמר בחצות.
- אם יש טעות בקובץ, האתר פשוט ממשיך לפי השעות הרגילות.
- זה משנה רק את האתר. שעות הפעילות ב־Google Maps ובמודעות נשארות בנפרד.
