---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "Concentrador Ambato"
  - "Ambato Concentrator"
  - "Concentrador de la Red Metropolitana de Ambato"
generation_complete: true
---

# Concentrador de Ambato

## Descripción

El **Concentrador de Ambato** es el equipo de agregación desde el cual se recomienda iniciar la verificación de un enlace reportado en [[CEDIA]]. Según el procedimiento establecido, el técnico debe ingresar al [[SAM CLIENT]], buscar los extremos del enlace reportado y comenzar la revisión precisamente por este concentrador. Se trata del punto central de la red Metropolitana de Ambato, donde convergen los enlaces de los clientes atendidos por esa red. Su función como nodo de agregación lo convierte en el primer punto de control ante cualquier incidencia de conectividad en la zona.

La importancia operativa del concentrador radica en que permite determinar cuántos enlaces tiene asociados, dato que a su vez define las acciones a seguir durante el diagnóstico. Si el problema se manifiesta en este punto de convergencia, es probable que afecte a múltiples clientes de forma simultánea; si no, la falla suele localizarse en un tramo o enlace individual hacia el usuario final. En el contexto del análisis de [[link loss]], revisar el concentrador permite descartar o confirmar un origen común de la pérdida de enlace antes de escalar la revisión hacia otros segmentos de la red. Es, por tanto, el elemento de referencia obligado para la verificación de enlaces reportados en la infraestructura de [[CEDIA]].

## Entidades relacionadas

- [[entities/sam-client|SAM CLIENT]]
- [[entities/cedia|CEDIA]]

## Conceptos relacionados

- [[concepts/link-loss|link loss]]

## Menciones en la fuente

- "3) Entrar a los extremos para verificar, empezar por el Concentrador de Ambato" (3) Entrar a los extremos para verificar, empezar por el Concentrador de Ambato) — [[Work/4 Cedia|4 Cedia]]
- "4) Verificar cuantos enlaces tiene, para determinar que realizar" (4) Verificar cuántos enlaces tiene, para determinar qué realizar) — [[Work/4 Cedia|4 Cedia]]