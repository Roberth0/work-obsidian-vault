---
type: concept
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "dirección MAC"
  - "MAC address"
  - "Media Access Control address"
---

# MAC

## Definición

MAC (Media Access Control) es el término que designa la dirección física de un dispositivo de red: un identificador único asignado al hardware de una interfaz de red, utilizado para identificar equipos de forma inequívoca dentro de un segmento de red y para diagnosticar problemas de conectividad. En el documento de referencia se emplea tanto para individualizar un equipo concreto como para describir el estado de aprendizaje de direcciones en la tabla de un switch de acceso.

## Características clave

- Se compone de seis octetos expresados normalmente en notación hexadecimal, habitualmente separados por espacios o dos puntos (por ejemplo, `2C AC 5C 9C B0`).
- Es una dirección de capa 2 (enlace de datos) asignada al hardware o a la interfaz virtual del dispositivo.
- Identifica de manera única a un dispositivo dentro de una red local, a diferencia de las direcciones de capa 3 (IP), que son lógicas y reasignables.
- Los switches aprenden las direcciones MAC asociándolas a sus puertos físicos; cuando un puerto no registra aprendizajes, se considera evidencia de un problema de enlace.
- Sirve como dato de correlación entre el inventario de equipos, la topología y los eventos de caída detectados en la red.

## Aplicaciones

- **Identificación de equipos en reportes de incidentes**: en el reporte de caída del AP parquesanrafael1 se registra la dirección `2C AC 5C 9C B0` para individualizar el dispositivo afectado.
- **Diagnóstico de conectividad en switches de acceso**: en el diagnóstico del switch `sw2cc4ttgye.telconet.net` el puerto `Fa0/11` "no aprende MAC", lo que indica un problema de aprendizaje de direcciones en la tabla del switch y constituye evidencia técnica de un enlace caído.
- **Monitorización de la red inalámbrica y de acceso**: el seguimiento de las direcciones MAC permite detectar desconexiones, validar la presencia de dispositivos y localizar la ubicación física de una falla.
- **Trazabilidad y auditoría**: permiten vincular un evento de red con el equipo concreto que lo originó.

## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[concepts/enlace-wifi|Enlace WIFI]]
- [[concepts/monitorización-proactiva|Monitorización proactiva]]
- [[concepts/login|Login]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]

## Menciones en la fuente

- "Mediante monitoreo proactivo se observa la caida del enlace AP Login: 	tn_wifi2_parquesanrafael1 con MAC 2C AC 5C 9C B0 is DOWN en la controladora HW  https://157.100.14.130/" — [[Work/3. Corporativos|3. Corporativos]]
- "Se envia vía mail la notificación. UM:sw2cc4ttgye.telconet.net Fa0/11 no aprende MAC" — [[Work/3. Corporativos|3. Corporativos]]