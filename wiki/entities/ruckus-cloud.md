---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "Ruckus Cloud (MSP)"
  - "telconet.msp.ruckus.cloud"
  - "Ruckus Cloud MSP"
generation_complete: true
---

# Ruckus Cloud

## Descripción

Ruckus Cloud es la plataforma en la nube de gestión de controladoras [[Controladora|controladoras]] Ruckus empleada por [[Telconet S.A.]] para la administración de su red inalámbrica corporativa. El acceso se realiza a través de la URL `https://telconet.msp.ruckus.cloud/auth`, un portal dedicado a la instancia MSP (Managed Service Provider) de la organización. Según el documento, el ingreso se efectúa con el correo `noc@telconet.ec`, tras lo cual se solicita un código enviado al mismo correo electrónico como segundo factor de autenticación, esquema que refuerza el control sobre las [[Credenciales|credenciales]] del [[NOC]].

La plataforma está asociada a la controladora cuya IP es `34.102.183.44`, por lo que funciona como punto central de [[Login|inicio de sesión]] y supervisión de ese equipo. Junto a las controladoras Huawei, Cisco, Omarsa y Ruijie, Ruckus Cloud forma parte del conjunto de plataformas de administración inalámbrica utilizadas para el soporte de los nodos WiFi corporativos. Su uso está orientado a las tareas operativas del [[NOC]], que gestiona el aprovisionamiento, la verificación de estado y la resolución de incidentes sobre los puntos de acceso asociados.

## Entidades relacionadas

- [[entities/noc|NOC]]
- [[entities/telconet|Telconet S.A.]]

## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[entities/0-1-correos-y-claves|Credenciales]]
- [[concepts/login|Login]]

## Menciones en la fuente

- "### Controladora https://34.102.183.44

Ingresar al siguiente link con el correo `noc@telconet.ec` y revisar codigo en el correo
https://telconet.msp.ruckus.cloud/auth" — [[Work/3. Corporativos|3. Corporativos]]