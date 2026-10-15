---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "TIS ID"
  - "ID de Sparkle"
  - "Ticket ID de Sparkle"
generation_complete: true
---

# TIS-ID

## Definición

El **TIS-ID** es el identificador de ticket que **Sparkle (Telecom Italia Sparkle)** utiliza para el seguimiento de casos escalados. Aparece como campo obligatorio dentro de la plantilla de escalamiento dirigida a Sparkle, junto con la fecha de inicio (Start Date) y la zona horaria (Time Zone: GTM-5). Funciona como referencia única que permite a [[Telconet]] y [[Sparkle]] correlacionar un mismo incidente a lo largo del proceso de escalamiento.

## Características clave

- **Identificador de ticket**: es un código de referencia único asociado a un caso escalado ante Sparkle.
- **Emisor/Receptor**: lo asigna y administra Sparkle; lo consume Telconet para dar seguimiento.
- **Obligatoriedad**: su inclusión es requerida al enviar una solicitud al correo `contactcenter.tis@tisparkle.com`.
- **Contexto de la plantilla**: se solicita junto con la fecha de inicio (Start Date) y la zona horaria (Time Zone: GTM-5).
- **Función de correlación**: permite vincular el registro interno del incidente con el registro del proveedor, evitando ambigüedad entre casos similares.
- **Ámbito**: aplica al canal de escalamiento internacional con Sparkle.

## Aplicaciones

- **Apertura de escalamientos**: completar la plantilla de escalamiento enviada a Sparkle con el TIS-ID correspondiente.
- **Seguimiento de casos**: consultar el estado de un incidente usando el TIS-ID como clave de búsqueda ante el proveedor.
- **Correlación de incidentes**: cotejar el ticket interno de Telconet con el registro de Sparkle durante la gestión del [[Caso técnico]].
- **Trazabilidad y auditoría**: documentar el historial de un [[Escalamiento]] con una referencia verificable entre ambas partes.
- **Comunicación con el centro de contacto**: incluir el TIS-ID en los correos dirigidos a `contactcenter.tis@tisparkle.com` para agilizar la atención.

## Conceptos relacionados

- [[concepts/escalamiento|Escalamiento]]
- [[concepts/caso-técnico|Caso técnico]]

## Entidades relacionadas

- [[entities/sparkle|Sparkle]]
- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "TIS-ID: " (TIS-ID: ) — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Start Date: 
Time Zone: GTM-5 " (Fecha de inicio: 
Zona horaria: GTM-5 ) — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]