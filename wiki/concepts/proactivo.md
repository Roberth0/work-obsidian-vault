---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-vips_147ea4]]"
tags:
aliases:
  - "Proceso Proactivo"
  - "Proactivos"
generation_complete: true
---

# Proactivo

## Definición

El **proactivo** es el proceso mediante el cual el equipo genera casos de forma anticipada ante incidencias detectadas por el monitoreo, es decir, antes de que el cliente las reporte. Se trata de un mecanismo operativo que traslada los hallazgos del [[Monitoreo VIPS|monitoreo]] a la apertura formal de casos, organizando buena parte de las reglas operativas descritas en la fuente.

## Características clave

- Es un proceso de **apertura anticipada de casos**: el equipo abre el caso por iniciativa propia a partir de lo detectado por el monitoreo, sin esperar el reporte del cliente.
- Su disparador es una incidencia detectada por el monitoreo.
- **Obligatoriedad por cliente**: para los clientes [[Banco Bolivariano]] y [[Produbanco]] siempre se apertura casos en el proactivo, conforme a la disposición de Edson.
- **Excepción por reubicación**: cuando existe una orden de [[Reubicacion|reubicación]], no es necesario generar el proactivo para esos puntos.
- Involucra al equipo de [[NOC IPCCL1 PROACTIVOS]] como responsable de la generación de los casos.

## Aplicaciones

- Apertura proactiva de casos para clientes con cobertura permanente (Banco Bolivariano y Produbanco), donde no se espera el reporte del cliente para iniciar la gestión.
- Atención anticipada de incidencias detectadas por el monitoreo en puntos monitoreados.
- Exclusión del proceso en puntos que se encuentran bajo una orden de reubicación, evitando la apertura innecesaria de casos.
- Coordinación con incidencias de red, como el [[Corte de Ruta|corte de ruta]], que pueden detectarse desde el monitoreo y derivar en un caso proactivo.

## Conceptos relacionados

- [[concepts/vips|Monitoreo VIPS]]
- [[concepts/reubicacion|Reubicacion]]
- [[concepts/corte-de-ruta|Corte de Ruta]]

## Entidades relacionadas

- [[entities/banco-bolivariano|Banco Bolivariano]]
- [[entities/produbanco|Produbanco]]
- [[entities/noc-ipccl1-proactivos|NOC IPCCL1 PROACTIVOS]]

## Menciones en la fuente

- "chicos para los clientes Banco Bolivariano y Produbanco para el proactivo siempre se apertura casos, no se olviden de esa disposición" — [[Work/2. VIPS|2. VIPS]]
- "Chicos, respecto al proceso de proactivo. En los casos de clientes en los que se tenga una orden de reubicación, no es necesario generar el proactivo para esos puntos. ej:" — [[Work/2. VIPS|2. VIPS]]