---
type: index
tags: [index, resources]
---

# Resources Index

[[start/dashboard|← Back to Dashboard]]

---

> **Resources** = All the knowledge you capture and want to keep.
> Articles, tutorials, guides, useful code, books, videos, etc.

---

## By Category

```dataview
TABLE length(rows) as "Resources"
FROM "resources"
WHERE type = "resource"
GROUP BY category
SORT length(rows) DESC
```

---

## Recent Resources

```dataview
TABLE category as "Category", file.ctime as "Added"
FROM "resources"
WHERE type = "resource"
SORT file.ctime DESC
LIMIT 15
```

---

## Suggested Categories

Organize your resources by topics:

- **Programming** - Code, tutorials, frameworks
- **Design** - UI/UX, tools, inspiration
- **Business** - Marketing, sales, strategy
- **Tools** - Software, apps, services
- **Books** - Book summaries and notes
- **Videos/Courses** - Course notes
- **Articles** - Saved articles
- **Concepts** - Ideas and mental frameworks

---

## Search by Tag

```dataview
LIST
FROM "resources"
WHERE type = "resource"
GROUP BY file.tags
```

---

## Actions

- [[templates/resource|Add New Resource]]

---

## Tips for Resources

1. **Capture fast** - Use template and fill details later
2. **Summary first** - Write your own summary, don't copy/paste everything
3. **Apply learning** - Connect resources with projects where you use them
4. **Review periodically** - Some resources become more relevant over time

---

*Updated: `=date(today)`*
