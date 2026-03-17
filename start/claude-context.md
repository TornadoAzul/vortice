---
type: system
tags: [system, claude, ai, context]
---

# Claude Context - VORTEX System

[[start/dashboard|← Back to Dashboard]]

---

> This file provides context for Claude Code (or any AI assistant) to understand and work with your VORTEX system effectively.

---

## System Overview

**Name:** VORTEX (Personal Management System)
**Platform:** Obsidian Vault
**Purpose:** Unified system for managing projects, clients, knowledge, and life
**Structure:** Folder-based organization with templates and linking

---

## Folder Structure & Purpose

```
vortex/
├── start/           # System home (dashboard, guides, this file)
├── inbox/           # Quick capture & unprocessed items
├── projects/        # Active & completed projects
├── clients/         # CRM - all client information
├── areas/           # Life areas (ongoing, no end date)
├── resources/       # Knowledge base & references
├── archive/         # Completed/inactive projects & clients
├── journal/         # Daily notes & personal reflections
├── templates/       # Note templates for quick creation
└── media/           # Attachments & files
```

---

## Core Concepts

### 1. Projects vs Areas
- **Projects** = Time-bound work with a defined end (e.g., "Build website for Acme Corp")
- **Areas** = Ongoing life spheres (e.g., "Health", "Career", "Finances")

### 2. Linking System
- All entities link together via `[[wiki-links]]`
- Projects link to clients
- Tasks link to projects
- Meetings link to clients & projects
- Creates interconnected knowledge graph

### 3. Metadata (Frontmatter)
Every note has YAML frontmatter for:
- Type classification
- Status tracking
- Priority levels
- Dates & deadlines
- Tags for organization

### 4. Dynamic Views
Uses Dataview plugin for:
- Auto-updating lists
- Statistics & counts
- Filtering by status/type
- Aggregating related notes

---

## Templates Available

| Template | File | Purpose |
|----------|------|---------|
| Client | `templates/client.md` | Client/contact management |
| Project | `templates/project.md` | Project tracking |
| Task | `templates/task.md` | Individual task management |
| Meeting | `templates/meeting.md` | Meeting notes & follow-ups |
| Idea | `templates/idea.md` | Idea capture & development |
| Daily Note | `templates/daily-note.md` | Daily journaling |
| Resource | `templates/resource.md` | Knowledge capture |

---

## Status Systems

### Projects
- `todo` - Planned, not started
- `in-progress` - Currently working
- `blocked` - Waiting on external factor
- `completed` - Finished
- `paused` - Temporarily on hold

### Clients
- `active` - Current working relationship
- `potential` - Lead/prospect
- `inactive` - Not currently working together

### Tasks
- `todo` - Not started
- `in-progress` - Currently doing
- `blocked` - Cannot proceed
- `completed` - Done
- `paused` - Temporarily stopped

### Ideas
- `new` - Just captured
- `researching` - Investigating feasibility
- `validated` - Worth pursuing
- `developing` - Building/implementing
- `implemented` - Successfully deployed
- `discarded` - Decided not to pursue

---

## File Naming Conventions

- **Format:** `lowercase-with-dashes`
- **Descriptive:** `acme-corp-website-redesign` not `project-1`
- **No numbers prefix:** Avoid `01-project-name`
- **Consistent:** Same pattern across all files

---

## When Helping Users

### Creating New Notes
1. Ask which type (client, project, task, etc.)
2. Use appropriate template from `templates/`
3. Help fill in metadata
4. Save in correct folder with proper naming
5. Create necessary links to related notes

### Finding Information
1. Check relevant index file first
2. Use grep/search for content
3. Look in appropriate folder
4. Check dashboard for quick access

### Organizing & Structuring
1. New items → `inbox/` first
2. Process → Move to proper folder
3. Link → Connect related notes
4. Update → Keep statuses current
5. Archive → Move old items to `archive/`

### Suggesting Improvements
- Respect user's workflow preferences
- Build on existing structure
- Maintain consistency with templates
- Keep it simple and usable

---

## Common User Requests

### "Add a new client"
1. Create from `templates/client.md`
2. Fill in name, company, contact info
3. Save as `clients/client-name.md`
4. Link to related projects if any

