---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
tags:
aliases:
  - "Backbone Proveedores Internacionales"
  - "Proveedores Internacionales de Backbone"
  - "International Backbone Providers"
generation_complete: true
---

# 1.2 Backbone Proveedores Internacionales

## Definición

**1.2 Backbone Proveedores Internacionales** es el documento operativo de [[Telconet]] que concentra la información de contacto, escalamiento y credenciales de acceso necesarias para gestionar los enlaces de backbone internacionales de la red. Funciona como referencia única para el personal de operaciones y de soporte que debe coordinar incidentes con proveedores externos de capacidad internacional.

## Características clave

- Reúne los **contactos operativos y de escalamiento** de los proveedores internacionales de backbone, incluyendo listas de correos específicas por proveedor y por nivel de escalamiento.
- Documenta el uso de la **herramienta de monitoreo de salidas internacionales (NetFlow)**, con enlaces directos a los tableros de consulta de tráfico.
- Define un **flujo de gestión de casos de backbone**: apertura de tareas de seguimiento durante el incidente y creación de tareas de RFO (Reason For Outage) al momento de la resolución.
- Registra **proveedores internacionales** como [[Akamai]], [[Cables & Wireless]] (C&W), [[PCCW]], [[Sparkle]], [[Claro]] y [[CNT]], cada uno con su propio esquema de contacto.
- Detalla los **logins de circuitos CNT** (cnt-burts, cnt-inaquito-bogota, tn-cnt-salinas, tn-cnt-manta) vinculados a IDs de Telconet y de C&W.
- Incluye el **circuito UFINET ECCOTEL10267004C** asociado a Edge uno, las credenciales del **Portal Arelion** y una referencia al nodo **PE05CAR**.

## Aplicaciones

- **Gestión de incidentes de backbone internacional**: permite identificar de inmediato a quién escalar según el proveedor afectado y el nivel de severidad del caso.
- **Monitoreo proactivo de tráfico internacional**: el uso de NetFlow facilita la detección de degradaciones o saturación en las salidas internacionales antes de que impacten al cliente final.
- **Cierre formal de incidentes**: la creación de tareas de RFO garantiza la documentación de la causa raíz y alimenta los procesos de mejora continua.
- **Aprovisionamiento y verificación de circuitos**: los logins de circuitos CNT y la información del circuito UFINET permiten validar el estado de los enlaces contratados.
- **Acceso a portales de proveedor**: las credenciales del Portal Arelion habilitan la consulta directa de información operativa del proveedor.

## Conceptos relacionados

## Entidades relacionadas

- [[entities/akamai|Akamai]]
- [[entities/cables-&-wireless|Cables & Wireless]]
- [[entities/sparkle|Sparkle]]