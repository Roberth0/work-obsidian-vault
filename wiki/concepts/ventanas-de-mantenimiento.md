---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "VMs"
  - "Ventanas Programadas"
  - "Ventanas Programadas de OTN"
generation_complete: true
---

# Ventanas de Mantenimiento

## Definición

Las Ventanas de Mantenimiento (VMs) son los periodos planificados durante los cuales se ejecutan cambios o intervenciones sobre la red, bajo la coordinación de [[OTN]]. Constituyen un proceso operativo formal mediante el cual las modificaciones de red se agendan, se comunican y se documentan, en lugar de realizarse de manera improvisada.

En la documentación de origen, este concepto aparece vinculado al rol o etiqueta «Tareas sisrred // Ventanas de Mantenimiento», lo que lo sitúa como una actividad operativa recurrente y con responsables definidos dentro de la organización.

## Características clave

- **Planificadas y coordinadas:** las intervenciones no son reactivas, sino que se agendan previamente y se coordinan con [[OTN]].
- **Vinculadas a un rol operativo:** el documento las asocia a la etiqueta «Tareas sisrred // Ventanas de Mantenimiento», dotándolas de un responsable claro.
- **Seguimiento activo durante la ventana:** durante las ventanas programadas de OTN se debe llamar para preguntar por novedades sobre las VMs planificadas.
- **Cierre con documentación:** al finalizar cada ventana se debe escalar una tarea de informe técnico.
- **Trazabilidad:** el esquema de apertura–seguimiento–informe garantiza que cada intervención quede registrada.

## Aplicaciones

- **Gestión de cambios en la red:** agendar modificaciones de infraestructura en franjas horarias acordadas para minimizar el impacto en el servicio.
- **Coordinación operativa con OTN:** mantener un canal formal de comunicación que permita conocer el estado y las novedades de las VMs en curso.
- **Escalamiento de informes técnicos:** generar y escalar el informe técnico al cierre de cada ventana, dejando constancia de lo ejecutado.
- **Auditoría y control:** disponer de un historial de intervenciones que facilite el análisis posterior de incidentes o cambios.

## Conceptos relacionados

## Entidades relacionadas

- [[entities/otn|OTN]]
- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "Tareas sisrred // Ventanas de Mantenimiento" — [[Work/1. Backbone|1. Backbone]]
- "Se debe llamar a preguntar cualquier novedad sobre las VMs planificadas" — [[Work/1. Backbone|1. Backbone]]
- "Se debe escalar tarea de informe tecnico al finalizar las VMs" — [[Work/1. Backbone|1. Backbone]]