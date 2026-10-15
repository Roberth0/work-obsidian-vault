---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "comando show lag description"
  - "show lag description | match UNIANDES"
  - "descripción de LAG"
generation_complete: true
---

# show lag description

## Definición

**show lag description** es un comando de red que permite consultar la composición de un agregado de enlaces (LAG, *Link Aggregation Group*): indica cuántos enlaces lo integran y cuáles son, así como su estado individual. Se ejecuta sobre un concentrador o un extremo de la red y su salida puede filtrarse para aislar únicamente los enlaces que pertenecen a un cliente determinado, por ejemplo mediante el filtro `| match UNIANDES`.

## Características clave

- Es un comando de **consulta y diagnóstico**, no de configuración: no modifica el estado del agregado de enlaces.
- Devuelve el **número y la identidad de los enlaces** que forman parte de un LAG, lo que permite verificar su composición real frente a la esperada.
- Admite **filtrado de salida** con `| match`, lo que permite acotar el resultado a un cliente o servicio concreto (por ejemplo, `show lag description | match UNIANDES`).
- Se aplica indistintamente sobre **concentradores** y sobre **extremos** (equipos terminales del enlace).
- Su resultado se interpreta junto con otras verificaciones de capa física y lógica para decidir las acciones correctivas sobre un enlace reportado.

## Aplicaciones

- **Diagnóstico de enlaces reportados:** dentro del procedimiento de revisión del enlace reportado en Cedia, el comando se utiliza para determinar el estado y la composición de los enlaces del servicio afectado antes de definir las acciones a seguir.
- **Identificación de enlaces por cliente:** combinado con `| match UNIANDES`, permite aislar los enlaces que corresponden al cliente UNIANDES dentro de la salida completa del equipo.
- **Verificación de LAG tras cambios o incidentes:** sirve para confirmar cuántos miembros activos conserva un agregado después de una caída, un mantenimiento o una reconfiguración.
- **Correlación con pérdida de enlaces:** al mostrar el número de enlaces presentes, ayuda a comprobar si una [[link loss]] observada se debe a la salida de uno o varios miembros del agregado.

## Conceptos relacionados

- [[concepts/link-loss|link loss]]

## Entidades relacionadas

- [[entities/concentrador-de-ambato|Concentrador de Ambato]]
- [[entities/sam-client|SAM CLIENT]]

## Menciones en la fuente

- "show lag description | match UNIANDES" (show lag description | match UNIANDES) — [[Work/4 Cedia|4 Cedia]]
- "4) Verificar cuantos enlaces tiene, para determinar que realizar" (4) Verificar cuántos enlaces tiene, para determinar qué realizar) — [[Work/4 Cedia|4 Cedia]]