---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/0-1-correos-y-claves_b0e46c]]"
  - "[[sources/1-backbone_5939cb]]"
  - "[[sources/1-2-backbone-proveedores-internacionales_861235]]"
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
  - "[[sources/2-vips_147ea4]]"
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/4-cedia_d7cef1]]"
  - "[[sources/comandos_d202a8]]"
tags:
  - "organization"
aliases:
  - "Telconet S.A."
  - "Telconet.ec"
  - "noc@telconet.ec"
---

# Telconet

## Descripción

Telconet es la empresa ecuatoriana de telecomunicaciones que opera como red de transporte y acceso en el país, y constituye el contexto organizativo central de la documentación operativa recogida en [[0-1-correos-y-claves|0-1-correos-y-claves]] y [[1-backbone|1. Backbone]]. Su dominio `telconet.ec` aparece repetidamente como nombre de usuario de acceso a portales de terceros —entre ellos [[Cirion]], [[UFINET]] y [[Kentik]]—, lo que refleja su condición de operador de red con múltiples relaciones con proveedores de capacidad, tránsito y visibilidad. La cuenta `noc@telconet.ec` es el punto de contacto operativo usado para reportar y gestionar incidencias en varios de los procedimientos documentados, incluido el nuevo portal de generación de incidencias de UFINET.

La estructura interna de la compañía se organiza en jefaturas —OTN, IPCCL, REDESLAN, BOC y CERT, entre otras— distribuidas entre sus dos sedes principales: Quito (UIO) y Guayaquil (GYE). El equipo de NOC es el principal usuario de las credenciales documentadas, y se encarga del monitoreo, la atención y el escalamiento de incidencias hacia las jefaturas correspondientes. Telconet opera el [[Backbone|Backbone]] monitoreado por ese NOC y sostiene su operación sobre infraestructura de acceso remoto y VPN propia, identificada por el dominio `vpn0.telconet.ec` y el usuario `ipccl2-gye1`.

En el plano de la operación diaria, la compañía gestiona chats internos de coordinación como Backbone Nacional y NOC-IPCCL1-Backbone, y mantiene relaciones de peering e interconexión con operadores como [[UFINET]], [[TIGO]] y [[Fastly]]. Telconet se relaciona directamente con todos los contactos de proveedores listados en las notas como parte de su ecosistema operativo, y mantiene servicios apoyados en infraestructuras externas como [[Cloudflare]]. La gestión de sus accesos y de su estructura de escalamiento depende de las [[Jefaturas]] internas y del inventario de [[Credenciales de acceso]] asociado a cada portal.

En su operación del backbone internacional, Telconet gestiona la herramienta de monitoreo NetFlow de salidas internacionales, accesible en https://aplicaciones.telconet.ec/netflow/salidasInternacionales, desde donde se revisa el estado de los enlaces internacionales. Entre sus proveedores de capacidad internacional se encuentra [[Arelion]], cuyo portal (https://www.arelion.com/portal/) se accede con el usuario `noc@telconet.ec`. En el escalamiento de circuitos [[CNT]] se debe generar un caso técnico sobre el login que corresponda según el ID de circuito de TELCONET; para el login `cnt-inaquito-bogota`, CNT reporta los IDs de Telconet mientras que Telconet reporta los CID C&W (Cables and Wireless). Para reportes de nodos de las regiones CDN de [[Akamai]] en Telconet, la lista de contacto es `nocc-shift@akamai.com`, incluyendo en copia a `mmuniz@akamai.com`.

