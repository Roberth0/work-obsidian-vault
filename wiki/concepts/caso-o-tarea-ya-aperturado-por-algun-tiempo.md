---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-vips_147ea4]]"
tags:
aliases:
  - "Caso antiguo"
  - "Tarea sin avances"
  - "Caso estancado"
generation_complete: true
---

# Caso o tarea ya aperturado por algun tiempo

## Definición

**Caso o tarea ya aperturado por algun tiempo** es la situación operativa en la que una tarea o caso permanece abierto durante varios días sin registrar avances en su seguimiento. La regla asociada establece que, si el caso tiene más de dos días de creación y no presenta progreso, se debe notificar en el chat de Telegram del [[NOC IPCCL1 PROACTIVOS]] mediante un mensaje con formato específico que incluye el número de tarea, el identificador del punto y el último seguimiento registrado.

## Características clave

- **Criterio temporal**: el detonante es la antigüedad del caso — más de dos días desde su creación.
- **Criterio de inactividad**: debe combinarse con la ausencia de avances en el seguimiento; no basta con que el caso sea antiguo.
- **Canal de notificación definido**: la alerta se publica en el chat de Telegram del [[NOC IPCCL1 PROACTIVOS]].
- **Formato obligatorio del mensaje**: número de tarea, identificador del punto (por ejemplo, `ijsud-carapungo1`) y último seguimiento con fecha y hora.
- **Propósito preventivo**: evitar que los casos queden estancados y garantizar la visibilidad del estancamiento ante el equipo de L1.
- **Carácter proactivo**: traslada la iniciativa al equipo de monitoreo en lugar de esperar a que el usuario o el cliente reclame.

## Aplicaciones

- **Monitoreo proactivo de tickets en L1**: revisión periódica del inventario de casos abiertos para detectar aquellos sin movimiento.
- **Recordatorios y escalamiento interno**: uso del mensaje estandarizado para reactivar la gestión de una tarea olvidada, tanto en [[VIPS]] como en otros sistemas monitoreados.
- **Trazabilidad del seguimiento**: el último seguimiento registrado en la notificación deja constancia de la fecha y hora exactas en que se abandonó el avance, lo que facilita auditorías posteriores.
- **Prevención de incidentes prolongados**: se aplica de forma complementaria a otros eventos operativos como el [[Corte de Ruta]], donde la falta de seguimiento puede agravar el impacto.
- **Control de gestión de accesos**: sirve para vigilar [[Logins que no se gestionan]], que tienden a quedar abiertos sin resolución.

## Conceptos relacionados

- [[concepts/vips|VIPS]]
- [[concepts/corte-de-ruta|Corte de Ruta]]
- [[concepts/logins-que-no-se-gestionan|Logins que no se gestionan]]

## Entidades relacionadas

- [[entities/telegram|Telegram]]
- [[entities/noc-ipccl1-proactivos|NOC IPCCL1 PROACTIVOS]]

## Menciones en la fuente

- ">[!info]- Caso o tarea ya aperturado por algun tiempo" — [[Work/2. VIPS|2. VIPS]]
- "Si la tarea/caso en cuestion ya tiene mas de dos dias de creacion y no se tiene avances en el seguimiento se debe notificar en el chat de ***Telegram*** de NOC IPCCL1 PROACTIVOS con el siguiente texto:" — [[Work/2. VIPS|2. VIPS]]