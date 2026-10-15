---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "Caso técnico"
  - "Caso tecnico CNT"
  - "Ticket técnico"
generation_complete: true
---

# Caso técnico

## Definición

Un **caso técnico** es el mecanismo formal que [[Telconet]] debe generar para escalar incidentes con [[CNT]]. Constituye la vía oficial de comunicación y seguimiento de incidentes con este proveedor internacional del backbone.

De acuerdo con la documentación de referencia, para iniciar el escalamiento se debe generar un caso técnico sobre el login que corresponda de acuerdo al ID de circuito de Telconet, es decir, el caso se registra contra el identificador de acceso asociado al circuito afectado y no de forma genérica.

## Características clave

- **Formalidad**: es un procedimiento reglado, no una comunicación informal entre operadores; requiere apertura y registro formal ante el proveedor.
- **Vinculación al ID de circuito**: el caso técnico se asocia al *login* CNT que corresponde al ID de circuito de Telconet involucrado.
- **Dependencia del login correcto**: su aplicación efectiva depende de identificar correctamente el login ligado al circuito; un login erróneo desvía o invalida el caso.
- **Naturaleza de escalamiento**: se utiliza cuando el incidente requiere intervención del proveedor, integrándose en el flujo de [[Escalamiento]].
- **Trazabilidad**: al ser un caso registrado, permite seguimiento, asignación de responsables y posterior documentación del cierre mediante un [[RFO]].
- **Ámbito**: aplica a los enlaces de backbone internacional provistos por CNT, identificados por logins como `cnt-burts`, `cnt-inaquito-bogota`, `tn-cnt-salinas` y `tn-cnt-manta`.

## Aplicaciones

- **Escalamiento de incidentes con CNT**: cuando una falla o degradación en un enlace del [[Backbone]] no se resuelve por las vías ordinarias de monitoreo y notificación.
- **Apertura por circuito afectado**: el operador identifica el ID de circuito de Telconet y determina el login CNT correspondiente antes de generar el caso.
- **Gestión de enlaces internacionales**: aplicable a los distintos logins CNT documentados (`cnt-burts`, `cnt-inaquito-bogota`, `tn-cnt-salinas`, `tn-cnt-manta`) y a cualquier enlace que se integre bajo el mismo esquema.
- **Seguimiento y cierre**: el caso técnico es el expediente sobre el que se solicita diagnóstico, se recibe respuesta del proveedor y se documenta la causa raíz.
- **Soporte a la documentación posterior**: alimenta la elaboración del RFO y de los informes de afectación de servicio.

## Conceptos relacionados

- [[concepts/escalamiento|Escalamiento]]
- [[concepts/rfo|RFO]]

## Entidades relacionadas

- [[entities/cnt|CNT]]
- [[entities/telconet|Telconet]]
- [[entities/cables-&-wireless|Cables & Wireless]]
- [[entities/backbone|Backbone]]

## Menciones en la fuente

- "Se debe genera un ~={red}caso tecnico =~ sobre el login que corresponda de acuerdo al ID de circuito de TELCONET" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]