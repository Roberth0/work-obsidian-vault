---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "login aux"
  - "nombre de usuario"
generation_complete: true
---

# Login

## Definición

**Login** es el término que designa el identificador de cuenta utilizado para asociar un equipo o un enlace dentro de las plataformas de monitoreo y de las controladoras de Telconet. Funciona como la clave operativa que permite vincular un dispositivo o circuito concreto con su registro correspondiente en los sistemas de gestión, de modo que su estado, sus métricas y las tareas asociadas puedan rastrearse de forma individualizada.

## Características clave

- **Identificador de asociación**: cada login vincula un equipo o enlace con su registro en las plataformas de monitoreo y controladoras de Telconet.
- **Formato heterogéneo**: los logins responden a convenciones de nomenclatura variadas según su origen, e incluyen prefijos de servicio, referencias a nodos, a sitios o a clientes.
- **Trazabilidad**: permiten seguir el estado de enlaces y APs, así como localizar el historial de tareas de soporte asociadas a cada elemento.
- **Responsabilidad operativa**: determinados conjuntos de logins quedan bajo la gestión de equipos específicos; por ejemplo, los logins con prefijo `tn_wifi2_` son gestionados por el [[NOC MIMG]] para [[Guayaquil]] y [[Quito]].
- **Distinción por alcance**: algunos logins identifican servicios masivos o de sitio, mientras que otros corresponden a clientes o nodos particulares.
- **Uso transversal**: aparecen tanto en tareas de soporte como en actividades de monitoreo proactivo.

## Aplicaciones

- **Monitoreo de enlaces y APs**: seguimiento del estado operativo de cada enlace o punto de acceso a partir de su login, lo que permite detectar degradaciones o caídas de servicio.
- **Gestión de tareas de soporte**: localización y priorización de tareas asociadas a un login concreto, facilitando la trazabilidad del caso.
- **Monitoreo proactivo**: identificación temprana de anomalías por parte de los equipos de NOC antes de que el usuario final las reporte.
- **Segmentación por cliente o sitio**: agrupación de equipos y enlaces según el login, lo que ayuda a distinguir entre infraestructura de sitio, de servicio y de cliente.
- **Control de responsabilidades**: asignación de la gestión de determinados rangos de logins a equipos concretos, como el caso de los logins `tn_wifi2_` a cargo del [[NOC MIMG]].

## Conceptos relacionados

- [[concepts/enlace-wifi|Enlace WIFI]]
- [[concepts/tarea|Tarea]]

## Entidades relacionadas

- [[entities/mimg|MIMG]]
- [[entities/gye|Guayaquil]]
- [[entities/uio|Quito]]
- [[entities/radio-uio|RADIO UIO]]
- [[entities/0-1-correos-y-claves|Credenciales]]

## Menciones en la fuente

- "Estimados RADIO UIO, se asigna la tarea: 107963875 para realizar el soporte. // Login: AP_NODO-WIFIPOMASQUIUIO" — [[Work/3. Corporativos|3. Corporativos]]
- "Mediante monitoreo se verifica enlace caído, asociado al login aux: coopjipijapa-tterrestregye_1 con IP: 181.39.39.230 CONTACTO: 052600367." — [[Work/3. Corporativos|3. Corporativos]]