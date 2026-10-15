---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "Enlace inalámbrico"
  - "TIPO ENLACE: WIFI"
  - "enlace caído"
generation_complete: true
---

# Enlace WIFI

## Definición

**Enlace WIFI** es el término con el que [[Telconet S.A.]] designa los vínculos inalámbricos monitoreados dentro de su red corporativa. Se trata de un enlace de acceso cuya caída es detectada por el sistema de monitoreo y que se registra y reporta dentro de los documentos operativos de la compañía.

## Características clave

- Se identifica de forma explícita en los reportes mediante la etiqueta `TIPO ENLACE: WIFI`.
- Cada enlace se describe con un conjunto de atributos operativos: tipo de enlace, ciudad, dirección, y el [[Login]] asociado al servicio.
- Está sujeto a [[Monitorización proactiva]]: la caída se detecta antes de que el cliente la reporte y genera una notificación automática.
- La notificación de pérdida de monitoreo se envía al cliente por correo electrónico.
- Puede vincularse a una [[MAC]] dentro de la infraestructura de red asociada.
- Cuando se detecta una caída, el enlace se valida y se asocia a una [[Tarea]] de soporte.
- Se documenta con ejemplos concretos, como el enlace del cliente con login `tn_wifi2_parquesanrafael1`, clasificado como `TIPO ENLACE: WIFI` en la ciudad de UIO ([[Quito]]).
- Sus registros se distribuyen geográficamente entre las plazas operativas de Telconet, incluyendo [[Quito]] y [[Guayaquil]].

## Aplicaciones

- **Reporte de caídas de servicio**: documentar la pérdida de conectividad inalámbrica de un cliente y su trazabilidad operativa.
- **Notificación al cliente**: envío automático del correo de pérdida de monitoreo cuando el enlace cae.
- **Gestión de soporte**: validación del enlace caído y creación de tareas de soporte asociadas a su login.
- **Auditoría de infraestructura inalámbrica**: inventario de enlaces WIFI por ciudad, dirección y login para análisis operativo.
- **Integración con controladoras**: administración y verificación de los vínculos inalámbricos a través de la [[Controladora]] correspondiente.

## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[concepts/monitorización-proactiva|Monitorización proactiva]]
- [[concepts/tarea|Tarea]]
- [[concepts/login|Login]]
- [[concepts/mac|MAC]]

## Entidades relacionadas

- [[entities/telconet|Telconet S.A.]]
- [[entities/uio|Quito]]
- [[entities/gye|Guayaquil]]

## Menciones en la fuente

- "Por monitoreo se observa caído el enlace:" — [[Work/3. Corporativos|3. Corporativos]]
- "TIPO ENLACE: WIFI" — [[Work/3. Corporativos|3. Corporativos]]
- "Se informa que se ha aperturado la tarea: 102759089 para realizar el soporte." — [[Work/3. Corporativos|3. Corporativos]]