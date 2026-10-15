---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "Wireless - All APs"
  - "All APs"
  - "sección Wireless"
generation_complete: true
---

# Wireless / All APs

## Definición

**Wireless / All APs** es la ruta de navegación específica de la interfaz de la [[Controladora]] inalámbrica que se debe consultar para validar el estado de los puntos de acceso ([[Access Point]]). Corresponde al apartado de la controladora donde se listan todos los APs registrados y desde el cual el equipo de soporte verifica su disponibilidad dentro de los nodos WiFi.

Según el procedimiento operativo documentado, para validar los APs se debe acceder a la controladora en la dirección 181.198.110.134 y ubicarse en la sección **Wireless / All APs**.

## Características clave

- Es una **ruta de navegación de la interfaz**, no un dispositivo ni un servicio de red en sí mismo.
- Agrupa el listado completo (*All APs*) de puntos de acceso administrados por una misma controladora.
- Requiere autenticación previa mediante [[Credenciales]] válidas y el correspondiente [[Login]] en la controladora.
- Se consulta sobre una controladora concreta, identificada por su dirección IP dentro de la red corporativa.
- Forma parte del **procedimiento de verificación** de disponibilidad de APs en los nodos de [[Enlace WIFI]].
- Su revisión permite determinar si un AP está en línea, registrado o con problemas de conexión con la controladora.

## Aplicaciones

- **Soporte operativo:** validar el estado de los puntos de acceso cuando se reporta una incidencia de conectividad inalámbrica en un nodo WiFi.
- **Verificación de disponibilidad:** confirmar que los APs de un sitio aparecen registrados y activos en la controladora antes de escalar un caso.
- **Diagnóstico de enlaces:** contrastar la información del AP con el estado del [[Enlace WIFI]] para descartar fallas de cobertura o de registro.
- **Tareas del equipo de radio:** actividad de revisión asignada al equipo responsable de la red inalámbrica.
- **Auditoría de inventario inalámbrico:** conocer cuántos APs están asociados a una controladora en un momento dado.

## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[access-point|Access Point]]
- [[concepts/login|Login]]
- [[concepts/enlace-wifi|Enlace WIFI]]

## Entidades relacionadas

- [[entities/telconet|Telconet S.A.]]
- [[entities/0-1-correos-y-claves|Credenciales]]

## Menciones en la fuente

- "Para validar los APs, se debe acceder a la controladora `181.198.110.134`en la seccion ***Wireless / All APs***" — [[Work/3. Corporativos|3. Corporativos]]