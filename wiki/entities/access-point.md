---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
type_confirmed: true
sources:
  - "[[sources/3-corporativos_04d2e4]]"
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
  - "product"
aliases:
  - "AP"
  - "APs"
  - "Punto de Acceso"
---

# Access Point

## Definición

Un **Access Point** (AP), o punto de acceso, es el dispositivo inalámbrico que provee cobertura WiFi a los clientes y que es administrado de forma centralizada desde las controladoras. En el contexto operativo del documento, el AP constituye la unidad de trabajo sobre la cual se ejecutan las tareas de validación, inventario y monitorización de la red inalámbrica corporativa.

## Características clave

- **Dispositivo de borde inalámbrico**: entrega cobertura WiFi a los clientes finales, actuando como punto de enlace entre la red cableada y los dispositivos inalámbricos.
- **Administración centralizada**: los APs no se configuran de forma aislada, sino que se gestionan desde las controladoras correspondientes.
- **Identificación dual (login y MAC)**: los enlaces de APs se monitorean tanto por su nombre de login como por su dirección MAC, lo que permite correlacionar el inventario lógico con el inventario físico.
- **Nomenclatura estandarizada**: los APs siguen convenciones de nombrado definidas por prefijos, tales como `AP_NODO-WIFIPOMASQUIUIO` o `tn_wifi2_`. Un ejemplo documentado de login es `tn_wifi2_parquesanrafael1`.
- **Agrupación por nodos**: los dispositivos se organizan en conjuntos denominados "APS Nodos WIFI", que facilitan la revisión y el inventario por sitio o zona de cobertura.
- **Estado operativo binario**: el estado del AP se expresa como UP o DOWN, y esta condición es la que determina la generación de notificaciones hacia soporte.
- **Configuración de hostname por AP**: para cada AP se debe cambiar el hostname al formato login/mac y verificar el grupo al cual se asigna.
- **Ajustes según fabricante de controladora**: si la controladora es RUCKUS debe agregarse '6.' adelante; además se modifica la sección inventory (Host Router y Name).
## Aplicaciones

- **Validación de inventario WiFi**: la verificación de los APs desplegados se realiza accediendo a la controladora en la sección *Wireless / All APs*.
- **Monitorización proactiva de enlaces**: el seguimiento continuo de los enlaces de APs (por login y por MAC) permite detectar degradaciones o caídas antes de que el cliente final las reporte.
- **Revisión de "APS Nodos WIFI"**: agrupación de los puntos de acceso por nodo para auditar cobertura y consistencia del despliegue.
- **Gestión de notificaciones de soporte**: la transición de estado UP/DOWN de un AP dispara alertas y flujos de escalamiento hacia los equipos de soporte.
- **Trazabilidad por nomenclatura**: el uso de prefijos consistentes (`AP_NODO-...`, `tn_wifi2_...`) permite mapear cada AP a su ubicación y a su propietario operativo.
- **Ingreso de APs**: el proceso operativo de *Ingresos de APs* permite registrar hasta 5 puntos de acceso por operación, con una IP de ingreso de 172.24.27.27.
- **Datos requeridos en el registro**: para cada AP se exige completar AP, Login Auxiliar, Nombre en la controladora, MAC e IP Controladora.
- **Actualización de MACROS**: el ingreso del AP incluye como paso adicional la actualización de MACROS.
## Conceptos relacionados

- [[concepts/controladora|Controladora]]
- [[concepts/monitorización-proactiva|Monitorización proactiva]]

## Entidades relacionadas

- [[entities/telconet|Telconet S.A.]]
- [[entities/noc-radio|NOC-RADIO]]
- [[entities/huawei|Huawei]]
- [[entities/cisco|Cisco]]
- [[entities/omarsa|Omarsa]]

## Menciones en la fuente

- "Para validar los APs, se debe acceder a la controladora `181.198.110.134`en la seccion ***Wireless / All APs***" — [[Work/3. Corporativos|3. Corporativos]]
- "Notificar chat: ***NOC-RADIO Revisiones APS Nodos WIFI***" — [[Work/3. Corporativos|3. Corporativos]]
- "Mediante monitoreo proactivo se observa la caida del enlace AP Login: 	tn_wifi2_parquesanrafael1 con MAC 2C AC 5C 9C B0 is DOWN en la controladora HW  https://157.100.14.130/" — [[Work/3. Corporativos|3. Corporativos]]
- "### Ingresos de APs (Hasta 5)" — [[Work/4.1 Telcograph|4.1 Telcograph]]
- "- [ ] AP
- [ ] Login Auxiliar
- [ ] Nombre en la controladora
- [ ] MAC 
- [ ] IP Controladora" — [[Work/4.1 Telcograph|4.1 Telcograph]]