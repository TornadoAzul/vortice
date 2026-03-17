---
type: index
tags: [index, clients, crm]
---

# Clients Index (CRM)

[[start/dashboard|← Back to Dashboard]]

---

## Active Clients

```dataview
TABLE company as "Company", contact.email as "Email", contact.phone as "Phone", start_date as "Since"
FROM "clients"
WHERE type = "client" AND status = "active"
SORT name ASC
```

---

## Potential Clients

```dataview
TABLE company as "Company", contact.email as "Email"
FROM "clients"
WHERE type = "client" AND status = "potential"
SORT name ASC
```

---

## Inactive Clients

```dataview
TABLE company as "Company", start_date as "Last Contact"
FROM "clients"
WHERE type = "client" AND status = "inactive"
SORT start_date DESC
```

---

## Client Stats

**Total Clients:** `= length(list(file.name FROM "clients" WHERE type = "client"))`
**Active:** `= length(list(file.name FROM "clients" WHERE status = "active"))`
**Potential:** `= length(list(file.name FROM "clients" WHERE status = "potential"))`

---

## Projects by Client

```dataview
TABLE file.folder as "Client", length(rows) as "# Projects"
FROM "projects"
WHERE type = "project"
GROUP BY client
SORT length(rows) DESC
```

---

## Actions

- [[templates/client|Add New Client]]
- [[archive/index|View Archived Clients]]

---

## Quick View

### Upcoming Client Meetings

```dataview
TABLE client as "Client", date as "Date", title as "Topic"
FROM "inbox" OR "resources"
WHERE type = "meeting" AND date >= date(today)
SORT date ASC
LIMIT 5
```

---

*Updated: `=date(today)`*
