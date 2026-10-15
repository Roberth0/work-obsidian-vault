---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "NOC MIMG"
  - "Área MIMG"
generation_complete: true
---

# MIMG

## Descripción

MIMG es un área o nodo de gestión del [[NOC]] de [[Telconet S.A.|Telconet]] encargado de administrar los logins de la red WiFi identificados con el prefijo `tn_wifi2_`. Según el documento de origen, MIMG gestiona los logins `tn_wifi2_` correspondientes a [[Guayaquil]] y [[Quito]] que aparecen en el listado del panel [[Telcograf]], asociados a la variable de grupo `MUNICIPIO_DEL_DISTRITO_METROPOLITANO_DE_QUITO`. Esta gestión se realiza en coordinación con las [[Credenciales]] del usuario `noc`, lo que vincula cada [[Login]] administrado por MIMG con un conjunto de credenciales de acceso compartido. MIMG forma parte de la estructura operativa de NOC de Telconet junto a [[NOC-RADIO]] y los equipos de radio de GYE (Guayaquil) y UIO (Quito). Su rol es, por tanto, de carácter administrativo y de control de acceso sobre los logins WiFi corporativos de las dos principales ciudades atendidas, más que de operación directa de radiofrecuencia.

## Entidades relacionadas

- [[entities/noc|NOC]]
- [[entities/telconet|Telconet S.A.]]
- [[entities/gye|Guayaquil]]
- [[entities/uio|Quito]]
- [[entities/telcograf|Telcograf]]

## Conceptos relacionados

- [[concepts/login|Login]]
- [[entities/0-1-correos-y-claves|Credenciales]]

## Menciones en la fuente

- "Gestiona NOC MIMG logins con tn_wifi2_.... que sean de guayaquil y de quito los que esten en el siguiente listado del [Telcograf]" — [[Work/3. Corporativos|3. Corporativos]]