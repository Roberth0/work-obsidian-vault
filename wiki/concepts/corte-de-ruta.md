---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-vips_147ea4]]"
tags:
aliases:
  - "Corte de ruta"
  - "Bloqueo de ruta"
  - "Ruta caída"
generation_complete: true
---

# Corte de Ruta

## Definición

El **corte de ruta** es un procedimiento operativo que se activa cuando una ruta determinada cae, es decir, cuando deja de estar disponible o deja de operar con normalidad. El objetivo del procedimiento es asegurar que toda ruta caída cuente con el seguimiento adecuado dentro del sistema de casos, evitando que una interrupción quede sin registro ni responsable asignado.

## Características clave

- Se activa ante la caída de una ruta determinada, no ante cualquier incidencia genérica.
- El primer paso consiste en preguntar en el chat de L1 ([[Telegram]] o WhatsApp) si ya existe un caso asignado a dicha ruta.
- Si no existe un caso asociado a la ruta caída, el operador debe crearlo.
- Cada caso se identifica mediante un código único con formato de fecha y secuencia; el documento cita como ejemplo el identificador `20240831-0153B`.
- El flujo garantiza trazabilidad: toda ruta caída queda vinculada a un caso con seguimiento.
- Es un procedimiento de coordinación entre canales de comunicación operativos y el sistema de gestión de casos.

## Aplicaciones

- **Monitoreo operativo de rutas**: cuando el monitoreo detecta que una ruta dejó de responder, se dispara el procedimiento de corte de ruta.
- **Mesas de ayuda de nivel 1 (L1)**: los operadores verifican en el chat el estado del caso antes de crear uno nuevo, evitando duplicados.
- **Gestión de incidentes**: el identificador de caso permite rastrear el ciclo de vida del incidente desde su detección hasta su resolución.
- **Auditoría y reportes**: los casos creados por corte de ruta sirven como registro histórico de las interrupciones y de su atención.
- **Coordinación entre equipos y turnos**: el registro en el chat evita que dos turnos abran casos distintos para la misma ruta caída.

## Conceptos relacionados

- [[concepts/proactivo|Proactivo]]
- [[concepts/vips|Monitoreo VIPS]]

## Entidades relacionadas

- [[entities/telegram|Telegram]]

## Menciones en la fuente

- "Preguntar en el chat de L1, Telegram/WhatsApp si se dispone de un caso asignado por dicha ruta." — [[Work/2. VIPS|2. VIPS]]
- "Si no se tiene caso se lo debe crear" — [[Work/2. VIPS|2. VIPS]]
- "Ejemplo de caso **20240831-0153B**" — [[Work/2. VIPS|2. VIPS]]