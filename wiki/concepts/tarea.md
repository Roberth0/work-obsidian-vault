---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "ticket"
  - "número de tarea"
  - "caso"
generation_complete: true
---

# Tarea

## Definición

Una **Tarea** es el término empleado por [[Telconet S.A.]] para designar los tickets o casos numerados mediante los cuales se registra, asigna y da seguimiento a las incidencias de red dentro del flujo operativo del [[NOC]]. Cada tarea posee un identificador numérico único (por ejemplo, 107963875, 102759089, 101743384 o 102757614) que permite rastrear el incidente desde su apertura hasta su resolución o escalamiento. En la documentación operativa, el término se usa de manera intercambiable con "caso", como ocurre con el caso 20240430-0187B.

## Características clave

- **Identificador numérico único**: cada tarea se nombra con un número de ticket que la distingue de forma inequívoca (por ejemplo, tarea 107963875).
- **Asignación a un equipo responsable**: la tarea se deriva a un grupo de trabajo concreto, como [[RADIO UIO]] o L1, según el tipo de incidencia.
- **Fecha de apertura**: una tarea puede estar "aperturada" desde una fecha determinada, dato que sirve para medir el tiempo de atención.
- **Objeto de la incidencia**: el ticket describe el problema a resolver, por ejemplo soporte de AP en un nodo WiFi, pérdida de monitoreo o afectación a un cliente específico.
- **Trazabilidad y escalamiento**: es el mecanismo central que permite seguir el ciclo de vida de una incidencia y escalarla entre niveles de soporte.
- **Equivalencia con "caso"**: el término se emplea como sinónimo de caso, especialmente cuando el identificador sigue un formato de fecha y código (caso 20240430-0187B).

## Aplicaciones

- **Registro de incidencias de red**: apertura de tareas para documentar fallas detectadas de forma manual o mediante [[Monitorización proactiva]].
- **Soporte de infraestructura inalámbrica**: tareas como la 107963875, asociadas a soporte de AP en un nodo WiFi, vinculadas a [[Enlace WIFI]].
- **Seguimiento de pérdida de monitoreo**: tareas como la 102759089, correspondiente a la pérdida de monitoreo de parquesanrafael1.
- **Atención a clientes corporativos**: tareas como la 101743384, asociada al cliente danec.
- **Coordinación y derivación entre equipos**: asignación de tareas a grupos como [[RADIO UIO]] o L1 para su diagnóstico y resolución.
- **Escalamiento operativo**: uso del número de tarea como referencia común en la comunicación entre niveles del NOC.

## Conceptos relacionados

- [[concepts/login|Login]]
- [[concepts/enlace-wifi|Enlace WIFI]]
- [[concepts/monitorización-proactiva|Monitorización proactiva]]

## Entidades relacionadas

- [[entities/radio-uio|RADIO UIO]]
- [[entities/noc|NOC]]
- [[entities/telconet|Telconet S.A.]]

## Menciones en la fuente

- "Estimados RADIO UIO, se asigna la tarea: 107963875 para realizar el soporte. // Login: AP_NODO-WIFIPOMASQUIUIO" — [[Work/3. Corporativos|3. Corporativos]]
- "Se informa que se ha aperturado la tarea: 102759089 para realizar el soporte." — [[Work/3. Corporativos|3. Corporativos]]
- "Estimados L1 se escala el caso 20240430-0187B Caida del servicio de clientes que dependen de la ruta: GYE-Miraflores 1-Puerto Hondo 1/Puerto Azul 1-F01" — [[Work/3. Corporativos|3. Corporativos]]