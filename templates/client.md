---
type: client
name:
company:
status: active
contact:
  email:
  phone:
  linkedin:
start_date:
tags: [client]
---

# {{name}}

## General Information

**Company:** {{company}}
**Status:** {{status}}
**Start Date:** {{start_date}}

### Contact Details
- Email: {{email}}
- Phone: {{phone}}
- LinkedIn: {{linkedin}}
- Other:

## Related Projects

```dataview
LIST
FROM "projects"
WHERE contains(client, this.file.name)
```

## Interaction History

### Last Meeting
Date:
Notes:

### Next Steps
- [ ]

## Notes & Observations

### Preferences
-

### Important Information
-

## Billing

| Project | Amount | Status | Date |
|---------|--------|--------|------|
|         |        |        |      |

## Files & Resources

-

---
**Created:** {{date}}
**Last updated:** {{date}}
