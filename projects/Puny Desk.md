---
type: project
name: Puny Desk
client: Puny.bz
status: in-progress
priority: high
start_date: 2026-03-17
due_date:
completion: 0%
tags: [project, puny, desk, communications, leo, ai, interface, mobile-first]
category: UI/UX Development
---

# Puny Desk

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

Desarrollar la interfaz Desk de Puny - un centro de comunicaciones unificado con asistente AI (Leo) para gestionar conversaciones multicanal, llamadas y configuración del asistente virtual. Desk es el modo de recepción que maneja toda la comunicación entrante con clientes.

### Principios de Diseño

1. **Inbox zero mindset** — Limpiar la cola, ver qué está manejado
2. **Conversation-first** — Hilos, no mensajes fragmentados
3. **Leo visibility** — Siempre claro qué manejó Leo vs. necesita humano
4. **Fast response** — Un tap para devolver llamada, texto o tomar acción
5. **Mobile-first** — Funciona completamente desde el teléfono

### Deliverables

#### Core Screens
- [ ] Inbox (vista unificada de conversaciones)
- [ ] Conversation Detail (hilo completo con acciones)
- [ ] Calls Log (registro de todas las llamadas)
- [ ] Call Detail (información completa con transcripción)
- [ ] Leo Settings Hub (configuración del asistente)
- [ ] Business Info (detalles del negocio para Leo)
- [ ] FAQs (preguntas y respuestas)
- [ ] Test Call (probar cómo suena Leo)
- [ ] Playbook (reglas personalizadas avanzadas)
- [ ] Edit Playbook (configurar escenarios)
- [ ] Phone Number (gestión del número de negocio)

#### Component Library
- [ ] Conversation Row
- [ ] Call Row
- [ ] Message Bubble (Incoming/Outgoing)
- [ ] Leo Summary Card
- [ ] FAQ Card
- [ ] Playbook Card
- [ ] Knowledge Gap Card
- [ ] Quick Action Button

#### Onboarding Flow
- [ ] Welcome screen
- [ ] Business Name setup
- [ ] What You Do description
- [ ] Hours configuration
- [ ] Test Call invitation

## Tasks

### To Do
- [ ] Configurar estructura de navegación (Bottom Tab Bar: Inbox | Calls | Leo | Number)
- [ ] Implementar Inbox con secciones (Needs Attention, Handled by Leo)
- [ ] Desarrollar Conversation Detail con Leo Summary
- [ ] Crear sistema multicanal (Call, SMS, WhatsApp, Web)
- [ ] Construir Calls Log con filtros
- [ ] Implementar Call Detail con transcripción y audio playback
- [ ] Desarrollar Leo Settings Hub
- [ ] Crear Business Info form con horarios y servicios
- [ ] Implementar FAQs con templates y suggested questions
- [ ] Construir Test Call flow
- [ ] Desarrollar Playbook system (triggers y behaviors)
- [ ] Crear Phone Number management
- [ ] Implementar Onboarding flow completo

### In Progress
- [ ] Revisar especificaciones de diseño

### Completed
- [x] Documentación de diseño completada

## Navigation Structure

```
Desk (Tab)
├── Inbox (default)
│   └── Conversation Detail
├── Calls
│   └── Call Detail
├── Leo Settings
│   ├── Business Info
│   ├── FAQs
│   ├── Playbook (advanced)
│   └── Test Call
└── Phone Number
```

**Bottom Tab Bar:** Inbox | Calls | Leo | Number

## Screens Breakdown

### 1. Inbox
- **Purpose:** Unified view of all conversations needing attention
- **Sections:** Needs Attention (red), Handled by Leo (collapsible)
- **Channels:** Call, SMS, WhatsApp, Web
- **Interactions:** Swipe to archive/call, Pull to refresh

### 2. Conversation Detail
- **Components:** Leo Summary, Message thread, Quick actions
- **Quick Actions:** Call, Book, Pay, Send Glo, Create Task
- **Multi-channel:** Soporte para diferentes canales de comunicación

### 3. Calls Log
- **Purpose:** All calls with outcomes
- **Call Types:** Inbound (↙), Outbound (↗), Missed (✗)
- **Handler Info:** Leo answered, Transferred, You answered

### 4. Call Detail
- **Components:** Call metadata, Outcome badge, Leo summary, Full transcript
- **Features:** Audio playback, Searchable transcript

### 5. Leo Settings
- **Sections:** Status toggle, Setup (Business/FAQs/Test), Advanced (Playbook/Personality/Notifications)
- **Knowledge Gaps:** Surfaced learning opportunities

### 6. FAQs
- **Features:** Search, Suggested FAQs, Templates, Categories
- **Learning:** Auto-suggestions from unanswered calls

