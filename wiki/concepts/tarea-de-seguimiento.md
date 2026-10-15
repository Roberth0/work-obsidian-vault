---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "Tarea de tracking"
  - "Task de seguimiento"
  - "Tarea de seguimiento de caso"
generation_complete: true
---

# Tarea de seguimiento

## Definición

La **tarea de seguimiento** es un procedimiento interno de [[Telconet]] aplicado a los casos que afectan al [[Backbone]]. Consiste en la creación de una tarea asignada al perfil del técnico con el fin de contabilizar el tiempo transcurrido desde la apertura del caso hasta que el incidente queda solventado. Se trata de un mecanismo de registro y control operativo, no de un objeto técnico en sí mismo.

## Características clave

- **Se genera al abrir el caso**: la tarea se crea en el momento de la apertura del incidente, de modo que el conteo de tiempo comienza desde el primer instante.
- **Asignación por perfil**: la tarea queda asignada al perfil del técnico responsable de la atención del caso, lo que permite atribuir el tiempo de resolución a un rol concreto.
- **Función de contabilización**: su propósito principal es medir y dejar constancia del tiempo transcurrido hasta la resolución del incidente.
- **Complementariedad con el RFO**: una vez resuelto el incidente, la tarea de seguimiento se complementa con una tarea de [[RFO]], que documenta la causa raíz.
- **Carácter de trazabilidad**: no resuelve el incidente por sí misma; produce el registro que sustenta el reporte posterior.
- **Naturaleza de gestión**: es una práctica de gestión operativa dentro del flujo de atención de incidentes del backbone.

## Aplicaciones

- **Medición del tiempo de resolución (MTTR)**: permite calcular cuánto tarda un incidente de backbone en ser solventado, desde su apertura hasta su cierre.
- **Sustento del reporte posterior**: el registro generado sirve como evidencia y respaldo documental en los informes de gestión y de nivel de servicio.
- **Seguimiento de escalamientos**: se utiliza junto con el esquema de [[Escalamiento]] a proveedores internacionales, permitiendo observar cuánto tiempo permanece un caso en cada instancia hasta su resolución.
- **Control de casos sobre [[Salidas Internacionales]]**: aplicable a incidentes que afectan enlaces y salidas internacionales, donde la coordinación con terceros alarga los tiempos de resolución.
- **Auditoría interna**: facilita la revisión histórica de casos y la verificación de que cada incidente cuenta con su registro de tiempos y su correspondiente [[RFO]].

## Conceptos relacionados

- [[concepts/rfo|RFO]]
- [[concepts/escalamiento|Escalamiento]]
- [[concepts/salidas-internacionales|Salidas Internacionales]]

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/backbone|Backbone]]

## Menciones en la fuente

- ">[!tip]+ Para casos de backbone se debe crear una tarea asigna a mi perfil para dar seguimiento del tiempo cuando se solvente el incidente. Cuando se solventa el incidente se crea una tarea de RFO" (>[!tip]+ Para casos de backbone se debe crear una tarea asignada a mi perfil para dar seguimiento del tiempo cuando se solvente el incidente. Cuando se solventa el incidente se crea una tarea de RFO) — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]