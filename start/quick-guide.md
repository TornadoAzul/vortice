---
type: guide
tags: [start, guide, help]
---

# Quick Guide - VORTEX System

[[start/dashboard|← Back to Dashboard]]

---

## Welcome to VORTEX

This is your personal command center for managing projects, clients, notes, and your life.

---

## System Structure

### Core Folders

| Folder | Purpose | When to Use |
|--------|---------|-------------|
| **start** | Home base & system files | First place to go |
| **inbox** | Quick capture & processing | Jot things down fast |
| **projects** | Active & completed projects | Manage project work |
| **clients** | CRM & client management | Track all client info |
| **areas** | Life areas (ongoing) | Health, Career, etc. |
| **resources** | Knowledge base | Save useful info |
| **archive** | Completed/inactive items | Old projects/clients |
| **journal** | Daily notes & reflections | Personal journaling |
| **templates** | Note templates | Create new notes |
| **media** | Files & attachments | Auto-created |

---

## Quick Start Workflow

### 1. Start Your Day
1. Open [[start/dashboard|Dashboard]]
2. Check **Today's Priorities**
3. Review **Active Projects**
4. Check **Urgent Tasks**

### 2. Capture Something Fast
- Use [[inbox/quick-capture|Quick Capture]] for anything
- Process inbox regularly (move to proper folders)

### 3. Create Structured Notes
Use templates for:
- New client → [[templates/client|Client Template]]
- New project → [[templates/project|Project Template]]
- New task → [[templates/task|Task Template]]
- Meeting notes → [[templates/meeting|Meeting Template]]
- Quick idea → [[templates/idea|Idea Template]]
- Daily journal → [[templates/daily-note|Daily Note Template]]
- Save resource → [[templates/resource|Resource Template]]

### 4. Link Everything
- Link clients to projects: `[[client-name]]`
- Link projects to tasks
- Link meetings to clients/projects
- This creates your personal knowledge graph

### 5. Review & Archive
- **Weekly**: Process inbox, update project statuses
- **Monthly**: Review areas, archive completed items
- **Quarterly**: Big picture review

---

## Key Features

### Dataview Queries
The dashboard uses Dataview plugin to show:
- Active projects dynamically
- Client lists
- Pending tasks
- Statistics

**Note:** Install Dataview plugin for full functionality.

### Frontmatter (Metadata)
Each note has metadata at the top:
```yaml
---
type: project
status: in-progress
priority: high
---
```
This powers searches and views.

### Statuses & States

**Projects:**
- `todo` - Not started
- `in-progress` - Working on it
- `blocked` - Waiting on something
- `completed` - Done
- `paused` - On hold

**Clients:**
- `active` - Current client
- `potential` - Lead/prospect
- `inactive` - Not working together

**Tasks:**
- `todo` - To do
- `in-progress` - Doing now
- `blocked` - Can't proceed
- `completed` - Done
- `paused` - On hold

**Ideas:**
- `new` - Just captured
- `researching` - Investigating
- `validated` - Worth doing
- `developing` - Building it
- `implemented` - Done
- `discarded` - Not doing

---

## Best Practices

### 1. Capture Fast, Organize Later
- Dump everything in inbox first
- Process regularly
- Don't let inbox grow too large

### 2. Use Consistent Naming
- `lowercase-with-dashes` for files
- Descriptive names (e.g., `acme-corp-website-redesign`)

### 3. Link Liberally
- Connect related notes
- Build your knowledge graph
- Use `[[double-brackets]]`

### 4. Update Regularly
- Keep project statuses current
- Update completion percentages
- Mark tasks as done

### 5. Review System
- **Daily**: Priorities & tasks
- **Weekly**: Projects & inbox
- **Monthly**: Areas & goals
- **Quarterly**: Big picture

---

## Common Tasks

### Create a New Client
1. Go to [[templates/client|Client Template]]
2. Fill in details (name, company, contact)
3. Save in `clients/` folder as `client-name.md`

### Create a New Project
1. Go to [[templates/project|Project Template]]
2. Fill in info
3. Link to client: `[[client-name]]`
4. Save in `projects/` folder

### Archive Completed Work
1. Move file from original folder to `archive/`
2. File automatically disappears from active views

### Find Something
- Use Obsidian search (Cmd/Ctrl + O)
- Check relevant index file
- Search by tag

---

## Recommended Plugins

Install these Obsidian community plugins for best experience:

1. **Dataview** - Powers dynamic lists & stats (ESSENTIAL)
2. **Templater** - Advanced templates with dates
3. **Calendar** - Visual calendar for daily notes
4. **Tasks** - Advanced task management
5. **Periodic Notes** - Auto-create daily/weekly notes
6. **Kanban** - Visual project boards
7. **Obsidian Git** - Sync with GitHub (for backup)

---

## Tips & Tricks

### Quick Navigation
- Use `Cmd/Ctrl + O` to quick-open files
- Star important files for quick access
- Pin dashboard in sidebar

### Keyboard Shortcuts
- `Cmd/Ctrl + N` - New note
- `Cmd/Ctrl + O` - Quick open
- `Cmd/Ctrl + P` - Command palette
- `Cmd/Ctrl + E` - Toggle edit/preview

### Mobile Usage
- Install Obsidian on iOS/Android
- Sync via iCloud, Google Drive, or Obsidian Sync
- Use quick capture for on-the-go notes

---

## Need Help?

- Read: [[start/claude-context|Claude Context]] (for AI assistance)
- Check: [Obsidian Documentation](https://help.obsidian.md)
- Visit: [Obsidian Forum](https://forum.obsidian.md)

---

## Customize This System

This is YOUR system. Feel free to:
- Add/remove folders
- Modify templates
- Change statuses
- Create your own workflow

Make it work for YOU!

---

*Last updated: `=date(today)`*
