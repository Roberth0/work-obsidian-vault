---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "Escalamiento de proveedores"
  - "Niveles de escalamiento"
  - "Escalation"
generation_complete: true
---

# Escalamiento

## Definición

El escalamiento es el procedimiento mediante el cual Telconet contacta y sube de nivel la gestión de un incidente con un proveedor internacional, con el objetivo de acelerar la resolución de una afectación en los enlaces del [[Backbone]] y obtener la restitución del servicio o la información de causa raíz. El proceso se documenta por proveedor, de modo que cada uno cuenta con sus propios contactos, correos y niveles de atención.

## Características clave

- Es un procedimiento operativo estructurado **por proveedor**: el documento lo organiza en secciones como "Escalamiento Sparkle", "Escalamiento Claro" y "Escalamiento CNT".
- Define **niveles de escalamiento** progresivos, descritos explícitamente para proveedores como Cables & Wireless y PCCW.
- Cada proveedor dispone de **contactos y correos específicos** (mesas de ayuda, NOC, ingenieros de cuenta) que se utilizan durante el proceso.
- Para **CNT**, el escalamiento implica **generar un caso técnico** sobre el login correspondiente.
- Se activa típicamente cuando la atención de primer nivel no resuelve el incidente dentro de los tiempos esperados.
- Está vinculado a la solicitud formal del [[RFO]] (motivo de la falla) al proveedor una vez restablecido el servicio.
- Genera trazabilidad: cada escalamiento queda registrado con su nivel, contacto y evidencia del incidente.

## Aplicaciones

- Gestión de incidentes en enlaces internacionales del backbone: caídas totales, cortes de fibra, degradación de latencia o pérdida de paquetes.
- Activación de contactos de nivel superior en proveedores como Sparkle, Claro, CNT, Cables & Wireless y PCCW cuando la respuesta del primer nivel es insuficiente.
- Apertura y seguimiento de [[Caso técnico|casos técnicos]] con el proveedor (por ejemplo, sobre el login de CNT) hasta su cierre.
- Solicitud y seguimiento del [[RFO]] posterior a la resolución del evento.
- Documentación y estandarización de contactos por proveedor para su uso recurrente por parte del equipo de operaciones de red.

## Conceptos relacionados

- [[concepts/caso-técnico|Caso técnico]]
- [[concepts/rfo|RFO]]

## Entidades relacionadas

- [[entities/claro|Claro]]
- [[entities/sparkle|Sparkle]]
- [[entities/cnt|CNT]]
- [[entities/cables-&-wireless|Cables & Wireless]]
- [[entities/backbone|Backbone]]

## Menciones en la fuente

- "Nivel de Escalamiento" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Escalamiento Claro" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]