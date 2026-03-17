---
type: client
name: Puny.bz
company: Puny.bz
status: active
contact:
  email:
  phone:
  linkedin:
start_date: 2026-03-17
tags: [client, platform, saas, ai]
role: Platform Provider
---

# Puny.bz

## General Information

**Company:** Puny.bz
**Status:** active
**Start Date:** 2026-03-17
**Role:** Platform Provider - Proveedor de servicios para negocios

### Contact Details
- Email:
- Phone:
- LinkedIn:
- Other:

## About Puny.bz

Puny.bz es una plataforma integral de servicios para negocios que ofrece diferentes "Punies" (módulos/productos) que las compañías pueden utilizar para mejorar sus operaciones.

### Productos/Servicios (Punies)

#### Booking
- **Descripción:** Sistema de reservaciones y citas
- **Uso:** Clases, servicios, eventos
- **Clientes usando:** Fuzzforo LLC (Yoga)

#### Shop
- **Descripción:** Tienda en línea / E-commerce
- **Uso:** Venta de productos y mercancía
- **Clientes usando:** Fuzzforo LLC (merch)

#### Passes
- **Descripción:** Sistema de pases y programas de fidelidad
- **Uso:** Membresías, loyalty programs
- **Clientes usando:** Fuzzforo LLC

#### Ops (En Desarrollo)
- **Descripción:** CRM móvil para gestión de operaciones
- **Features:** Contacts, Pipeline, Tasks, Leo AI integration
- **Status:** In development - Design spec completed

#### Desk (En Desarrollo)
- **Descripción:** Centro de comunicaciones con asistente AI
- **Features:** Inbox multicanal, Leo AI, Call management, FAQs
- **Status:** In development - Design spec completed

## Proyectos Activos

### UI/UX Development

```dataview
TABLE status as "Status", priority as "Priority", completion as "Progress"
FROM "projects"
WHERE contains(client, "Puny.bz")
SORT priority DESC
```

#### Puny Ops
- **Status:** In Progress
- **Purpose:** CRM móvil para gestión de contactos, deals y tareas
- **Design Principles:** Mobile-first, Glanceable, Fast
- **Link:** [[Puny Ops]]

#### Puny Desk
- **Status:** In Progress
- **Purpose:** Centro de comunicaciones con Leo AI
- **Design Principles:** Inbox zero, Conversation-first, Leo visibility
- **Link:** [[Puny Desk]]

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
- [ ] Completar desarrollo de Puny Ops UI
- [ ] Completar desarrollo de Puny Desk UI
- [ ] Integración de Leo AI en ambas interfaces
- [ ] Testing móvil en dispositivos reales
- [ ] Definir roadmap de siguientes Punies

## Notes & Observations

### Preferences
- Enfoque mobile-first para todas las interfaces
- AI integration (Leo) como diferenciador clave
- UX optimizada para velocidad y eficiencia
- Design systems consistentes entre productos

### Important Information
- Platform provider para múltiples negocios
- Modelo modular (Punies separados que se pueden combinar)
- Leo AI es el asistente virtual que cruza productos
- Fuzzforo LLC es primer cliente registrado usando múltiples Punies

## Technology Stack

### Interfaces
- Mobile-first design
- React Native / Flutter (probable)
- Responsive (Phone, Tablet, Desktop)

### AI
- Leo - Asistente virtual
- Capacidades: Call handling, Message management, Summaries, Learning from gaps

### Integrations
- Multicanal: Calls, SMS, WhatsApp, Web
- Payment processing
- Calendar/Booking systems
- CRM functionality

## Billing

| Project | Amount | Status | Date |
|---------|--------|--------|------|
| Puny Ops Development | | In Progress | 2026-03-17 |
| Puny Desk Development | | In Progress | 2026-03-17 |

## Files & Resources

- Ops Design Spec: `/Users/tornadoazul/Downloads/Ops - Design Spec.md`
- Desk Design Spec: `/Users/tornadoazul/Downloads/Desk - Design Spec.md`

---
**Created:** 2026-03-17
**Last updated:** 2026-03-17
