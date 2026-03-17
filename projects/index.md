---
type: index
tags: [index, projects]
---

# Projects Index

[[start/dashboard|← Back to Dashboard]]

---

## In Progress

```dataview
TABLE priority as "Priority", client as "Client", completion as "Progress", due_date as "Due"
FROM "projects"
WHERE type = "project" AND status = "in-progress"
SORT priority DESC, due_date ASC
```

---

## To Start

```dataview
TABLE priority as "Priority", client as "Client", start_date as "Planned Start"
FROM "projects"
WHERE type = "project" AND status = "todo"
SORT start_date ASC
```

---

## Blocked Projects

```dataview
TABLE client as "Client", due_date as "Due"
FROM "projects"
WHERE type = "project" AND status = "blocked"
```

---

## Recently Completed

```dataview
TABLE client as "Client", completion as "Completed", due_date as "Delivered"
FROM "projects"
WHERE type = "project" AND status = "completed"
SORT due_date DESC
LIMIT 10
```

---

## Stats

**Total Projects:** `= length(list(file.name FROM "projects" WHERE type = "project"))`
**In Progress:** `= length(list(file.name FROM "projects" WHERE status = "in-progress"))`
**Completed:** `= length(list(file.name FROM "projects" WHERE status = "completed"))`

---

## Actions

- [[templates/project|Create New Project]]
- [[archive/index|View Archived Projects]]

---

## By Client

```dataview
TABLE length(rows) as "Projects"
FROM "projects"
WHERE type = "project"
GROUP BY client
SORT length(rows) DESC
```

---

*Updated: `=date(today)`*
