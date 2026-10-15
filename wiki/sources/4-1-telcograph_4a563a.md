---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/4.1 Telcograph.md]]"
tags:
  - cedia
aliases:
  - Telcograph 4.1
  - Procedimiento Telcograph (Unión de Razones Sociales y Ingresos de APs)
sources:
  - "[[entities/telcograph]]"
  - "[[entities/ruckus]]"
  - "[[sources/access-point]]"
  - "[[entities/informacion-recibida-de-sistemas]]"
  - "[[concepts/union-de-razones-sociales]]"
  - "[[concepts/ingresos-de-aps]]"
  - "[[concepts/macros]]"
  - "[[concepts/controladora]]"
  - "[[concepts/login-aux]]"
  - "[[concepts/ip-de-ingreso]]"
  - "[[concepts/inventario-del-zabbix]]"
  - "[[concepts/hostname]]"
contentHash: 3aa-075430f0
generation_complete: true
---

# 4.1 Telcograph - Resumen

## Fuente

- Archivo original: [[Work/4.1 Telcograph.md]]
- Ingerido: 2026-09-23

## Contenido principal

Este documento recoge procedimientos operativos internos para la gestión del cliente [[entities/telcograph|Telcograph]], vinculado con Cedia a través de los enlaces de la nota. El escrito se abre con una advertencia: cuando el cliente supera las 500M se debe cambiar de plantilla. El contenido se organiza en dos bloques. El primero, la [[concepts/union-de-razones-sociales|Unión de Razones Sociales]], detalla tareas ya completadas: cancelar los puntos de la razón social antigua en [[entities/informacion-recibida-de-sistemas|Información recibida de sistemas]], actualizar los datos de SERVER IP, Name ZG ORG e ID Grafana en *Razones sociales*, y crear los nuevos puntos con los cambios aplicados. El segundo, los [[concepts/ingresos-de-aps|Ingresos de APs]], describe el alta de hasta cinco puntos de acceso con la [[concepts/ip-de-ingreso|IP de Ingreso]] 172.24.27.27, el cambio de [[concepts/hostname|hostname]] al formato login/mac, la actualización de [[concepts/macros|MACROS]] —agregando «6.» adelante si la [[concepts/controladora|controladora]] es [[entities/ruckus|RUCKUS]]— y la modificación de la sección [[concepts/inventario-del-zabbix|inventory]].

## Entidades clave

- [[entities/telcograph|Telcograph]] — cliente al que se refiere el documento, cuyo volumen supera las 500M.
- [[entities/ruckus|RUCKUS]] — marca de controladora que activa la regla de agregar «6.» en las MACROS.
- [[access-point|AP]] — punto de acceso que se ingresa (hasta 5) en la infraestructura del cliente.
- [[entities/informacion-recibida-de-sistemas|Información recibida de sistemas]] — sección donde se cancelan y crean los puntos de configuración.

## Conceptos clave

- [[concepts/union-de-razones-sociales|Unión de Razones Sociales]] — procedimiento de migración/unificación de datos entre sistemas internos.
- [[concepts/ingresos-de-aps|Ingresos de APs]] — flujo estructurado para registrar puntos de acceso.
- [[concepts/macros|MACROS]] — variables de configuración que se actualizan durante el alta del AP.
- [[concepts/controladora|Controladora]] — sistema que gestiona centralmente los puntos de acceso.
- [[concepts/login-aux|Login Auxiliar]] — credencial secundaria usada como identificador del dispositivo.
- [[concepts/ip-de-ingreso|IP de Ingreso]] — dirección de acceso (172.24.27.27) para provisionar los APs.
- [[concepts/inventario-del-zabbix|Inventory]] — sección donde se modifican Host Router y Name.
- [[concepts/hostname|Hostname]] — nombre del dispositivo, definido en formato login/mac.

## Puntos principales

- Cuando el cliente supera las 500M se debe cambiar de plantilla, según la advertencia inicial del documento.
- La **Unión de Razones Sociales** implica cancelar los puntos de la razón social antigua, cambiar SERVER IP, Name ZG ORG e ID Grafana en *Razones sociales*, y crear los nuevos puntos en *Información recibida de sistemas*.
- El **ingreso de APs** admite hasta 5 dispositivos y requiere la IP de ingreso **172.24.27.27**.
- Cada AP requiere los datos: AP, Login Auxiliar, Nombre en la controladora, MAC e IP Controladora.
- El **hostname** del AP debe cambiarse al formato **login/mac**.
- Al actualizar las **MACROS**, si la controladora es **RUCKUS** se debe agregar «6.» adelante.
- En la sección **inventory** se debe modificar el Host Router (Login Auxiliar) y el Name (Login).

## Menciones en la fuente

- ">[!warning] Cliente supera las 500M, se debe cambiar de plantilla a" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "### Union de Razones Sociales" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "links:
  - "[[4 Cedia]]"" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "tags:
  - cedia" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Actualizar MACROS, si la controladora es **RUCKUS** agregar *6.* adelante" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Cambiar datos de SERVER IP, Name ZG ORG e ID Grafana en *Razones sociales*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "### Ingresos de APs (Hasta 5)" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [ ] AP
- [ ] Login Auxiliar
- [ ] Nombre en la controladora
- [ ] MAC 
- [ ] IP Controladora" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Cancelar puntos de la razon social antigua en *Informacion recibida de sistemas*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Crear los puntos con los nuevos cambios en *Informacion recibida de sistemas*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "En la seccion inventory modificar" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Host Router: Login Auxiliar" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [x] Cancelar puntos de la razon social antigua en *Informacion recibida de sistemas*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [x] Cambiar datos de SERVER IP, Name ZG ORG e ID Grafana en *Razones sociales*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "### Ingresos de APs (Hasta 5) 

Datos requeridos

IP de Ingreso : *172.24.27.27*" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Cambiar hostname a: login/mac" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Verificar el grupo al cual se asigna" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [ ] Nombre en la controladora
- [ ] MAC 
- [ ] IP Controladora" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Datos que se deben proporcionar" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [ ] MAC" — [[Work/4.1 Telcograph|4.1 Telcograph]]