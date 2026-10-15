---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "Login CNT"
  - "ID de circuito"
  - "Circuit Login"
generation_complete: true
---

# Login de circuito

## Definición

El **login de circuito** es la denominación que [[Telconet]] utiliza para identificar cada enlace contratado con [[CNT]] y sobre el cual se debe generar un [[Caso técnico]]. Funciona como el identificador operativo que vincula un circuito del backbone con su proveedor, su documentación de soporte (capturas de pantalla, registros de configuración) y el proceso formal de [[Escalamiento]].

Cada login corresponde a un enlace específico y actúa como llave de referencia única para la gestión de incidentes, de modo que tanto Telconet como el proveedor puedan rastrear el mismo circuito a lo largo del flujo de soporte.

## Características clave

- **Formato de nomenclatura mixto**: los identificadores combinan prefijos de proveedor, como `cnt-` (CNT) y `tn-cnt-` (Telconet–CNT), seguidos del nombre del enlace o de la ciudad.
- **Unicidad por enlace**: cada login identifica un enlace concreto y no un servicio genérico; en el documento se enumeran varios, entre ellos `cnt-burts`, `cnt-inaquito-bogota`, `tn-cnt-salinas` y `tn-cnt-manta`.
- **Trazabilidad documental**: cada login está asociado a capturas de pantalla específicas que evidencian el estado del enlace.
- **Correspondencia multi-proveedor**: en enlaces internacionales, un mismo circuito puede recibir identificadores distintos según quién lo reporte. Para el login `cnt-inaquito-bogota`, CNT reporta los IDs de Telconet y Telconet reporta los CID de [[Cables & Wireless]].
- **Disparador de proceso**: la existencia del login habilita la apertura de un caso técnico formal con el proveedor.

## Aplicaciones

- **Gestión de incidentes de backbone**: permite referenciar de forma inequívoca el enlace afectado al reportar una falla a [[CNT]] o a [[Cables & Wireless]].
- **Apertura y seguimiento de casos técnicos**: el login es el dato mínimo requerido para generar el [[Caso técnico]] y para dar seguimiento a su estado.
- **Escalamiento con proveedores**: facilita el [[Escalamiento]] al traducir los identificadores internos de Telconet a los identificadores que cada proveedor reconoce (IDs de Telconet, CID de C&W).
- **Documentación y auditoría**: las capturas de pantalla asociadas a cada login sirven como evidencia de configuración y de estado del enlace.
- **Inventario de enlaces internacionales**: la lista de logins funciona como inventario operativo de los circuitos contratados con proveedores internacionales.

## Conceptos relacionados

- [[concepts/caso-técnico|Caso técnico]]
- [[concepts/escalamiento|Escalamiento]]

## Entidades relacionadas

- [[entities/cnt|CNT]]
- [[entities/cables-&-wireless|Cables & Wireless]]
- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "Se debe genera un ~={red}caso tecnico =~ sobre el login que corresponda de acuerdo al ID de circuito de TELCONET" (Se debe generar un caso técnico sobre el login que corresponda de acuerdo al ID de circuito de TELCONET) — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]