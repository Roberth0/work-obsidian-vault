---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "Ruckus Wireless"
  - "Controladora RUCKUS"
generation_complete: true
---

# RUCKUS

## Descripción

RUCKUS es una marca/producto de controladora inalámbrica mencionada explícitamente en el documento fuente. Dentro del flujo operativo descrito, RUCKUS funciona como una referencia técnica para determinar el tratamiento de los puntos de acceso: cuando la controladora del AP es de tipo RUCKUS, corresponde aplicar una regla especial consistente en agregar el prefijo `6.` al actualizar las [[MACROS]]. Esta condición particular condiciona el comportamiento del proceso de [[Ingresos de APs]], diferenciándolo del procedimiento aplicado con otros tipos de controladora. El documento asociado a [[Telcograph]] recoge esta indicación, por lo que RUCKUS actúa como un criterio de clasificación para la configuración de puntos de acceso.

## Entidades relacionadas

- [[entities/telcograph|Telcograph]]

## Conceptos relacionados

- [[concepts/macros|MACROS]]
- [[concepts/ingresos-de-aps|Ingresos de APs]]

## Menciones en la fuente

- "Actualizar MACROS, si la controladora es **RUCKUS** agregar *6.* adelante" — [[Work/4.1 Telcograph|4.1 Telcograph]]