---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Corte de fibra óptica"
  - "Motivo NOC: Corte de Fibra"
  - "Fiber cut"
generation_complete: true
---

# Corte de Fibra

## Definición

El **Corte de Fibra** es una causa de incidencia que se registra como **motivo NOC** en el seguimiento de tareas de caída de [[ONT]] y cámaras. Corresponde a la clasificación que el área NOC asigna a la interrupción del servicio cuando el origen del problema se identifica en el segmento de fibra óptica, y se documenta de forma complementaria al **motivo OSS**.

## Características clave

- Se registra como **motivo NOC**, acompañando —no sustituyendo— al motivo OSS de la incidencia.
- Aparece tanto en el flujo de tareas de caída de ONT y cámaras como en la plantilla de **caídas masivas**.
- Se asocia típicamente con el motivo OSS "Corte de ultima Milla" / "Corte de UM", lo que lo vincula a fallas en la última milla de la red.
- Convive con el registro de datos técnicos de la incidencia: **login aux**, **IP** y la **UM de la OLT afectada**.
- Funciona como etiqueta de clasificación que permite agrupar, priorizar y dar trazabilidad a las incidencias por corte de fibra.

## Aplicaciones

- **Registro de incidencias en tareas de caída de ONT y cámaras:** al documentar la caída, se ingresa el motivo NOC junto al motivo OSS; por ejemplo, `Motivo NOC: Corte de Fibra` con `Motivo OSS: Corte de ultima Milla`.
- **Gestión de caídas masivas:** se utiliza la plantilla correspondiente, donde figura `Motivo NOC: Corte de Fibra` y `Motivo OSS: Corte de UM`, permitiendo estandarizar la comunicación del evento.
- **Trazabilidad operativa:** al acompañar datos como login aux, IP y la UM de la OLT afectada, facilita la localización del tramo de fibra comprometido y el posterior análisis de recurrencia.
- **Reportes y análisis de causas:** al ser un valor de motivo NOC, permite clasificar estadísticamente las incidencias atribuibles a fibra óptica frente a otras causas.

## Conceptos relacionados

- [[concepts/corte-de-ultima-milla|Corte de ultima Milla]]
- [[concepts/motivo-noc-y-motivo-oss|Motivo NOC y Motivo OSS]]
- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]
- [[concepts/caida-de-caja|Caida de caja]]

## Entidades relacionadas

- [[entities/oss|OSS]]
- [[entities/olt|OLT]]
- [[entities/ont|ONT]]

## Menciones en la fuente

- "Motivo NOC: Corte de Fibra" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Motivo OSS: Corte de ultima Milla" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Motivo NOC: Corte de Fibra
Motivo OSS: Corte de UM" — [[Work/2.1 CSCG|2.1 CSCG]]