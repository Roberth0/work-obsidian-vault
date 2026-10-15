---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "IP de ingreso"
  - "IP de entrada"
  - "Ingress IP"
generation_complete: true
---

# IP de Ingreso

## Definición

La **IP de Ingreso** es la dirección IP que funciona como punto de entrada para acceder a los puntos de acceso (AP) de la infraestructura del cliente [[Telcograph]]. En el procedimiento documentado se establece que su valor es `172.24.27.27`, dato exigido para iniciar el alta de hasta cinco APs en el sistema.

Se trata de la dirección sobre la cual el equipo técnico establece la conexión inicial que habilita las tareas posteriores de configuración; sin ella no es posible alcanzar los dispositivos ni provisionarlos.

## Características clave

- **Valor específico y único**: en el documento se fija como `172.24.27.27`, por lo que no es un rango ni una dirección genérica, sino un destino concreto de conexión.
- **Dirección de tipo privado**: pertenece al bloque `172.16.0.0/12` (RFC 1918), lo que indica un direccionamiento interno de la red del cliente.
- **Punto de entrada obligatorio**: constituye el canal de acceso a la infraestructura sobre la que se realizan las configuraciones.
- **Dato habilitante del alta**: su conocimiento es requisito previo para dar de alta hasta cinco APs.
- **Naturaleza operativa**: no es un parámetro configurable del AP, sino un dato de acceso que maneja el equipo técnico.
- **Uso transitorio en el flujo de trabajo**: se emplea durante la fase de conexión y provisión, antes de la configuración de los parámetros del dispositivo.

## Aplicaciones

- **Alta de puntos de acceso**: se utiliza como destino de conexión para iniciar el procedimiento de registro de hasta cinco APs en el sistema del cliente.
- **Acceso a la controladora**: sirve como vía de entrada hacia la [[Controladora]], donde posteriormente se configuran el login, la dirección MAC y el nombre de cada dispositivo.
- **Provisión de dispositivos**: permite al equipo técnico conectarse a los equipos antes de aplicarles la configuración definitiva.
- **Verificación de conectividad**: funciona como referencia para comprobar que existe comunicación con la infraestructura del cliente antes de comenzar las tareas de configuración.
- **Documentación de instalación**: se registra como dato fijo del procedimiento, de modo que cualquier técnico pueda reproducir el acceso sin depender de información adicional.

## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[concepts/login-aux|Login Auxiliar]]
- [[concepts/mac|mac]]
- [[concepts/inventario-del-zabbix|Inventory]]

## Entidades relacionadas

- [[entities/access-point|AP]]
- [[entities/telcograph|Telcograph]]

## Menciones en la fuente

- "IP de Ingreso : *172.24.27.27*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Datos requeridos" — [[Work/4.1 Telcograph|4.1 Telcograph]]