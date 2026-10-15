---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "caída de cámara"
  - "caida camara/s"
  - "Caída de cámara/s"
generation_complete: true
---

# Caida de camara/s

## Definición

La **Caida de camara/s** es uno de los escenarios de diagnóstico descritos en el documento de referencia y designa la pérdida de una o de varias cámaras de videovigilancia. El procedimiento de diagnóstico parte de la verificación del estado de la [[OLT]] en el [[OSS]] y, cuando se trata de una sola cámara, se espera que la OLT se encuentre activa; este criterio es el que permite distinguir el caso de una caída puntual del de una caída masiva. Posteriormente se realiza un `ping` hacia la cámara desde la pestaña «logico», obteniendo previamente su dirección IP a partir del inventario de [[Zabbix]]. Si no se recibe respuesta al [[Sin respuesta ICMP|ICMP]], se genera un caso por la caída desde Zabbix.

## Características clave

- Es un **escenario de diagnóstico** dentro del procedimiento operativo, no un fallo de red genérico.
- Afecta a **una o varias cámaras** del sistema de videovigilancia ([[Camaras]]).
- Exige como primer paso la **verificación del estado de la OLT en el OSS**.
- Con una sola cámara afectada, la **OLT debe permanecer activa**; este comportamiento diferencia el caso de una caída masiva.
- Requiere la **identificación previa de la IP de la cámara** mediante el inventario de Zabbix.
- Se confirma mediante **prueba de conectividad (`ping`) desde la pestaña «logico»**.
- La **ausencia de respuesta ICMP** determina la apertura de un caso por la caída desde Zabbix.

## Aplicaciones

- **Diagnóstico de incidencias en videovigilancia**: permite clasificar una pérdida de cámara como incidente puntual o como parte de una caída de mayor alcance.
- **Triaje operativo**: la correlación entre el estado de la OLT y el número de cámaras afectadas orienta la prioridad y el alcance del caso.
- **Gestión de tickets y escalado**: la creación del caso desde Zabbix cuando no hay respuesta ICMP asegura la trazabilidad de la incidencia.
- **Validación de conectividad extremo a extremo**: el `ping` desde la pestaña «logico» comprueba la alcanzabilidad efectiva de la cámara antes de declarar la caída.

## Conceptos relacionados

- [[concepts/sin-respuesta-icmp|Sin respuesta ICMP]]

## Entidades relacionadas

- [[entities/camaras|Camaras]]
- [[entities/oss|OSS]]
- [[entities/zabbix|Zabbix]]
- [[entities/olt|OLT]]

## Menciones en la fuente

- "Se debe verificar el estado  de la OLT en el [OSS](https://oss.netlife.net.ec/dashboard) para realizar el diagnostico, al ser solo una camara/s la OLT se deberia encontrar activa" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Posteriormente en la pestaña *logico* se debe hacer ping hacia la camara, para ello se debe conocer su IP mediante la opcion inventario del zabbix" — [[Work/2.1 CSCG|2.1 CSCG]]