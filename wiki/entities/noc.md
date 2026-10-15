---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
type_confirmed: true
sources:
  - "[[sources/0-1-correos-y-claves_b0e46c]]"
  - "[[sources/3-corporativos_04d2e4]]"
tags:
  - "organization"
aliases:
  - "Network Operations Center"
  - "Centro de Operaciones de Red"
  - "NOC (Network Operations Center)"
---

# NOC

## Definición

El NOC (Network Operations Center, o Centro de Operaciones de Red) es el centro de operaciones encargado de la supervisión, el monitoreo y la gestión de incidencias de una infraestructura de red. Constituye el punto central de coordinación operativa entre [[Telconet]] y sus contrapartes externas, y actúa como destinatario formal de las comunicaciones de incidencia y como entidad con contacto telefónico propio.

El NOC es el área interna de [[Telconet]] encargada de la gestión y el monitoreo de la red, lo que amplía su rol coordinador con una función operativa directa sobre la infraestructura.
## Características clave

- **Función de supervisión y monitoreo**: agrupa las tareas de vigilancia continua del estado de la infraestructura de red.
- **Gestión de incidencias**: es el destinatario designado de los correos de notificación de incidencias.
- **Canal de contacto propio**: cuenta con un número telefónico de contacto directo asignado (Contacto NOC: 0999997036).
- **Punto de coordinación externa**: sirve de enlace operativo entre la organización y terceros, como el [[Peering|peering]] con otras redes.
- **Rol operativo aglutinante**: concentra y articula el conjunto de herramientas de monitoreo documentadas.
- **Destinatario en esquemas de escalamiento**: en escenarios con [[Cloudflare]], las incidencias deben notificarse simultáneamente al NOC y al EPP.
- **Canal de contacto por correo**: dispone de la dirección de correo directa "noc" <noc@telconet.ec>, complementando el canal telefónico ya documentado.
- **Credenciales de acceso propias**: cuenta con credenciales de usuario `noc` (noc@telconet.ec con contraseña 4buR*k9&-5A2) para el acceso a plataformas de administración como https://telconet.msp.ruckus.cloud/auth.
- **Rol operativo NOC-RADIO**: el grupo NOC-RADIO se encarga de las revisiones de APs de los nodos WiFi ("Notificar chat: ***NOC-RADIO Revisiones APS Nodos WIFI***").
- **Plataformas de monitoreo empleadas**: utiliza herramientas como Zabbix y Telcograf para el seguimiento de enlaces y APs.
## Aplicaciones

- **Notificación de incidencias**: envío de correos de incidencia al NOC como destinatario establecido en los procedimientos operativos.
- **Escalamiento conjunto con terceros**: en el contexto de Cloudflare, la notificación de incidencias se dirige al NOC y al EPP de forma paralela.
- **Contacto telefónico directo**: uso del número de contacto del NOC para la coordinación y el seguimiento de problemas operativos.
- **Monitoreo de interconexiones**: seguimiento del estado de los enlaces de [[Peering|peering]] entre redes.
- **Coordinación con proveedores y contrapartes**: gestión de la comunicación técnica con organizaciones externas como [[Cloudflare]] y [[Telconet]].
- **Gestión de logins tn_wifi2_**: administración de los logins con prefijo `tn_wifi2_...` correspondientes a los nodos de Guayaquil y Quito incluidos en el listado de Telcograf.
- **Destinatario en copia (Cc)**: inclusión del NOC en copia en los correos dirigidos a contacto técnico, junto con soporte e ipccl2.
## Conceptos relacionados

- [[concepts/peering|Peering]]

## Entidades relacionadas

- [[entities/cloudflare|Cloudflare]]
- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "Incidencias enviar correo a NOC y EPP" (Incidencias enviar correo a NOC y EPP) — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Contacto NOC : `0999997036`" (Contacto NOC : `0999997036`) — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- ""CloudFlare NOC" <noc@cloudflare.com>;" ("CloudFlare NOC" <noc@cloudflare.com>;) — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Gestiona NOC MIMG logins con tn_wifi2_.... que sean de guayaquil y de quito los que esten en el siguiente listado del [Telcograf](https://telcograf.telconet.ec/pM5jDZYe9Ws4JI=/d/9OHSQ8Mint4/2-1-access-point?orgId=267&var-grupo=MUNICIPIO_DEL_DISTRITO_METROPOLITANO_DE_QUITO&var-host=tn_wifi2_parpomasquimirador)" — [[Work/3. Corporativos|3. Corporativos]]
- ""soporte" <soporte@telconet.ec>; "noc" <noc@telconet.ec>; "ipcc l2" <ipcc_l2@telconet.ec>" — [[Work/3. Corporativos|3. Corporativos]]