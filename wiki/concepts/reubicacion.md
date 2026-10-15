---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-vips_147ea4]]"
tags:
aliases:
  - "Reubicación"
  - "Orden de Reubicación"
  - "Reubicación de puntos"
generation_complete: true
---

# Reubicacion

## Definición

La **reubicación** es una orden que se aplica a los puntos de determinados clientes dentro del proceso proactivo. Cuando un cliente cuenta con una orden de reubicación, los puntos asociados quedan exceptuados de la generación del proactivo, por lo que no se requiere abrir el caso correspondiente para esos puntos.

## Características clave

- Actúa como una **excepción** a la regla general de apertura de casos del proceso proactivo.
- Se aplica a un alcance acotado: únicamente los **puntos** de ciertos clientes, no a la totalidad de la cartera.
- Su presencia en un cliente determina que **no es necesario generar el proactivo** para los puntos afectados.
- Es una condición verificable y documentada, lo que permite decidir de forma anticipada si corresponde o no generar el proactivo.
- Es independiente del resultado del monitoreo: la excepción opera con prescindencia de que los puntos hayan sido detectados en el proceso.

## Aplicaciones

- **Filtrado previo en el proceso proactivo**: antes de generar el proactivo de un punto, se verifica si el cliente tiene una orden de reubicación vigente; de tenerla, el punto se omite.
- **Reducción de casos innecesarios**: evita la apertura de casos para puntos que serán reubicados, optimizando el esfuerzo operativo del equipo.
- **Documentación de escenarios**: el escenario se ilustra en el material de origen mediante una imagen de apoyo (Pasted image 20250426095923.png) que ejemplifica el caso de un cliente con orden de reubicación.
- **Criterio de excepción en monitoreo**: complementa las reglas de [[Monitoreo VIPS]] al definir cuándo un punto no debe ingresar al flujo de [[Proactivo]].

## Conceptos relacionados

- [[concepts/proactivo|Proactivo]]
- [[concepts/vips|Monitoreo VIPS]]

## Entidades relacionadas

## Menciones en la fuente

- "Chicos, respecto al proceso de proactivo. En los casos de clientes en los que se tenga una orden de reubicación, no es necesario generar el proactivo para esos puntos. ej:" — [[Work/2. VIPS|2. VIPS]]