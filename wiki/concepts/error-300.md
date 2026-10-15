---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "300"
  - "grabando incorrectamente (300)"
  - "Error de grabación 300"
generation_complete: true
---

# Error 300

## Definición

El **Error 300** es un código de falla asociado a la Inteligencia Artificial (IA) que indica que un dispositivo monitoreado está **grabando incorrectamente**. Se trata de una alerta operativa dentro del flujo de gestión de incidencias de los dispositivos de IA supervisados por el área CSCG, y no de un error de software en sentido estricto: describe una condición de estado del equipo (su capacidad de captura/registro) detectada por la plataforma de monitoreo.

## Características clave

- **Código numérico de falla (300):** se identifica explícitamente como "300" en los mensajes de alerta y en la descripción del equipo afectado.
- **Diagnóstico específico:** señala un problema de grabación, no de conectividad, temperatura u otro tipo de incidencia.
- **Origen en el monitoreo automatizado:** la detección proviene de la plataforma de monitoreo de infraestructura, que reporta el nombre técnico del equipo afectado.
- **Gestión basada en tareas:** cada ocurrencia genera una tarea asignada a un responsable del área, con un identificador numérico único.
- **Escalamiento a través del canal de AI:** la incidencia se comunica al equipo de AI mediante un mensaje que menciona al equipo afectado, el código de error y a una persona de contacto.
- **Trazabilidad:** el error se vincula simultáneamente al equipo, a la tarea y al responsable, lo que permite seguimiento y cierre.

## Aplicaciones

- **Gestión de incidencias de dispositivos de IA:** identificación y clasificación de alertas de grabación defectuosa dentro del inventario de equipos monitoreados por CSCG.
- **Asignación de responsabilidades:** generación de una tarea (por ejemplo, la tarea 107821158) asignada a [[Marjorie Alexandra Chalen Troya]] para su resolución.
- **Comunicación con el equipo de AI:** envío de un mensaje de solicitud de ayuda referente al equipo `cscgvidanalit-csrcal52a3_5` que graba incorrectamente, mencionando a [[Alvaro Soriano]].
- **Correlación con otras fallas:** el mismo esquema de códigos permite distinguir el Error 300 de otras condiciones del dispositivo, como [[Temperatura elevada]].
- **Auditoría y reporte:** registro histórico de ocurrencias por equipo y por tarea para análisis de recurrencia.

## Conceptos relacionados

- [[concepts/temperatura-elevada|Temperatura elevada]]

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]

## Menciones en la fuente

- "Estimados AI, su gentil ayuda con la tarea 107821158 // cscgvidanalit-csrcal52a3_5 Esta grabando incorrectamente (300) @~Alvaro Soriano" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Inteligencia Artificial (Error 300)" — [[Work/2.1 CSCG|2.1 CSCG]]