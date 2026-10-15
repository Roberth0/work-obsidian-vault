---
type: concept
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
  - "term"
aliases:
  - "Controladora WiFi"
  - "Controladora inalámbrica"
  - "Wireless Controller"
---

# Controladora

## Definición

En el dominio de las redes inalámbricas corporativas, **Controladora** designa el dispositivo o plataforma central que administra los access points (AP) de un cliente o nodo. Es el punto de acceso administrativo desde el cual se aprovisiona, supervisa y valida el estado de los AP desplegados en una ubicación determinada.

Cada controladora se identifica por su dirección IP o URL. En el documento de referencia se listan varias:

- Controladora del nodo WiFi — `181.39.190.2`
- Controladora de provincias — `181.198.110.134` (Cisco)
- Nueva controladora — `181.39.24.107` (Huawei)
- Controladora — `181.39.24.133`
- Controladora del cliente Omarsa — `181.39.128.171:8081`

## Características clave

- **Administración centralizada:** concentra la gestión de los access points de un cliente o nodo, evitando la configuración individual de cada AP.
- **Identificación por IP o URL:** cada controladora se referencia mediante su dirección de red y, cuando corresponde, un puerto específico (por ejemplo `181.39.128.171:8081`).
- **Multi-proveedor:** el parque incluye controladoras de distintos fabricantes, como [[Cisco]], [[Huawei]] y [[Meraki]].
- **Validación de APs:** el trabajo operativo sobre la controladora se realiza típicamente en la sección *Wireless / All APs*, donde se verifica el estado de los puntos de acceso.
- **Multi-tenant:** en escenarios con clientes que comparten plataforma, como [[Omarsa]], es necesario cambiar el `tenantid` antes de ingresar a la controladora correspondiente.
- **Alcance variable:** existen controladoras asociadas a un nodo WiFi puntual, a un conjunto de provincias, o exclusivamente a un cliente.
- **RUCKUS como fabricante adicional:** el parque de controladoras incluye también dispositivos RUCKUS y el tipo de controladora condiciona el flujo de configuración: "Actualizar MACROS, si la controladora es **RUCKUS** agregar *6.* adelante".
## Aplicaciones

- **Soporte técnico:** el flujo de soporte incluye acceder a la controladora para validar los APs del cliente afectado.
- **Diagnóstico de conectividad inalámbrica:** permite confirmar si un AP está registrado, en línea o con problemas.
- **Gestión por cliente y por región:** facilita separar la operación entre nodos, provincias y clientes específicos.
- **Integración con [[Monitorización proactiva]]:** la controladora es una de las fuentes consultadas para anticipar incidentes en la red inalámbrica.
- **Ingreso de APs (hasta 5):** en el alta de APs, la controladora es un dato requerido, ya que se solicitan el "Nombre en la controladora" y la "IP Controladora", junto con AP, Login Auxiliar y MAC.
- **Actualización de MACROS según tipo de controladora:** si la controladora es **RUCKUS**, la regla operativa indica agregar *6.* adelante al actualizar los MACROS.
## Conceptos relacionados

- [[access-point|Access Point]]
- [[concepts/monitorización-proactiva|Monitorización proactiva]]

## Entidades relacionadas

- [[entities/huawei|Huawei]]
- [[entities/cisco|Cisco]]
- [[entities/meraki|Meraki]]
- [[entities/omarsa|Omarsa]]

## Menciones en la fuente

- "**Controladora** `181.39.190.2` User: `IPCC-NCE` Pass: `!PCCl1*TN2024`" — [[Work/3. Corporativos|3. Corporativos]]
- "Controladora `181.198.110.134`Claves Cisco" — [[Work/3. Corporativos|3. Corporativos]]
- "Para validar los APs, se debe acceder a la controladora `181.198.110.134`en la seccion ***Wireless / All APs***" — [[Work/3. Corporativos|3. Corporativos]]
- "- [ ] Nombre en la controladora
- [ ] MAC 
- [ ] IP Controladora" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "Actualizar MACROS, si la controladora es **RUCKUS** agregar *6.* adelante" — [[Work/4.1 Telcograph|4.1 Telcograph]]