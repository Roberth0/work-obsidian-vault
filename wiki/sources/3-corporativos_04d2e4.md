---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/3. Corporativos.md]]"
tags:
  - gye
  - aps
  - corporativos
  - controladoras
aliases:
  - Corporativos
  - Controladoras WiFi Corporativas
sources:
  - "[[entities/telconet]]"
  - "[[entities/huawei]]"
  - "[[entities/cisco]]"
  - "[[entities/omarsa]]"
  - "[[entities/meraki]]"
  - "[[sources/noc]]"
  - "[[entities/noc-radio]]"
  - "[[entities/telcograf]]"
  - "[[entities/ipcc]]"
  - "[[entities/gye]]"
  - "[[entities/uio]]"
  - "[[entities/mimg]]"
  - "[[entities/radio-uio]]"
  - "[[entities/ruckus-cloud]]"
  - "[[concepts/controladora]]"
  - "[[sources/access-point]]"
  - "[[concepts/monitorización-proactiva]]"
  - "[[entities/0-1-correos-y-claves]]"
  - "[[concepts/login]]"
  - "[[concepts/tarea]]"
  - "[[concepts/mac]]"
  - "[[concepts/enlace-wifi]]"
  - "[[concepts/wireless-all-aps]]"
contentHash: f3b-ffc8d638
generation_complete: true
---

# 3. Corporativos - Resumen

## Fuente

- Archivo original: [[Work/3. Corporativos.md]]
- Ingerido: 2026-09-23

## Contenido principal

Documento operativo interno de [[entities/telconet|Telconet S.A.]] que recopila [[entities/0-1-correos-y-claves|Credenciales]] de acceso, direcciones IP y enlaces de administración de las [[concepts/controladora|Controladoras]] WiFi de clientes corporativos. Reúne usuarios y contraseñas de fabricantes como [[entities/huawei|Huawei]], [[entities/cisco|Cisco]], [[entities/meraki|Meraki]] y [[entities/ruckus-cloud|Ruckus Cloud]], además de las controladoras de nodos y provincias y la del cliente [[entities/omarsa|Omarsa]] en Panamá. Describe el flujo de soporte mediante [[entities/noc-radio|NOC-RADIO]]: validar los [[access-point|Access Points]] accediendo a la controladora en la sección [[concepts/wireless-all-aps|Wireless / All APs]] y ejecutar la [[concepts/monitorización-proactiva|Monitorización proactiva]] de enlaces caídos. Incluye plantillas de correo para notificar pérdida de monitoreo, listados de hosts de [[entities/mimg|MIMG]], referencias a [[entities/telcograf|Telcograf]] y ejemplos de [[concepts/tarea|Tareas]] de clientes.

## Entidades clave

- [[entities/telconet|Telconet S.A.]] — operador y emisor de las notificaciones de pérdida de monitoreo.
- [[entities/huawei|Huawei]], [[entities/cisco|Cisco]], [[entities/meraki|Meraki]], [[entities/ruckus-cloud|Ruckus Cloud]] — fabricantes y plataformas de controladoras gestionadas.
- [[entities/omarsa|Omarsa]] — cliente corporativo en Panamá con controladora propia.
- [[entities/ipcc|IPCC]] — usuario estándar de acceso a múltiples controladoras.
- [[noc|NOC]], [[entities/noc-radio|NOC-RADIO]], [[entities/mimg|MIMG]], [[entities/radio-uio|RADIO UIO]] — grupos operativos de gestión y campo.
- [[entities/gye|Guayaquil]] y [[entities/uio|Quito]] — zonas geográficas de referencia (GYE / UIO).
- [[entities/telcograf|Telcograf]] — plataforma de visualización para revisar los APs.
- [[entities/3-corporativos|3. Corporativos]] — la fuente misma.

## Conceptos clave

