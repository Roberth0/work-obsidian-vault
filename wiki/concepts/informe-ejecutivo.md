---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "Informe Ejecutivo de Caída de Equipo"
  - "Informe de Caída de Equipo"
  - "Executive Report"
generation_complete: true
---

# Informe Ejecutivo

## Definición

El **Informe Ejecutivo** es el documento formal que se elabora cuando ocurre una caída de equipo y que debe estar correctamente redactado y validado antes de poder cerrar el caso. Constituye el registro oficial del incidente: consolida los datos del servicio afectado, el análisis técnico del problema, las acciones correctivas aplicadas y el plan de mejoramiento comprometido, y su validación es requisito previo a la finalización de la tarea asociada.

## Características clave

- **Obligatoriedad de cierre**: no se puede finalizar el caso hasta que el informe esté redactado y validado.
- **Campos obligatorios verificables**:
  - Cliente Afectado
  - Servicios Afectados
  - Fecha y hora de inicio (**no modificar**)
  - Fecha y hora de finalización (verificar la subida del equipo mediante la alarma en [[Zabbix]])
  - No. de Casos/Tareas (**no modificar**)
  - Departamento Asignado
  - Análisis del problema
  - Acciones correctivas
  - Plan de mejoramiento
  - Status Actual
- **Trazabilidad temporal**: la hora de finalización se confirma con evidencia de monitoreo (subida del equipo reflejada en la alarma de [[Zabbix]]).
- **Criterio especial para enlaces interurbanos**: en estos casos, la hora de finalización es la hora en que los clientes afectados —por ejemplo [[Telcos|Nedetel]], [[Telcos|Xtrim]] o [[Telcos|Claro]]— validan la operatividad del servicio.
- **Ciclo de cierre documentado**: una vez validado, se descarga el PDF generado y se finaliza la tarea adjuntando el informe corregido.
- **Calidad de redacción**: exige revisión y corrección previa, de modo que el documento final refleje fielmente lo ocurrido.

## Aplicaciones

- **Gestión de incidentes por caída de equipo**: registro formal y estandarizado de cada evento, tanto en la red de [[CEDIA]] como en servicios provistos a terceros.
- **Cierre de casos y tareas**: actúa como entregable final y condición de cierre en la herramienta de tickets.
- **Coordinación con clientes y operadores**: en escenarios interurbanos, articula la validación de operatividad con los clientes afectados antes de fijar la hora de finalización.
- **Auditoría y seguimiento**: permite reconstruir la cronología del incidente, verificar el cumplimiento de los acuerdos de nivel de servicio y dar seguimiento a los planes de mejoramiento.
- **Mejora continua**: el análisis del problema y las acciones correctivas documentadas alimentan la prevención de fallas recurrentes.

## Conceptos relacionados

- [[concepts/vpn|VPN]]
- [[concepts/link-loss|link loss]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/zabbix|Zabbix]]
- [[entities/cedia|CEDIA]]

## Menciones en la fuente

- "Se debe verificar que el informe este bien redactado, se realiza informe ejecutivo cuando ahi una caida de equipo." — [[Work/4 Cedia|4 Cedia]]
- "Si el informe es por caso interurbano la hora de finalizacion es la hora en la cual los clientes (nedetel, xtrim, claro, etc) afectados validan operatividad" — [[Work/4 Cedia|4 Cedia]]
- "**Cliente Afectado:** Clientes que dependen del equipo sw1zapallochone 
	**Servicios Afectados:** Internet y Datos" — [[Work/4 Cedia|4 Cedia]]