---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "Unión de Razones Sociales"
  - "Unificación de Razones Sociales"
  - "Merger of Legal Entity Names"
generation_complete: true
---

# Union de Razones Sociales

## Definición

La **Union de Razones Sociales** es un procedimiento operativo consistente en fusionar o migrar la configuración de razones sociales de un cliente dentro de los sistemas internos. El proceso implica dar de baja la configuración asociada a la razón social antigua y registrar la nueva, de modo que los datos del cliente permanezcan coherentes una vez completada la unificación.

## Características clave

- Es un procedimiento de tipo **migración/unificación**, no una operación de configuración desde cero: parte de una razón social existente que debe ser sustituida.
- Vincula al menos dos sistemas internos: **"Razones sociales"** (donde residen los datos identificativos y de infraestructura) e **"Informacion recibida de sistemas"** (donde se registran los puntos consumidos por las herramientas de monitorización).
- Tiene una secuencia definida en dos fases: primero la **cancelación** de los puntos de la razón social antigua, después la **creación** de los puntos con los nuevos cambios.
- Requiere actualizar campos técnicos concretos en la ficha de la razón social: **SERVER IP**, **Name ZG ORG** e **ID Grafana**.
- Se dispara ante **cambios estructurales del cliente**, como superar el umbral de las 500M.
- Su objetivo final es preservar la **coherencia de datos** y evitar puntos huérfanos o duplicados tras la unificación.

## Aplicaciones

- **Alta de una nueva razón social tras un cambio estructural**: cuando el cliente supera las 500M y necesita operar bajo una razón social distinta, este procedimiento traslada la configuración completa.
- **Mantenimiento de la monitorización**: al actualizar SERVER IP, Name ZG ORG e ID Grafana se garantiza que las herramientas de observabilidad sigan recibiendo datos de la entidad correcta.
- **Saneamiento del inventario de puntos**: la cancelación de los puntos de la razón social antigua en "Informacion recibida de sistemas" elimina registros obsoletos.
- **Trazabilidad operativa**: el procedimiento deja documentadas las tareas completadas, lo que permite auditar qué se migró y en qué orden.

## Conceptos relacionados

- [[concepts/ingresos-de-aps|Ingresos de APs]]
- [[concepts/macros|MACROS]]

## Entidades relacionadas

- [[entities/telcograph|Telcograph]]
- [[entities/4-cedia|cedia]]

## Menciones en la fuente

- "### Union de Razones Sociales" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [x] Cancelar puntos de la razon social antigua en *Informacion recibida de sistemas*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [x] Cambiar datos de SERVER IP, Name ZG ORG e ID Grafana en *Razones sociales*" — [[Work/4.1 Telcograph|4.1 Telcograph]]