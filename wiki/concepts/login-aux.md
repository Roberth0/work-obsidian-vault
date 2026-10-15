---
type: concept
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
  - "term"
aliases:
  - "login auxiliar"
  - "login_aux"
  - "login del enlace auxiliar"
---

# login aux

## Definición

El **login aux** es el identificador del enlace auxiliar de un cliente que se asocia a cada tarea de Troubleshooting proactivo generada desde Zabbix en la plataforma Telcos. Funciona como la clave de correlación entre el evento de monitoreo y el cliente afectado: aparece como parámetro dentro de las peticiones a `reasignarTarea` y su valor se menciona explícitamente en el campo `motivo` para describir el contexto del enlace caído.

El **Login Auxiliar** es también la credencial secundaria o de apoyo que se utiliza como identificador al dar de alta los puntos de acceso (AP) en la infraestructura del cliente Telcograph, funcionando como nexo entre la identificación del cliente y la del dispositivo dentro de la controladora.
## Características clave

- **Identificador de enlace auxiliar de cliente**: no identifica la tarea, sino el enlace del cliente sobre el que se generó el evento de monitoreo.
- **Parámetro de la petición `reasignarTarea`**: se envía junto con otros datos de la tarea bajo la forma `login=<valor>`, por ejemplo `login=happy-comitepueblo2` o `login=coopjep-atm-sanfernando`.
- **Se acompaña de otros datos técnicos**: habitualmente va junto con la IP del enlace y la unidad de monitoreo (UM).
- **Clave de correlación**: su valor se cita dentro del campo `motivo`, lo que permite vincular el evento de Zabbix con el cliente y el enlace concretos.
- **Se distingue de los identificadores de la tarea**: es un campo diferente de [[nombre_tarea]] y [[numero_tarea]], que identifican la tarea misma y no el enlace afectado.
- **Formato variable**: el valor combina el nombre del cliente o cooperativa con la designación del enlace (por ejemplo, terminaciones con número o con sufijo tipo `-atm-<localidad>`).
- **Dato obligatorio en el ingreso de APs**: en el procedimiento de ingreso de APs (hasta 5), el Login Auxiliar es uno de los datos que se deben proporcionar, junto con el AP, el Nombre en la controladora, la MAC y la IP Controladora.
- **Regla de formato según controladora**: si la controladora es RUCKUS, debe agregarse «6.» delante del valor correspondiente al ingreso del AP.
## Aplicaciones

- **Automatización de tareas de Troubleshooting proactivo**: permite crear y reasignar tareas desde Zabbix asociándolas al enlace correcto del cliente.
- **Construcción de peticiones a `reasignarTarea`**: es uno de los parámetros requeridos para que la plataforma Telcos identifique el objeto de la tarea.
- **Trazabilidad y diagnóstico**: al figurar en el campo `motivo` junto a la IP y la UM, facilita reconstruir el contexto de una caída o degradación del enlace.
- **Correlación entre monitoreo y cliente**: sirve de puente entre el evento disparado en Zabbix y el registro del cliente en telconet.
- **Configuración del hostname del dispositivo**: el escenario de nombrado utiliza el formato 'login/mac' («Cambiar hostname a: login/mac»), empleando el Login Auxiliar como identificador del equipo.
- **Procedimiento de inventario**: en la sección inventory se debe modificar el campo 'Host Router' asignándole el valor del Login Auxiliar, y el campo 'Name' con el valor 'Login'.
## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/id_detalle|id_detalle]]
- [[concepts/motivo|motivo]]
- [[concepts/numero_tarea|numero_tarea]]
- [[concepts/puerto-connected-no-aprende-mac|Puerto connected, no aprende MAC]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/telconet|telconet]]
- [[entities/zabbix|Zabbix]]

## Menciones en la fuente

- "id_detalle=49413265&id_tarea=4023&motivo=Mediante monitoreo se verifica enlace caído, asociado al login aux: happy-comitepueblo2_2 con IP: 10.221.135.174." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "login=happy-comitepueblo2&fecha_ejecucion=2024-10-18T00:00&hora_ejecucion=2024-10-18T01:00&intIdDetalleHist=123852026" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "Datos que se deben proporcionar" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Cambiar hostname a: login/mac" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Host Router: Login Auxiliar" — [[Work/4.1 Telcograph|4.1 Telcograph]]