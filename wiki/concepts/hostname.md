---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
aliases:
  - "Nombre de host"
  - "Host name"
generation_complete: true
---

# Hostname

## Definición

Un **hostname** (nombre de host) es el nombre asignado a un dispositivo dentro de una red, que lo identifica de forma única dentro de la infraestructura. A diferencia de la dirección MAC o la dirección IP, el hostname es un identificador legible para las personas, configurable por el administrador, y se utiliza para reconocer y gestionar cada equipo en los sistemas de monitoreo y aprovisionamiento.

## Características clave

- Identificador lógico y legible de un dispositivo dentro de una red; es independiente de su dirección física ([[MAC]]) y puede modificarse sin alterar el hardware.
- Es configurable por el administrador, por lo que su valor depende de las convenciones de nomenclatura definidas en cada despliegue.
- En el procedimiento de ingreso de APs del cliente [[Telcograph]], debe adoptar el formato `login/mac`, es decir, la combinación del [[Login Auxiliar]] y la dirección [[MAC]] del dispositivo.
- La convención `login/mac` permite identificar rápidamente cada punto de acceso y asociarlo con el cliente correspondiente.
- Se corresponde con el campo *Name* que se modifica en la sección [[Inventory]] de la plataforma de gestión.

## Aplicaciones

- **Aprovisionamiento de puntos de acceso:** durante el ingreso de un [[AP]] a la infraestructura, el hostname se renombra siguiendo el formato `login/mac` antes de completar el registro.
- **Identificación y soporte operativo:** un hostname descriptivo permite localizar un equipo específico en la plataforma sin necesidad de consultar su dirección MAC.
- **Trazabilidad por cliente:** al incorporar el Login Auxiliar, el nombre del dispositivo queda vinculado de forma explícita al cliente al que pertenece el equipo.
- **Inventario y gestión:** el hostname es el valor que se registra y actualiza en el campo *Name* de la sección [[Inventory]], lo que mantiene sincronizados el nombre del dispositivo y su registro administrativo.

## Conceptos relacionados

- [[concepts/login-aux|Login Auxiliar]]
- [[concepts/mac|mac]]
- [[concepts/inventario-del-zabbix|Inventory]]

## Entidades relacionadas

- [[entities/access-point|AP]]

## Menciones en la fuente

- "Cambiar hostname a: login/mac" — [[Work/4.1 Telcograph|4.1 Telcograph]]