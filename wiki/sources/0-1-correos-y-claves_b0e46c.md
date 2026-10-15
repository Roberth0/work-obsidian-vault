---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/0.1 Correos y Claves.md]]"
tags: [other]
aliases: ["Correos y Claves", "Credenciales y Contactos NOC Telconet"]
contentHash: a06-30d1381a
generation_complete: true
---

# 0.1 Correos y Claves - Resumen

## Fuente

- Archivo original: [[Work/0.1 Correos y Claves.md]]
- Ingerido: 2026-09-23

## Contenido principal

Este documento es una nota operativa interna de [[entities/telconet|Telconet]] que recopila correos electrónicos, credenciales de acceso y contactos de escalamiento utilizados por el equipo de [[noc|NOC]] y áreas afines. Contiene usuarios y contraseñas para herramientas de monitoreo y gestión como eSyslog, PacketLight, Zabbix, TeliGraph, Kentik, QlikSense y Fiberhome, así como para portales de terceros como Cirion y UFINET. Además, describe la estructura de [[concepts/jefaturas|jefaturas]] organizadas por área y ciudad (OTN, IPCCL1/2, REDESLAN, AI, BOC, Infraestructura, CERT, Monitoreo Sistemas) en Quito (UIO) y Guayaquil (GYE), con los nombres de los responsables. También incluye contactos corporativos de proveedores y clientes como [[entities/cloudflare|Cloudflare]], Meta/Facebook, Amazon, Telia, Telxius, CSD Movistar, El Rosado, Disney, IBM y Kyndryl. Por su naturaleza, es una fuente de [[entities/0-1-correos-y-claves|credenciales de acceso]] y contactos que debe tratarse como información altamente sensible.

## Entidades clave

- [[entities/telconet|Telconet]] — empresa de telecomunicaciones ecuatoriana y contexto organizativo central de la nota; su dominio `telconet.ec` aparece como usuario en portales de terceros.
- [[entities/cloudflare|Cloudflare]] — proveedor de infraestructura de red, CDN y seguridad con una sección propia dedicada al escalamiento de incidencias vía NOC y EPP.
- [[entities/0-1-correos-y-claves|0-1-correos-y-claves]] — la propia nota operativa, registrada como entidad documental.

## Conceptos clave

- [[concepts/jefaturas|Jefaturas]] — estructura organizativa de Telconet que agrupa las áreas operativas bajo responsables designados, segmentadas por especialidad y ciudad (UIO/GYE).
- [[entities/0-1-correos-y-claves|Credenciales de acceso]] — inventario de usuarios y contraseñas para herramientas de monitoreo, portales de terceros y equipos de red.
- [[noc|NOC]] — Centro de Operaciones de Red, punto central de coordinación entre Telconet y sus contrapartes externas.

## Puntos principales

- La nota recopila **credenciales de acceso** (usuarios y contraseñas) para herramientas de monitoreo y portales de terceros usados por el NOC de Telconet.
- Se documentan accesos a herramientas como **eSyslog, PacketLight, Zabbix, TeliGraph Clientes, Kentik, Fiberhome y QlikSense**, así como a los portales de **Cirion y UFINET**.
- La estructura organizativa se describe mediante **jefaturas por área y ciudad** (OTN, IPCCL1/2, REDESLAN, AI, BOC, Infraestructura, CERT, Monitoreo Sistemas) en Quito (UIO) y Guayaquil (GYE).
- **Cloudflare** cuenta con una sección dedicada que indica enviar incidencias a NOC y EPP, con múltiples direcciones de contacto (`noc@`, `epp@`, `dcops@`, `noc-notify@`).
- Se listan **contactos corporativos** de proveedores y clientes como Meta/Facebook, Amazon, Telia, Telxius, CSD Movistar, El Rosado, Disney, IBM y Kyndryl para escalamiento.
- El documento contiene **información sensible** (contraseñas en texto plano) que requiere manejo seguro y controlado.
- Se registran contactos de personas específicas como Marcelo Lomas (Soporte de Software), el NOC de CSD Movistar (`0999997036`) y números de infraestructura UIO.

## Menciones en la fuente

- "Cirion User: `noc@telconet.ec`Password: `Cirion2025@telco`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Portal UFINET: `noc@telconet.ec`Password: `Noctelconet123`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Kentik: `noc@telconet.ec` password: `N0CT31con3t2025@`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Fiberhome
User: `TELCONET\nocgye` 
Pass: `Noctelco2025`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "### Cloudflare
Incidencias enviar correo a NOC y EPP" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- ""CloudFlare NOC" <noc@cloudflare.com>;" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- ""Edge Partner Program" <epp@cloudflare.com>;" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- ""Data Center Operations" <dcops@cloudflare.com>;" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Zabbix Telcograph User: `Zabbix_Admin`Password: `Z@bbix_@dm1n_2018**`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Zabbix SSH User: `root`Password: `fJNu$gRHTg!w21`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- ""stalynrojas" <stalynrojas@fiberhome.com>;" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "QlinkSense
usuario:   `qlik0\jmarchan`
pass:       `gJKKjBzWnJijF05Tpp0V`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Telcograph Clientes User: `noc`Password: `VCzrk"kUr3xMH~E6`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "eSyslog User: `noc`Password: `VCzrk"kUr3xMH~E6`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "PacketLigh User: `PACKETLIGHT\nocgye`  Password: `nocgye2020`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "Linphone/zoiper extension password: `TNlAtam#2o2!`" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "### Meta / Facebook" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]
- "![[Pasted image 20241108192616.png]]" — [[Work/0.1 Correos y Claves|0.1 Correos y Claves]]