### 7. Playbook
- **Purpose:** Custom rules for specific scenarios
- **Components:** Triggers, Behaviors, Scripts, Info collection
- **Templates:** After Hours, Pricing, Complaints, Appointments

### 8. Phone Number
- **Features:** Call forwarding, Caller ID, Voicemail, Number porting

## Timeline

| Phase | Estimated Date | Status | Notes |
|-------|----------------|--------|-------|
| Design Spec Review | 2026-03-17 | ✓ | Especificaciones completas |
| Component Library | | Pending | Crear biblioteca de componentes |
| Inbox Module | | Pending | Conversaciones y filtros |
| Calls Module | | Pending | Log y detalles con transcripciones |
| Leo Settings | | Pending | Configuración del AI |
| Business Info & FAQs | | Pending | Setup básico |
| Playbook System | | Pending | Reglas avanzadas |
| Onboarding Flow | | Pending | Primera experiencia de usuario |
| Testing & Refinement | | Pending | Pruebas multicanal |
| Launch | | Pending | Despliegue a producción |

## Required Resources

### Team
- UI/UX Designer
- Frontend Developer (React Native / Mobile)
- Backend Developer (API integration)
- AI/ML Engineer (Leo integration)
- QA Tester
- Voice/Audio Engineer (transcripciones)

### Tools
- Figma (diseño)
- React Native / Flutter (desarrollo móvil)
- Twilio / Similar (comunicaciones multicanal)
- Speech-to-Text API (transcripciones)
- Leo AI Engine
- Audio playback libraries

### References
- [[Puny Desk - Design Spec]] (ubicado en Downloads)
- Archivo de especificación original

## Technical Specifications

### Status Indicators

| Status | Visual | Meaning |
|--------|--------|---------|
| Needs attention | 🔴 Red dot | Requires human action |
| Unread | Bold text | New, not viewed |
| Leo handled | ✓ Gray check | Resolved by Leo |
| Leo flagged | ⚠️ Orange | Leo escalated |
| Missed call | 📞✗ | Call not answered |
| Inbound | ↙ | Call/message received |
| Outbound | ↗ | Call/message sent |

### Channel Icons

| Channel | Icon |
|---------|------|
| Phone call | 📞 |
| SMS | 💬 |
| WhatsApp | 📱 |
| Web chat | 💻 |

### Message Bubbles
- **Incoming:** Left-aligned, light background
- **Outgoing/Leo:** Right-aligned, brand color, Leo badge
- **Timestamps:** Below bubbles with channel indicator

### Responsive Considerations

- **Phone (Primary):** Single column, bottom tab, full-screen conversations
- **Tablet:** Split view (Inbox list + Conversation detail)
- **Desktop (Future):** Three-column layout, keyboard shortcuts

## Project Notes

### Important Decisions

- Mobile-first con soporte multicanal completo
- Leo AI es el centro de la experiencia (visibility de qué manejó)
- Inbox zero como objetivo (clear queue mentality)
- Transcripciones de llamadas con audio playback
- Knowledge gaps para mejorar Leo continuamente

### Risks

- Complejidad de integración multicanal (SMS, WhatsApp, Web, Calls)
- Latencia en transcripciones de llamadas en tiempo real
- Calidad y precisión del AI Leo
- Privacidad de datos de conversaciones y transcripciones
- Sincronización en tiempo real entre dispositivos

### Learnings

-

## Integration Points

### Leo AI
- Inbox management (needs attention vs handled)
- Call answering and screening
- Message responses
- Summary generation
- Knowledge gap detection
- Playbook execution

### Ops Integration
- Quick actions (View in Ops)
- Contact creation from conversations
- Deal creation from leads
- Task creation

### Communication Channels
- Phone calls (Twilio/similar)
- SMS
- WhatsApp Business API
- Web chat widget

### Pay Integration
- Quick payment requests
- Payment links in conversations

## Onboarding Flow

### Steps
1. Welcome (Meet Leo intro)
2. Business Name (how Leo answers)
3. What You Do (one sentence description)
4. Hours (optional schedule)
5. Test Call (try Leo immediately)

**Goal:** Get Leo ready in under 5 minutes

## Knowledge Management

### FAQ System
- User-created FAQs
- Templates by industry
- Suggested questions from unanswered calls
- Categories and search

### Playbooks
- Trigger-based rules
- Custom scripts (Opening/Closing)
- Behavior checkboxes
- Information collection

## Related Meetings

```dataview
LIST
FROM "inbox" OR "resources"
WHERE contains(project, this.file.name) AND type = "meeting"
```

## Files

- Design Spec: `/Users/tornadoazul/Downloads/Desk - Design Spec.md`

---
**Created:** 2026-03-17
**Last updated:** 2026-03-17
