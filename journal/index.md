---
type: index
tags: [index, journal]
---

# Journal Index

[[start/dashboard|← Back to Dashboard]]

---

## Today's Note

[[templates/daily-note|Create Today's Note]]

---

## Recent Entries

```dataview
LIST
FROM "journal"
WHERE type = "daily"
SORT file.name DESC
LIMIT 30
```

---

## Stats

**Total Entries:** `= length(list(file.name FROM "journal" WHERE type = "daily"))`

---

## By Month

```dataview
TABLE length(rows) as "Entries"
FROM "journal"
WHERE type = "daily"
GROUP BY dateformat(date, "yyyy-MM") as "Month"
SORT rows.date DESC
```

---

## Benefits of Daily Journaling

- **Mental clarity** - Organize your thoughts
- **Track progress** - See how far you've come
- **Reflection** - Learn from your experiences
- **Gratitude** - Focus on the positive
- **Ideas** - Capture day-to-day insights
- **Memory** - Remember important moments

---

## Journaling Tips

1. **Morning or evening** - Choose a fixed time
2. **Don't pressure yourself** - Doesn't have to be perfect
3. **Be honest** - It's your private space
4. **Priorities first** - Top 3 tasks of the day
5. **Reflect at the end** - What did you learn today?

---

*Updated: `=date(today)`*
