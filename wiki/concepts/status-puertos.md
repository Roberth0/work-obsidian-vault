---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "status puertos"
  - "estado de los puertos"
  - "consulta del estado de los puertos"
generation_complete: true
---

# Status puertos

## Definición

**Status puertos** es la opción del [[OSS]] que permite consultar el estado de los puertos de una caja para localizar en qué puerto —y por tanto en qué caja— está conectada una [[OLT]] caída. Es un procedimiento de diagnóstico dentro del flujo de atención de caídas que, a partir del estado observado en los puertos, permite determinar si la caída es masiva o puntual.

## Características clave

- Es una consulta de estado, no una acción de configuración: su función es observar y localizar, no modificar el servicio.
- Permite identificar el puerto y la caja asociados a una OLT caída.
- Distingue el alcance de la falla según el patrón observado:
  - Si **todas las OLTs de la caja** aparecen caídas, se interpreta como una **caída de caja** (problema masivo).
  - Si **alguna OLT permanece activa**, se interpreta como un **problema puntual**.
- Es un paso previo a la decisión de tratamiento del incidente: caída de caja o incidente puntual.
- Forma parte del flujo de diagnóstico de caída de [[ONT]] y cámaras.

## Aplicaciones

- Diagnóstico de caída de ONT y cámaras: se ejecuta como paso intermedio para acotar el origen de la falla antes de escalar o derivar el caso.
- Diferenciación de incidentes masivos frente a incidentes puntuales, lo que orienta la prioridad y el equipo responsable de la resolución.
- Localización física/lógica del puerto y la caja afectados cuando se reporta una OLT caída.
- Soporte a la decisión operativa: si el resultado indica caída de caja, el caso se trata como caída masiva; si hay OLTs activas, se trata como incidente puntual.

## Conceptos relacionados

- [[concepts/caida-de-caja|Caida de caja]]
- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]

## Entidades relacionadas

- [[entities/oss|OSS]]
- [[entities/olt|OLT]]
- [[entities/ont|ONT]]

## Menciones en la fuente

- "En la opcion estado de los puertos (***status puertos***) debemos buscar el puerto y la caja a la cual esta conectada dicha OLT" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Se debe verificar el tipo de caida, si todos las OLTs de la caja se encuentran caidas se debe a un problema masivo / caida de caja. Si ahi alguna OLT activa significa que el problema es puntual." — [[Work/2.1 CSCG|2.1 CSCG]]