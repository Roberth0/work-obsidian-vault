---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "Reason For Outage"
  - "Reporte RFO"
generation_complete: true
---

# RFO

## Definición

RFO (acrónimo de *Reason For Outage*, "razón de la interrupción") es el informe que documenta la causa que originó una caída o interrupción del servicio. En el flujo operativo descrito en el documento, el RFO se constituye como el entregable formal que se genera tras solventar un incidente de [[Backbone|backbone]]: una vez restablecido el servicio, se crea la tarea de RFO correspondiente, cuyo propósito es dejar constancia escrita de la razón de la caída y de las acciones asociadas a su resolución.

## Características clave

- **Entregable obligatorio del proceso**: no es un documento opcional, sino una tarea generada de forma sistemática al cierre de cada incidente de backbone.
- **Vinculado a una tarea de seguimiento**: se asocia a la tarea que se crea al inicio del caso, de modo que la trazabilidad queda cubierta desde la apertura hasta el cierre.
- **Elaboración posterior a la solución**: se genera cuando el incidente ya ha sido solventado, no durante la fase de diagnóstico.
- **Carácter documental**: su función es explicar y registrar la causa de la interrupción, no ejecutar la restauración del servicio.
- **Criterio de cierre formal**: constituye el paso que permite dar por concluido administrativamente un caso técnico de backbone.

## Aplicaciones

- **Cierre formal de casos técnicos**: se utiliza como requisito para dar por terminado un incidente de backbone una vez restablecido el servicio.
- **Documentación de causa raíz**: sirve como registro histórico de por qué se produjo la caída, lo que facilita el análisis posterior de recurrencia.
- **Trazabilidad ante el cliente o proveedor**: al ser un entregable formal, permite respaldar la comunicación de lo ocurrido con un documento verificable.
- **Retroalimentación de la operación**: los informes acumulados alimentan la revisión de procesos de [[Escalamiento|escalamiento]] y de gestión de incidentes.
- **Evidencia para la mejora continua**: la información recogida ayuda a identificar patrones y a prevenir incidentes similares.

## Conceptos relacionados

- [[concepts/escalamiento|Escalamiento]]
- [[concepts/caso-técnico|Caso técnico]]

## Entidades relacionadas

- [[entities/telconet|Telconet]]
- [[entities/backbone|Backbone]]

## Menciones en la fuente

- "Cuando se solventa el incidente se crea una tarea de RFO" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]