Telconet S.A. es además el emisor de las notificaciones de pérdida de monitoreo, que encabeza con el formato "PERDIDA DE MONITOREO: TELCONET S.A." seguido del login afectado (p. ej. `tn_wifi2_parquesanrafael1`). En esta línea de servicio, la compañía gestiona controladoras WiFi de clientes corporativos y municipales, con logins del tipo `tn_wifi2_...` en Guayaquil y Quito, incluyendo clientes como Omarsa (Panamá) y el Municipio del Distrito Metropolitano de Quito; para su administración se accede al portal Ruckus MSP (https://telconet.msp.ruckus.cloud/auth) con el correo `noc@telconet.ec`, y se emplean plataformas de monitoreo como Telcograf (https://telcograf.telconet.ec) y Zabbix.

Telconet opera además herramientas internas como Telcos (https://telcos.telconet.ec, 172.24.15.70) y el dashboard de backbone disponible en https://monitoreoda.telconet.ec/zabbix/, y su personal usa el Zabbix de Backbone para el monitoreo. Las direcciones internas de sus servidores documentadas incluyen telcos.telconet.ec 172.24.15.70; telcodrive.telconet.net 172.24.5.141; sisred.telconet.net 172.24.4.63; y admin.cisco.telconet.ec, aaaa.telconet.ec y bitacora.telconet.ec 172.24.4.228. Por otro lado, rca-uio.telconet.ec 172.24.26.15 y backbonenoc.telconet.ec 172.24.5.126 aparecen marcados como 'NO VALE', y se listan rutas de red ADD/DELETE necesarias para acceder a los recursos. Entre sus credenciales de acceso figuran las credenciales NOKIA asociadas a Telconet, con USER `SoporteTelconet` y PASS `C3d1@Tn$$N0k!@25`, que complementan las cuentas ya listadas (`noc@telconet.ec`, `soporte@telconet.ec`, `ipcc_l2@telconet.ec`).

Sus equipos de soporte se organizan en niveles (N1/L1), en el NOC-RADIO y en grupos de coordinación como 'Estimados Radios GYE' y 'Estimados RADIO UIO'; las tareas se asignan mediante números de tarea (p. ej. tarea 102757614). Además de `noc@telconet.ec`, la compañía usa los correos institucionales `soporte@telconet.ec` e `ipcc_l2@telconet.ec` como contactos de escalamiento y para acceder a plataformas de administración.

Telconet es la empresa propietaria de la infraestructura y de los procesos documentados, y su personal opera el rol asociado al cliente CEDIA; su ecosistema operativo incluye clientes como CEDIA, Nedetel, Xtrim y Claro (antes CNT).

Además de la VPN corporativa identificada por `vpn0.telconet.ec`, el nombre de la compañía da nombre a una vpn-instance configurada en equipamiento Huawei, que actúa como contexto de red sobre el que se ejecutan las tareas de troubleshooting de enrutamiento y BGP. La nota [[Comandos]] parametriza la totalidad de sus comandos con `vpn-instance telconet`, de modo que esa instancia constituye el marco de referencia para la operación y diagnóstico de la red. Sobre esta instancia se consulta tanto su sesión BGP —con el peer 63.222.78.13 mediante el comando `display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose`— como su tabla de enrutamiento con `disp ip routing-table vpn-instance telconet 0.0.0.0 0`.
## Entidades relacionadas

- [[entities/cloudflare|Cloudflare]]
- [[entities/cirion|cirion]]
- [[entities/0-1-correos-y-claves|Credenciales de acceso]]
- [[entities/ufinet|UFINET]]
- [[entities/backbone|Backbone]]
- [[entities/snmp-v3|SNMP v3]]
- [[entities/pruebas-l3|Pruebas L3]]
- [[entities/noc-radio|NOC-RADIO]]
- [[entities/omarsa|Omarsa]]
- [[entities/zabbix|Zabbix]]
- [[entities/telcograf|Telcograf]]
- [[entities/huawei|Huawei]]

## Conceptos relacionados

- [[concepts/jefaturas|Jefaturas]]
- [[concepts/bgp|BGP]]
- [[concepts/vpn-instance|vpn-instance]]

## Nueva información (4 Cedia)

- Telconet opera herramientas internas como Telcos (https://telcos.telconet.ec, 172.24.15.70), Telcograph, Zabbix y el dashboard de backbone disponible en https://monitoreoda.telconet.ec/zabbix/, y su personal usa el Zabbix de Backbone para el monitoreo. (Amplía el inventario de plataformas de monitoreo y administración de Telconet ya mencionado en la página (Telcograf, Zabbix).)
- Direcciones internas de servidores Telconet documentadas: telcos.telconet.ec 172.24.15.70; telcodrive.telconet.net 172.24.5.141; sisred.telconet.net 172.24.4.63; admin.cisco.telconet.ec, aaaa.telconet.ec y bitacora.telconet.ec 172.24.4.228. Además, rca-uio.telconet.ec 172.24.26.15 y backbonenoc.telconet.ec 172.24.5.126 aparecen marcados como 'NO VALE', y se listan rutas de red ADD/DELETE necesarias para acceder a los recursos. (Añade el inventario de hosts y direcciones IP internas de la compañía, datos operativos nuevos no presentes en la página.)
- Credenciales NOKIA asociadas a Telconet: USER `SoporteTelconet` // PASS `C3d1@Tn$$N0k!@25`. (Es una credencial de acceso nueva que complementa las cuentas ya listadas (noc@telconet.ec, soporte@telconet.ec, ipcc_l2@telconet.ec).)

## Menciones en la fuente

- "Cirion User: `noc@telconet.ec`Password: `Cirion2025@telco`" (Usuario de Cirion: `noc@telconet.ec` Contraseña: `Cirion2025@telco`) — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Portal UFINET: `noc@telconet.ec`Password: `Noctelconet123`" (Portal UFINET: `noc@telconet.ec` Contraseña: `Noctelconet123`) — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Correo electrónico:  noc@telconet.ec     
Contraseña: Noctelconet123" — [[Work/1. Backbone|1. Backbone]]
- "- [I] vpn0.telconet.ec" — [[Work/1. Backbone|1. Backbone]]