---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Computer Emergency Response Team"
  - "Equipo de Respuesta ante Emergencias Informáticas"
generation_complete: true
---

# CERT

## Descripción

CERT (Computer Emergency Response Team) es el equipo de respuesta ante incidentes de seguridad al que el [[noc]] debe notificar las alarmas relevantes dentro del flujo de monitoreo descrito en el documento. En la sección dedicada a [[Arbor]], la fuente indica que la notificación a CERT se realiza vía Telegram y que aplica a las [[Alertas DoS]] que cumplan ciertos criterios: estar en ejecución (Ongoing) o ser de severidad HIGH y permanecer sin mitigar. De este modo, CERT funciona como la contraparte de seguridad que recibe los escalamientos generados por el monitoreo de ataques de denegación de servicio. El documento incluye capturas asociadas a CERT que probablemente muestran procedimientos operativos o listas de contacto del equipo. La entidad se enmarca en el entorno de operación de [[Telconet]], donde la coordinación entre monitoreo y respuesta a incidentes es parte del proceso de gestión de alertas.

## Entidades relacionadas

- [[entities/arbor|Arbor]]
- [[entities/telconet|Telconet]]
- [[entities/alertas-dos|Alertas DoS]]

## Conceptos relacionados

## Menciones en la fuente

- "Se debe realizar la notificación via telegram a CERT" — [[Work/1. Backbone|1. Backbone]]
- "### CERT" — [[Work/1. Backbone|1. Backbone]]