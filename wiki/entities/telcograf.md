---
type: entity
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/3-corporativos_04d2e4]]"
tags:
aliases:
  - "telcograf.telconet.ec"
  - "Plataforma Telcograf"
generation_complete: true
---

# Telcograf

## Descripción

Telcograf es una plataforma de visualización de datos con enfoque de dashboard, análoga a Grafana, alojada en el dominio `telcograf.telconet.ec`. Es utilizada por el [[NOC]] de [[Telconet S.A.]] como herramienta de consulta operativa para revisar el estado de los [[Access Point|access points]] de la red. El documento de origen enlaza a un panel específico denominado *access-point*, el cual expone variables de **grupo** y **host** que permiten filtrar la información mostrada. Mediante ese panel se listan los logins con prefijo `tn_wifi2_` correspondientes a las plazas de Guayaquil y Quito. El enlace concreto hace referencia al grupo `MUNICIPIO_DEL_DISTRITO_METROPOLITANO_DE_QUITO` y al host `tn_wifi2_parpomasquimirador`. Su existencia dentro del flujo documental de Telconet sugiere que Telcograf funciona como capa de observabilidad de la infraestructura inalámbrica, complementaria a las herramientas de recolección de métricas como [[Zabbix]].

## Entidades relacionadas

- [[entities/telconet|Telconet S.A.]]
- [[entities/noc|NOC]]
- [[entities/zabbix|zabbix]]

## Conceptos relacionados

- [[access-point|Access Point]]
- [[concepts/monitorización-proactiva|Monitorización proactiva]]

## Menciones en la fuente

- "Gestiona NOC MIMG logins con tn_wifi2_.... que sean de guayaquil y de quito los que esten en el siguiente listado del [Telcograf](https://telcograf.telconet.ec/pM5jDZYe9Ws4JI=/d/9OHSQ8Mint4/2-1-access-point?orgId=267&var-grupo=MUNICIPIO_DEL_DISTRITO_METROPOLITANO_DE_QUITO&var-host=tn_wifi2_parpomasquimirador)" — [[Work/3. Corporativos|3. Corporativos]]