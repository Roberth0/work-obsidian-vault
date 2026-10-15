---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Escalamiento a TS y L1"
  - "Escalar el caso a L1"
  - "Escalar la tarea a TS"
generation_complete: true
---

# Escalamiento a TS y L1

## Definición

El **escalamiento a TS y L1** es el procedimiento operativo mediante el cual, ante una incidencia de CSCG, se crea un caso normal y se distribuye la carga de trabajo entre distintos niveles de soporte: la tarea se escala a la TS (Soporte Técnico) y el caso se escala a L1 (Nivel 1). El método define qué componente del flujo de resolución recibe cada nivel y garantiza la trazabilidad de la incidencia desde su registro hasta su atención.

## Características clave

- **Requiere la creación previa de un caso normal** en el sistema, que actúa como registro formal de la incidencia.
- **Distribución diferenciada por componente**: la *tarea* y el *caso* se escalan a niveles distintos (TS y L1 respectivamente), no como una única acción.
- **Dependencia del tipo de incidencia**: el destino del escalamiento varía según el evento (caída de OLT y cámaras, caída de ONT, caída de caja, entre otros).
- **Uso de la distribución de zonas**: en ciertos escenarios (por ejemplo, caída de ONT) el escalamiento de la tarea se determina según las zonas de GYE, consultando el Directorio Telefónico.
- **Trazabilidad**: al separar tarea y caso y asignarlos a niveles definidos, se conserva el seguimiento y la responsabilidad de cada componente.

## Aplicaciones

- **Caídas de OLT y cámaras (Machala y Salinas)**: se debe crear un caso normal, escalar la tarea a la TS y el caso a L1.
- **Caída de ONT**: se debe escalar la tarea de acuerdo con la distribución de zonas de GYE (consultando el Directorio Telefónico) y escalar el caso a L1.
- **Otras incidencias de CSCG** que requieran enrutar trabajo hacia el soporte de mayor especialización (TS) manteniendo el registro y seguimiento en el primer nivel (L1).

## Conceptos relacionados

- [[concepts/caida-de-caja|Caida de caja]]
- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]

## Entidades relacionadas

- [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]]
- [[entities/olt|OLT]]

## Menciones en la fuente

- "Se debe crear un caso normal y escalar la tarea a la TS y el caso a L1" — [[Work/2.1 CSCG|2.1 CSCG]]
- "1. Escalar tarea de acuerdo a la distribucion de zonas de GYE, para ello se debe llamar [[0. Directorio Telefonico]]" — [[Work/2.1 CSCG|2.1 CSCG]]
- "2. Escalar el caso a L1" — [[Work/2.1 CSCG|2.1 CSCG]]