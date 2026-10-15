---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "Corporación Nacional de Telecomunicaciones"
  - "TELCONET-CNT"
generation_complete: true
---

# CNT

## Descripción

CNT (Corporación Nacional de Telecomunicaciones) es un proveedor de conectividad con el que [[Telconet]] gestiona circuitos internacionales. Para el escalamiento de incidentes ante CNT, el procedimiento documentado consiste en generar un caso técnico sobre el login que corresponda, de acuerdo con el ID de circuito de Telconet. Los logins habilitados para este propósito son `cnt-burts`, `cnt-inaquito-bogota`, `tn-cnt-salinas` y `tn-cnt-manta`, cada uno con su captura de pantalla asociada en la documentación de referencia. En el caso de `cnt-inaquito-bogota`, la operación es cruzada: CNT reporta los IDs de Telconet, mientras que Telconet reporta los CID de [[Cables & Wireless]]. CNT es, por tanto, un actor central para el escalamiento de circuitos hacia Colombia y otras rutas internacionales.

## Entidades relacionadas

- [[entities/cables-&-wireless|Cables & Wireless]]
- [[entities/telconet|Telconet]]
- [[entities/claro|Claro]]

## Conceptos relacionados

- [[concepts/caso-técnico|Caso técnico]]
- [[concepts/escalamiento|Escalamiento]]

## Menciones en la fuente

- "Se debe genera un ~={red}caso tecnico =~ sobre el login que corresponda de acuerdo al ID de circuito de TELCONET" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "- [ ] `cnt-burts`" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]