- [[concepts/controladora|Controladora]] — dispositivo o plataforma central que administra los APs.
- [[access-point|Access Point]] — equipo inalámbrico administrado desde la controladora.
- [[concepts/monitorización-proactiva|Monitorización proactiva]] — método de detección temprana de enlaces caídos.
- [[entities/0-1-correos-y-claves|Credenciales]], [[concepts/login|Login]] y [[concepts/tarea|Tarea]] — elementos operativos de acceso y trazabilidad.
- [[concepts/mac|MAC]], [[concepts/enlace-wifi|Enlace WIFI]] y [[concepts/wireless-all-aps|Wireless / All APs]] — datos y rutas técnicas del procedimiento.

## Puntos principales

- Reúne credenciales (usuario/contraseña) para controladoras WiFi de múltiples fabricantes: Ruckus, Huawei, Cisco, Meraki y Ruijie.
- Telconet gestiona controladoras de clientes corporativos y municipales, incluyendo Omarsa (Panamá) y el Municipio del Distrito Metropolitano de Quito.
- Las tareas de soporte se asignan por chat (NOC-RADIO) y correo, con números de tarea (ej. 107963875, 102757614) y seguimiento por niveles N1/L1.
- La validación de APs se realiza accediendo a la controladora (sección Wireless / All APs) tras detectar por monitoreo proactivo enlaces caídos (estado UP/DOWN, MAC).
- Se usan plataformas de monitoreo como Zabbix y Telcograf para revisar los APs y enlaces WiFi de Guayaquil y Quito.
- Controladoras específicas por nodo/provincia: `181.39.190.2` (nodo), `181.198.110.134` (Cisco), `181.39.24.107` (Huawei), `181.39.24.133` y `181.39.128.171:8081` (Omarsa).
- Para el cliente Omarsa, los host se reconocen como WIFI(1-9) y se requiere cambiar el tenantid a `dcifuentes` para acceder a la controladora.

## Menciones en la fuente

- "PERDIDA DE MONITOREO: TELCONET S.A. // login: tn_wifi2_parquesanrafael1" — [[Work/3. Corporativos|3. Corporativos]]
- "Estimados Radios GYE por favor su ayuda con la tarea 102757614" — [[Work/3. Corporativos|3. Corporativos]]
- "Estimados L1 su ayuda dando seguimiento a la tarea 101743384 del cliente danec-uio-eduardoberg que se encuentra aperturada desde el 2024-04-18, nuevamente se valida caído" — [[Work/3. Corporativos|3. Corporativos]]
- "**Ruckus** User: `IPCC`Pass:  `T!pccN2016`" — [[Work/3. Corporativos|3. Corporativos]]
- "Ingresar al siguiente link con el correo `noc@telconet.ec` y revisar codigo en el correo https://telconet.msp.ruckus.cloud/auth" — [[Work/3. Corporativos|3. Corporativos]]
- "**Huawei** User: `IPCC`Pass:  `T!pccN2016`" — [[Work/3. Corporativos|3. Corporativos]]
- "Nueva Controladora `https://181.39.24.107/`Claves Huawei" — [[Work/3. Corporativos|3. Corporativos]]
- "Mediante monitoreo proactivo se observa la caida del enlace AP Login: 	tn_wifi2_parquesanrafael1 con MAC 2C AC 5C 9C B0 is DOWN en la controladora HW  https://157.100.14.130/" — [[Work/3. Corporativos|3. Corporativos]]
- "**Cisco** User:  `Ipcc`Pass: `TipccN2014`" — [[Work/3. Corporativos|3. Corporativos]]
- "Controladora `181.198.110.134`Claves Cisco" — [[Work/3. Corporativos|3. Corporativos]]
- "Para validar los APs, se debe acceder a la controladora `181.198.110.134`en la seccion ***Wireless / All APs***" — [[Work/3. Corporativos|3. Corporativos]]
- "**Omarsa** User: `IPCC`Pass:  `T!pccN2016`" — [[Work/3. Corporativos|3. Corporativos]]
- "Controladora de Cliente Omarsa-Panama y los host son reconocibles como WIFI(1-9) por ejemplo WIFI1." — [[Work/3. Corporativos|3. Corporativos]]
- "### Controladora Omarsa https://181.39.128.171:8081/" — [[Work/3. Corporativos|3. Corporativos]]
- "Ruijie `https://cloud-la.ruijienetworks.com`" — [[Work/3. Corporativos|3. Corporativos]]