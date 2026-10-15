---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "comando show port"
  - "show port 2/3/2 | match tate"
generation_complete: true
---

# show port

## Definición

`show port` es un comando de red utilizado para verificar el estado operativo de un puerto y determinar el tiempo en que un enlace se cayó. Permite confirmar desde cuándo se produjo la interrupción del servicio, lo que resulta clave en el diagnóstico de enlaces reportados como caídos, como en el caso del enlace reportado en Cedia.

## Características clave

- Es un comando de consulta y diagnóstico, no de configuración: no modifica el estado del puerto, solo lo reporta.
- Devuelve información de estado del puerto, incluyendo si está activo o inactivo y por cuánto tiempo.
- Admite filtrado mediante tubería (`|`) hacia utilidades como `match`, lo que reduce la salida a los campos de interés.
- El filtrado con `match tate` (fragmento de la palabra "state") se utiliza para aislar la línea de estado y verificar fácilmente si el puerto está activo o inactivo.
- Se identifica el puerto por su notación jerárquica de módulo/ranura/puerto (por ejemplo, `2/3/2`).
- Permite acotar el momento de inicio de la caída del enlace, dato usado para correlacionar con otros eventos de red.

## Aplicaciones

- **Diagnóstico de enlaces caídos**: determinar si un puerto está activo o inactivo cuando se reporta una interrupción de servicio.
- **Determinación del tiempo de caída**: establecer desde cuándo se produjo la interrupción, como parte del procedimiento de diagnóstico del enlace reportado en Cedia.
- **Verificación puntual de un puerto**: consultar el estado de una interfaz específica sin desplegar la totalidad de la información del equipo.
- **Filtrado eficiente de salida**: emplear `show port <puerto> | match tate` para obtener únicamente la línea de estado en sesiones de diagnóstico rápidas.
- **Correlación con otros agregados**: complementar la revisión del puerto con la del agregado de enlaces mediante [[show lag description]] y con el análisis de [[link loss]].

## Conceptos relacionados

- [[concepts/show-lag-description|show lag description]]
- [[concepts/link-loss|link loss]]

## Entidades relacionadas

- [[entities/concentrador-de-ambato|Concentrador de Ambato]]
- [[entities/sam-client|SAM CLIENT]]

## Menciones en la fuente

- "5) Verificar tiempo en el que se cayo" (5) Verificar tiempo en el que se cayó) — [[Work/4 Cedia|4 Cedia]]
- "show port 2/3/2 | match tate" (show port 2/3/2 | match tate) — [[Work/4 Cedia|4 Cedia]]