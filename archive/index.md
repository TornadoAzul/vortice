---
type: index
tags: [index, archive]
---

# Archive Index

[[start/dashboard|← Back to Dashboard]]

---

> Completed projects and inactive clients that you no longer need in the main dashboard.

---

## Archived Projects

```dataview
TABLE client as "Client", due_date as "Completed", completion as "Progress"
FROM "archive"
WHERE type = "project"
SORT due_date DESC
```

---

## Archived Clients

```dataview
TABLE company as "Company", status as "Final Status"
FROM "archive"
WHERE type = "client"
SORT file.name ASC
```

---

## Archive Stats

**Archived Projects:** `= length(list(file.name FROM "archive" WHERE type = "project"))`
**Archived Clients:** `= length(list(file.name FROM "archive" WHERE type = "client"))`

---

## When to Archive

**Projects:**
- Completed more than 3 months ago
- No longer need to see in active dashboard
- Want to keep history but not quick access

**Clients:**
- No projects in 6+ months
- Business relationship ended
- Contact or company change

---

## How to Archive

1. Move file from original folder to `archive/`
2. Update status if needed
3. File will automatically disappear from active views

---

*Updated: `=date(today)`*
