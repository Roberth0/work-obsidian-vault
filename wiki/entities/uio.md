---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/0-directorio-telefonico_b3619c]]"
  - "[[sources/1-backbone_5939cb]]"
  - "[[sources/2-vips_147ea4]]"
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/4-cedia_d7cef1]]"
tags:
  - "place"
aliases:
  - "Quito"
  - "UIO (Quito)"
  - "Aeropuerto de Quito"
---

# UIO

## Descripción

UIO es el código IATA del aeropuerto de Quito y, en el directorio telefónico, funciona como abreviatura operativa para referirse a las instalaciones y contactos ubicados en esa ciudad. En la sección eléctrica, el documento indica que para UIO se debe "Revisar Personal de Turno en correo" en lugar de proporcionar un número telefónico directo, lo que la distingue de otras sedes del listado como [[GYE]]. UIO alberga además un [[Datacenter BOC]], que cuenta con contactos propios de [[Manos Remotas]] (0986576746) y de monitoreo (0998416095). Para el trámite de [[Escalamiento Permisos ingreso Cirion]] debe enviarse correo a DocQuito, contacto asociado al DC UIO. De este modo, UIO concentra varios de los contactos operativos clave del documento, incluida la relación con [[Cirion]].

En el contexto del NOC de Telconet, UIO funciona como una de las dos jurisdicciones principales junto con [[GYE]]. Para UIO o GYE, cuando no hay respuesta ICMP se debe escalar a OPU (y si no hay respuesta SSH, se escala la tarea a NW). La tarea L3 UIO se realiza seleccionando `Jurisdiccion UIO`, `Tipo Todas` y `Reporte L3`; si algún elemento aparece en modo routed se debe validar en el equipo y, de ser el caso, enviar tarea a NW. UIO cuenta además con el responsable de `GEPON TAP: Juan Carlos Chavez Alarcon`, y con credenciales de acceso a equipos como `ssh -l noc-operator fwhdcuio1` (Hillstone).

El monitoreo de VIPS se realiza 24/7 y UIO es uno de sus tres servidores Zabbix, accesible en https://172.24.27.13/zabbix/, lo que añade a UIO un rol nuevo como servidor de monitoreo de VIPS. Asimismo, la sigla UIO corresponde al código del Aeropuerto Internacional Mariscal Sucre de Quito, lo que vincula este servidor de monitoreo a una ubicación geográfica concreta.

En el [[NOC MIMG]], UIO adquiere un rol adicional como ciudad de referencia para la gestión de logins WiFi, ya que deben gestionarse los accesos con formato `tn_wifi2_....` que sean de Guayaquil y de Quito según el listado del [Telcograf], junto con [[GYE]].

UIO también figura como contexto del cliente `danec-uio-eduardoberg`, con la tarea 101743384 aperturada desde el 2024-04-18 y validada como caída, lo que amplía su papel operativo como identificador de ciudad en tareas de clientes corporativos gestionadas por el NOC de radio.
## Entidades relacionadas

- [[entities/gye|GYE]]
- [[entities/datacenter-boc|Datacenter BOC]]
- [[entities/cirion|Cirion]]
- [[entities/mimg|MIMG]]
- [[entities/radio-uio|RADIO UIO]]

## Conceptos relacionados

- [[concepts/escalamiento-permisos-ingreso-cirion|Escalamiento Permisos ingreso Cirion]]
- [[concepts/manos-remotas|Manos Remotas]]

## Menciones en la fuente

- "UIO - Revisar Personal de Turno en correo" — [[Work/0. Directorio Telefonico|0. Directorio Telefonico]]
- "Manos remotas Datacenter UIO  `0986576746`
Monitoreo Boc UIO `0998416095`" — [[Work/0. Directorio Telefonico|0. Directorio Telefonico]]
- "Se debe enviar un correo a DC UIO DocQuito@ciriontechnologies.com;  con el formulario y el listado de personal a asistir" — [[Work/0. Directorio Telefonico|0. Directorio Telefonico]]