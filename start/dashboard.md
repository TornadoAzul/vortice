---
type: dashboard
tags: [start, dashboard]
---

# VORTEX - Command Center

> *"Everything you need, in one place"*

---

## Quick View

### Quick Actions
- [[inbox/quick-capture|Quick Capture]] - Jot something down fast
- [[templates/client|New Client]]
- [[templates/project|New Project]]
- [[templates/task|New Task]]
- [[templates/meeting|New Meeting]]
- [[templates/idea|New Idea]]

### Today is
`=date(today)`

---

## Today's Priorities

### Top 3
- [ ]
- [ ]
- [ ]

---

## Active Projects

```dataview
TABLE status as "Status", client as "Client", completion as "Progress"
FROM "projects"
WHERE type = "project" AND status = "in-progress"
SORT priority DESC
```

**View All:** [[projects/index|Projects Index]]

---

## Active Clients

```dataview
TABLE company as "Company", status as "Status", contact.email as "Email"
FROM "clients"
WHERE type = "client" AND status = "active"
SORT name ASC
LIMIT 10
```

**View All:** [[clients/index|Clients Index]]

---

## Urgent Tasks

```dataview
TASK
FROM "projects" OR "inbox"
WHERE !completed AND priority = "high"
SORT due ASC
LIMIT 10
```

---

## Recent Ideas

```dataview
LIST status
FROM "inbox"
WHERE type = "idea"
SORT file.ctime DESC
LIMIT 5
```

---

## Inbox to Process

```dataview
LIST
FROM "inbox"
WHERE type != "idea"
SORT file.ctime DESC
LIMIT 10
```

**Items in Inbox:** `= length(list(file.name FROM "inbox"))`

---

## Main Navigation

| Section | Description | Quick Access |
|---------|-------------|--------------|
| **INBOX** | Quick capture & processing | [[inbox/quick-capture\|Go →]] |
| **PROJECTS** | Active & completed projects | [[projects/index\|Go →]] |
| **CLIENTS** | CRM & client management | [[clients/index\|Go →]] |
| **AREAS** | Life areas (Health, Finance, etc) | [[areas/index\|Go →]] |
| **RESOURCES** | Knowledge & references | [[resources/index\|Go →]] |
| **ARCHIVE** | Archived projects & clients | [[archive/index\|Go →]] |
| **JOURNAL** | Daily notes & reflections | [[journal/index\|Go →]] |

---

## System Stats

**Total Notes:** `= length(list(file.name FROM ""))`
**Active Projects:** `= length(list(file.name FROM "projects" WHERE status = "in-progress"))`
**Active Clients:** `= length(list(file.name FROM "clients" WHERE status = "active"))`
**Pending Tasks:** `= length(list(file.tasks.text FROM "projects" WHERE !completed))`

---

## System

- [[start/quick-guide|Quick Guide]]
- [[start/claude-context|Claude Context]]
- [[templates|View Templates]]

---

*Last updated: `=date(today)`*
