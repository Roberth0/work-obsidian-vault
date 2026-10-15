---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "monitoreo proactivo"
  - "monitorización proactiva de red"
  - "proactive monitoring"
generation_complete: true
---

# Monitorización proactiva

## Definición

La monitorización proactiva es el método mediante el cual Telconet detecta la caída de enlaces y de puntos de acceso (AP) antes de que el cliente lo reporte. Consiste en la observación continua del estado de los equipos de red —enlaces y APs— a través de herramientas de monitoreo y de la controladora, de modo que la incidencia se identifique desde el lado del proveedor y no a partir del reclamo del usuario.

## Características clave

- **Detección anticipada**: la caída del enlace se observa antes de que el cliente la reporte.
- **Fuente de verificación técnica**: la comprobación del estado del enlace se realiza sobre la controladora (por ejemplo, estados del tipo `is DOWN` en la controladora HW).
- **Cobertura por identificadores de login**: el método se aplica a distintos logins mediante la verificación de enlace caído.
- **Generación automática de notificaciones**: la detección deriva en correos con el asunto "PERDIDA DE MONITOREO".
- **Apertura de tareas de soporte**: cada evento detectado se registra como tarea con número de tarea asociado.
- **Escalamiento**: los casos sin seguimiento escalan a los niveles N1/L1.

## Aplicaciones

- Vigilancia del estado de enlaces de clientes corporativos y de sus equipos asociados.
- Supervisión de puntos de acceso inalámbricos administrados por controladora, incluidos los APs identificados por nombre (p. ej. `tn_wifi2_parquesanrafael1`).
- Verificación de enlaces caídos para múltiples logins dentro de la operación de red.
- Activación del flujo de notificación por correo al equipo responsable ("PERDIDA DE MONITOREO").
- Registro y trazabilidad de incidentes mediante tareas de soporte numeradas y su posterior escalamiento a N1/L1.

## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[access-point|Access Point]]

## Entidades relacionadas

- [[entities/telconet|Telconet S.A.]]
- [[entities/noc|NOC]]
- [[entities/noc-radio|NOC-RADIO]]
- [[entities/zabbix|zabbix]]
- [[entities/telcograf|Telcograf]]

## Menciones en la fuente

- "Mediante monitoreo proactivo se observa la caida del enlace AP Login: 	tn_wifi2_parquesanrafael1 con MAC 2C AC 5C 9C B0 is DOWN en la controladora HW  https://157.100.14.130/" — [[Work/3. Corporativos|3. Corporativos]]
- "Mediante monitoreo se verifica enlace caído, asociado al login aux: coopjipijapa-tterrestregye_1 con IP: 181.39.39.230 CONTACTO: 052600367. Se envia vía mail la notificación." — [[Work/3. Corporativos|3. Corporativos]]