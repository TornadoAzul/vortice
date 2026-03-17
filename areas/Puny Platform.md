---
type: area
name: Puny Platform
tags: [area, puny, platform, development]
focus: UI/UX Development
---

# Puny Platform

**Client:** [[Puny.bz]]
**Focus:** UI/UX Development para nuevas interfaces

---

## Overview

Área dedicada al desarrollo de la nueva interfaz de Puny, enfocada en crear experiencias móviles excepcionales con integración de AI.

## Active Projects

### 🎯 Current Development

#### [[Puny Ops]]
**CRM Móvil para Operaciones**

- Dashboard con métricas clave
- Gestión de Contacts con búsqueda avanzada
- Pipeline visual (Kanban) para deals
- Sistema de Tasks con prioridades
- Integración con Leo AI para insights

**Status:** In Progress | **Priority:** High

#### [[Puny Desk]]
**Centro de Comunicaciones con AI**

- Inbox unificado multicanal
- Leo AI assistant para atención al cliente
- Call management con transcripciones
- FAQs y Playbooks personalizables
- Onboarding en <5 minutos

**Status:** In Progress | **Priority:** High

---

## Puny Ecosystem

### Productos Existentes (Punies)

#### 📅 Booking
Sistema de reservaciones para clases, servicios y eventos
- **Clientes:** Fuzzforo LLC (Yoga)

#### 🛍️ Shop
E-commerce para venta de productos
- **Clientes:** Fuzzforo LLC (merch)

#### 🎫 Passes
Programas de fidelidad y membresías
- **Clientes:** Fuzzforo LLC

### Nuevas Interfaces (En Desarrollo)

#### 📊 Ops
CRM móvil con AI integration

#### 💬 Desk
Centro de comunicaciones con Leo AI

---

## Design Philosophy

### Core Principles

**Mobile-First**
- Teléfono como dispositivo principal
- Tablet y Desktop como secundarios
- Optimización para uso con un pulgar

**AI-Powered**
- Leo como asistente central
- Aprendizaje continuo (knowledge gaps)
- Automatización inteligente

**Speed & Efficiency**
- Carga <1 segundo en vistas principales
- Skeleton screens (no spinners)
- Datos fluyen automáticamente

**User-Centric**
- Glanceable interfaces (respuestas en 2s)
- Inbox zero mindset
- Minimal data entry

---

## Technology Stack

### Frontend
- React Native / Flutter (mobile)
- Responsive design
- Component libraries

### AI/ML
- Leo AI Engine
- Natural Language Processing
- Speech-to-Text (transcripciones)

### Communications
- Twilio / Similar provider
- Multi-channel: Calls, SMS, WhatsApp, Web
- Real-time synchronization

### Backend
- RESTful APIs
- Real-time data sync
- Cloud infrastructure

---

## Resources & Documentation

### Design Specs
- [[Ops - Design Spec]] - Especificaciones completas de UI/UX para Ops
- [[Desk - Design Spec]] - Especificaciones completas de UI/UX para Desk

### File Locations
- `/Users/tornadoazul/Downloads/Ops - Design Spec.md`
- `/Users/tornadoazul/Downloads/Desk - Design Spec.md`

---

## Client Ecosystem

### Businesses Using Puny

```dataview
TABLE company as "Company", location as "Location", services as "Punies Used"
FROM "clients"
WHERE contains(tags, "punybz") OR partner = "Puny.bz"
SORT company ASC
```

#### Featured: Fuzzforo LLC
- **Location:** Módulo de Mejoramiento Comunitario
- **Services:** Booking (Yoga), Shop (merch), Passes (fidelidad)
- **Status:** Active

---

## Development Roadmap

### Phase 1: Foundation (Current)
- [x] Design specifications completed
- [ ] Component libraries built
- [ ] Core screens developed

### Phase 2: Integration
- [ ] Leo AI integration
- [ ] Multi-channel communications
- [ ] Cross-product integrations

### Phase 3: Testing & Refinement
- [ ] Mobile device testing
- [ ] User feedback loops
- [ ] Performance optimization

### Phase 4: Launch
- [ ] Beta release
- [ ] Client onboarding
- [ ] Production deployment

---

## Key Features to Highlight

### Ops Highlights
✓ Dashboard en 2 segundos
✓ Drag & drop pipeline
✓ Leo alerts inteligentes
✓ Quick actions (Call, Text, Pay)
✓ Contact history completo

### Desk Highlights
✓ Inbox zero workflow
✓ Multi-channel unified inbox
✓ Leo AI answering calls
✓ Call transcriptions con audio
✓ Knowledge gap learning
✓ Playbooks personalizables

---

## Related Meetings

```dataview
LIST
FROM "inbox" OR "resources"
WHERE contains(tags, "puny") AND type = "meeting"
SORT date DESC
```

---

## Quick Links

- [[clients/Puny.bz|Puny.bz Client Profile]]
- [[projects/Puny Ops|Puny Ops Project]]
- [[projects/Puny Desk|Puny Desk Project]]
- [[clients/Fuzzforo LLC|Fuzzforo LLC - First Puny Client]]

---

**Created:** 2026-03-17
**Last updated:** 2026-03-17
