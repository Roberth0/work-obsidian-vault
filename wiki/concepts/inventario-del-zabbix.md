---
type: concept
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
  - "term"
aliases:
  - "Inventario de Zabbix"
  - "OpciónInventario de Zabbix"
  - "Zabbix Inventory"
  - "Inventory"
---

# Inventario del zabbix

## Definición

El **Inventario del zabbix** es la opción de la plataforma [[Zabbix]] que se utiliza en el documento para obtener la dirección IP de una cámara antes de diagnosticarla. Corresponde a la consulta del inventario de activos monitoreados, cuyo propósito en este procedimiento es identificar la dirección contra la cual se dirigirá un ping de verificación.

La sección inventory también funciona como el repositorio central de identificadores de los dispositivos dentro de la infraestructura del cliente Telcograph, donde se registran y modifican los datos asociados a los dispositivos de red, como el Host Router y el Name de cada punto de acceso, ampliando así su definición más allá del uso puntual de consulta de IP en [[Zabbix]].
## Características clave

- Es una opción de consulta dentro de [[Zabbix]], no una herramienta de diagnóstico por sí misma.
- Devuelve datos de identificación del activo, en particular la dirección IP de la cámara.
- Actúa como paso previo y habilitante: sin la IP obtenida no es posible dirigir el ping hacia la cámara.
- Vincula la información de inventario de activos con la verificación de conectividad de red.
- Se emplea en conjunto con la pestaña **lógico** de la OLT, donde se ejecuta el ping.
- Su resultado condiciona la interpretación posterior: si no hay respuesta, se registra [[Sin respuesta ICMP]] y eventualmente [[Caida de camara/s]].
- La correcta actualización de la sección inventory es clave para mantener la coherencia entre los datos de la controladora y los del inventario.
## Aplicaciones

- **Diagnóstico de cámaras:** obtener la IP de una cámara específica antes de ejecutar pruebas de conectividad.
- **Verificación de conectividad ICMP:** determinar la dirección destino del ping realizado desde la pestaña *lógico* de la OLT.
- **Correlación de inventario y fallas:** vincular el registro de activos con los incidentes de red detectados, como la caída de una cámara.
- **Flujo operativo de soporte:** secuencia estándar en la que primero se verifica el estado de la OLT, luego se consulta el inventario en [[Zabbix]], y finalmente se prueba la respuesta del dispositivo.
- **Ingreso de APs (Host Router):** en la sección *inventory* se debe modificar el campo Host Router, asignándole el Login Auxiliar del punto de acceso.
- **Ingreso de APs (Name):** en la sección *inventory* también se debe modificar el campo Name, asignándole el Login del dispositivo.
## Conceptos relacionados

- [[concepts/sin-respuesta-icmp|Sin respuesta ICMP]]
- [[concepts/caida-de-camaras|Caida de camara/s]]

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/camaras|Camaras]]

## Menciones en la fuente

- "Posteriormente en la pestaña *logico* se debe hacer ping hacia la camara, para ello se debe conocer su IP mediante la opcion inventario del zabbix" — [[Work/2.1 CSCG|2.1 CSCG]]
- "En la seccion inventory modificar" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [ ] Host Router: Login Auxiliar" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [ ] Name: Login" — [[Work/4.1 Telcograph|4.1 Telcograph]]