---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "PID Claro"
  - "Product ID"
  - "Identificador de producto"
generation_complete: true
---

# PID

## Definición

El **PID** es el identificador que se incluye al escalar un incidente ante [[Claro]], conforme a la plantilla de escalamiento descrita en el documento de proveedores internacionales. En el ejemplo de la nota, el cuerpo del correo dirigido a Claro solicita su ayuda y a continuación presenta el campo `PID:` como dato obligatorio a completar.

Funciona como la referencia de circuito o servicio que permite a Claro localizar el caso dentro de su propia red, por lo que constituye un campo de identificación técnico-operativo empleado en la comunicación con el proveedor.

## Características clave

- **Identificador técnico-operativo:** no es un número de ticket genérico, sino la referencia del circuito o servicio implicado.
- **Obligatorio en la plantilla:** se presenta como un campo (`PID:`) que debe completarse al escalar el incidente.
- **Orientado al proveedor:** su función es permitir que el proveedor localice el caso dentro de su red.
- **Vinculado al contexto de escalamiento:** aparece junto al resto de los datos exigidos por la plantilla de escalamiento, incluidos los contactos de TIC Claro.
- **Específico por caso:** cada incidente escalado requiere el PID correspondiente al servicio afectado.

## Aplicaciones

- **Escalamiento de incidentes ante Claro:** se incorpora en el cuerpo del correo de escalamiento, después del mensaje de solicitud de ayuda, como dato obligatorio.
- **Localización del caso en la red del proveedor:** permite al proveedor identificar el circuito o servicio afectado y agilizar el diagnóstico.
- **Trazabilidad de la comunicación con el proveedor:** sirve como referencia común entre el equipo interno (por ejemplo, [[Telconet]]) y Claro durante el seguimiento del caso.
- **Completado de la plantilla de escalamiento:** es uno de los campos que deben rellenarse antes de enviar la solicitud formal.

## Conceptos relacionados

- [[concepts/escalamiento|Escalamiento]]
- [[concepts/caso-técnico|Caso técnico]]

## Entidades relacionadas

- [[entities/claro|Claro]]
- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "Estimados Claro

Por favor su ayuda ....

PID: " (Estimados Claro

Por favor su ayuda ....

PID: ) — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]