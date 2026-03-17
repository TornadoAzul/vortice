---
type: project
name: Puny Ops
client: Puny.bz
status: in-progress
priority: high
start_date: 2026-03-17
due_date:
completion: 0%
tags: [project, puny, ops, crm, interface, mobile-first]
category: UI/UX Development
---

# Puny Ops

## Project Information

**Client:** [[Puny.bz]]
**Status:** in-progress
**Priority:** high
**Start:** 2026-03-17
**Due:**
**Progress:** 0%
**Category:** UI/UX Development

## Objective

### Description

Desarrollar la interfaz Ops de Puny - un CRM móvil optimizado para gestión de contactos, pipeline de ventas y tareas. Ops es el modo de operaciones que permite a los usuarios gestionar clientes, leads y deals desde dispositivos móviles.

### Principios de Diseño

1. **Glanceable** — Dashboard responde "¿qué ahora?" en 2 segundos
2. **Thumb-friendly** — Todas las acciones primarias alcanzables con un pulgar
3. **Zero data entry** — Los datos fluyen automáticamente; interacción mínima del usuario
4. **Mobile-first** — El teléfono es el dispositivo principal; tablet/desktop son secundarios
5. **Fast** — Dashboard carga en <1 segundo; sin spinners en vistas primarias

### Deliverables

#### Core Screens
- [ ] Dashboard (comando central diario)
- [ ] Contacts List (búsqueda y gestión de clientes)
- [ ] Contact Detail (perfil completo con historial)
- [ ] Pipeline Kanban (seguimiento visual de deals)
- [ ] Pipeline List View (vista rápida de todos los deals)
- [ ] Deal Detail (información completa del deal)
- [ ] Tasks (gestión de to-dos)
- [ ] New/Edit Task
- [ ] New/Edit Contact
- [ ] New/Edit Deal

#### Component Library
- [ ] Metric Card
- [ ] Leo Alert Card
- [ ] Contact Row
- [ ] Deal Card (Kanban)
- [ ] Task Row
- [ ] Activity Feed Item
- [ ] Tag Chip
- [ ] Stage Badge
- [ ] Empty States

## Tasks

### To Do
- [ ] Configurar estructura de navegación (Bottom Tab Bar)
- [ ] Implementar Dashboard con secciones (Key Numbers, Leo Alerts, Tasks, Activity Feed)
- [ ] Desarrollar sistema de búsqueda y filtros para Contacts
- [ ] Crear Contact Detail con tabs (Timeline, Details, Deals, Tasks)
- [ ] Construir Pipeline Kanban con drag & drop
- [ ] Implementar Pipeline List View con filtros
- [ ] Desarrollar sistema de Tasks con estados (Overdue, Today, Upcoming, Completed)
- [ ] Crear formularios para New/Edit Contact/Deal/Task
- [ ] Implementar Leo Summary en Contact Detail
- [ ] Configurar Quick Actions (Call, Text, Pay, Task)

### In Progress
- [ ] Revisar especificaciones de diseño

### Completed
- [x] Documentación de diseño completada

## Navigation Structure

```
Ops (Tab)
├── Dashboard (default)
├── Contacts
│   └── Contact Detail
├── Pipeline
│   └── Deal Detail
├── Tasks
└── Settings (gear icon)
```

**Bottom Tab Bar:** Dashboard | Contacts | Pipeline | Tasks

## Screens Breakdown

### 1. Dashboard
- **Purpose:** Daily command center — what needs attention now
- **Components:** Greeting, Metric cards, Leo alerts, Task list, Activity feed
- **Interactions:** Pull to refresh, Swipe task, Tap metrics

### 2. Contacts
- **Purpose:** Find and manage clients
- **Components:** Search bar, Filter chips, Contact rows, FAB
- **Sort:** By last interaction (most recent first)

### 3. Contact Detail
- **Purpose:** Full client profile with all history
- **Tabs:** Timeline, Details, Deals, Tasks
- **Quick Actions:** Call, Text, Pay, Task

### 4. Pipeline (Kanban)
- **Purpose:** Visual deal tracking
- **Interactions:** Drag cards between columns

### 5. Tasks
- **Purpose:** To-do management
- **Sections:** Overdue | Today | Upcoming | Completed

## Timeline

| Phase | Estimated Date | Status | Notes |
|-------|----------------|--------|-------|
| Design Spec Review | 2026-03-17 | ✓ | Especificaciones completas |
| Component Library | | Pending | Crear biblioteca de componentes reutilizables |
| Dashboard Development | | Pending | Pantalla principal |
| Contacts Module | | Pending | Lista y detalle de contactos |
| Pipeline Module | | Pending | Kanban y lista de deals |
| Tasks Module | | Pending | Sistema de tareas |
| Testing & Refinement | | Pending | Pruebas en dispositivos móviles |
| Launch | | Pending | Despliegue a producción |

## Required Resources

### Team
- UI/UX Designer
- Frontend Developer (React Native / Mobile)
- Backend Developer (API integration)
- QA Tester

### Tools
- Figma (diseño)
- React Native / Flutter (desarrollo móvil)
- API de Puny.bz
- Dataview integration para Leo

### References
- [[Puny Ops - Design Spec]] (ubicado en Downloads)
- Archivo de especificación original

## Technical Specifications

### Colors & Status

| Status | Color | Usage |
|--------|-------|-------|
| Overdue | Red | Tasks, stale deals |
| Today/Active | Blue | Current tasks, active items |
| Success | Green | Completed, won deals |
| Warning | Orange | Leo alerts, needs attention |
| Inactive | Gray | Archived, muted items |

### Typography Hierarchy

1. **Screen Title:** Large, bold (Dashboard, Contacts)
2. **Section Header:** Medium, semibold (TODAY'S TASKS)
3. **Card Title:** Regular, semibold (Contact name, Deal name)
4. **Body Text:** Regular (Descriptions, notes)
5. **Caption:** Small, muted (Timestamps, secondary info)
6. **Metric Number:** Extra large, bold (Key numbers)

### Responsive Considerations

- **Phone (Primary):** Single column, bottom tab navigation, full-width cards
- **Tablet:** Two-column layout, pipeline shows more stages
- **Desktop (Future):** Three-column layout, sidebar navigation, keyboard shortcuts

## Project Notes

### Important Decisions

- Mobile-first approach prioritiza teléfonos sobre desktop
- Leo AI integration es central para la experiencia (alerts, summaries)
- Skeleton screens preferidos sobre spinners para mejor UX
- Swipe actions para agilizar flujos de trabajo

### Risks

- Complejidad del drag & drop en Pipeline Kanban móvil
- Rendimiento con grandes volúmenes de datos (contacts, deals)
- Integración con Leo AI debe ser fluida y rápida
- Sincronización entre diferentes dispositivos

### Learnings

-

## Integration Points

### Leo AI
- Dashboard alerts
- Contact summaries
- Deal insights
- Activity feed generation

### Desk Integration
- Quick actions (Call, Text)
- Conversation links
- Call forwarding

### Pay Integration
- Quick payment actions
- Payment history in deals

## Related Meetings

```dataview
LIST
FROM "inbox" OR "resources"
WHERE contains(project, this.file.name) AND type = "meeting"
```

## Files

- Design Spec: `/Users/tornadoazul/Downloads/Ops - Design Spec.md`

---
**Created:** 2026-03-17
**Last updated:** 2026-03-17