### "Create a project"
1. Use `templates/project.md`
2. Fill metadata (client, dates, priority)
3. Link to client: `[[client-name]]`
4. Save as `projects/project-name.md`
5. Add to relevant tasks

### "What am I working on?"
1. Check `start/dashboard.md` active projects
2. Look at `projects/index.md` for filtered views
3. Show tasks with status `in-progress`

### "Find all notes about X"
1. Search content with grep
2. Check relevant folder
3. Look for tags
4. Check linked notes

### "Archive completed work"
1. Move file to `archive/` folder
2. Update status to `completed` if needed
3. Confirm it disappears from active views

---

## Important Files

### Must-Know Locations
- **Main Entry:** `start/dashboard.md`
- **Quick Capture:** `inbox/quick-capture.md`
- **User Guide:** `start/quick-guide.md`
- **This File:** `start/claude-context.md`

### Index Files (Navigation Hubs)
- `projects/index.md` - All projects views
- `clients/index.md` - CRM overview
- `areas/index.md` - Life areas
- `resources/index.md` - Knowledge base
- `archive/index.md` - Archived items
- `journal/index.md` - Daily notes

---

## Dataview Query Examples

### Active Projects
```dataview
LIST
FROM "projects"
WHERE type = "project" AND status = "in-progress"
```

### Clients by Status
```dataview
TABLE company, status
FROM "clients"
WHERE type = "client"
SORT status
```

### Tasks Due This Week
```dataview
TASK
WHERE due >= date(today) AND due <= date(today) + dur(7 days)
```

---

## Best Practices for AI Assistance

### DO
- ✅ Maintain consistent file naming
- ✅ Use templates for new notes
- ✅ Create proper links between notes
- ✅ Keep frontmatter metadata accurate
- ✅ Respect folder organization
- ✅ Update statuses when changing files
- ✅ Ask for clarification when uncertain

### DON'T
- ❌ Create files without templates
- ❌ Use random naming conventions
- ❌ Skip metadata/frontmatter
- ❌ Break existing links
- ❌ Put files in wrong folders
- ❌ Change system structure without asking
- ❌ Delete files without confirmation

---

## System Philosophy

1. **Capture Fast** - Get it down, organize later
2. **Link Everything** - Build knowledge graph
3. **Review Regularly** - Keep system current
4. **Simple is Better** - Don't over-complicate
5. **Flexible** - Adapt to user's needs
6. **Sustainable** - Easy to maintain long-term

---

## User Preferences

*This section can be updated as you learn user's specific preferences*

- Language: English (file structure), User may speak Spanish
- Naming: lowercase-with-dashes
- No emoji in file names (ok in content)
- Minimal metadata required
- Focus on simplicity

---

## Integration Points

### Potential Tools
- **Git/GitHub** - Version control & backup
- **Google Drive** - Sync across devices
- **Obsidian Mobile** - iOS/Android access
- **Dataview** - Dynamic queries (ESSENTIAL)
- **Templater** - Advanced templating

---

## Troubleshooting

### Links Not Working
- Check file exists in correct folder
- Verify filename matches link exactly
- Case-sensitive on some systems

### Dataview Not Showing Results
- Verify Dataview plugin installed
- Check query syntax
- Ensure metadata fields exist

### Can't Find Note
- Check all index files
- Use global search
- Look in archive folder
- Check inbox for unprocessed items

---

## Version & Updates

**System Version:** 1.0
**Created:** 2026-03-17
**Last Updated:** 2026-03-17
**Maintained by:** TornadoAzul + Claude Code

---

## Quick Reference for Claude

When user says... | Do this...
---|---
"new client" | Create from `templates/client.md` in `clients/`
"new project" | Create from `templates/project.md` in `projects/`
"quick note" | Add to `inbox/quick-capture.md`
"what's active?" | Show `start/dashboard.md` or relevant index
"find X" | Search with grep, check folders
"archive X" | Move to `archive/` folder
"daily note" | Create from `templates/daily-note.md` in `journal/`

---

*This context file helps maintain consistency and quality when working with the VORTEX system.*
