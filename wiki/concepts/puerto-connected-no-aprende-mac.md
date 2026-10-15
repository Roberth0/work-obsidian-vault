---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/101-telcos-zabbix-optimizaciones_942fa6]]"
tags:
aliases:
  - "Puerto connected no aprende MAC y no ahi ping vrf"
  - "Puerto conectado sin aprendizaje MAC"
  - "Puerto connected sin ping en VRF"
generation_complete: true
---

# Puerto connected, no aprende MAC

## Definición

"Puerto connected, no aprende MAC y no ahi ping vrf" es el síntoma técnico recurrente que se registra en el campo motivo de las tareas de Troubleshooting proactivo en Telcos. Describe una condición en la que el puerto de la unidad de monitoreo aparece en estado *connected*, pero no aprende direcciones MAC y tampoco responde a ping dentro de la VRF asociada. Es una señal típica de enlace caído, degradado o mal configurado, y funciona como criterio de clasificación para la generación y el envío automático de correos de notificación a los APs.

## Características clave

- El puerto se reporta como *connected*, lo que descarta a primera vista una caída física evidente del enlace.
- No se produce aprendizaje de direcciones MAC: no hay tráfico de capa 2 entrante en el puerto.
- El ping dentro de la VRF no obtiene respuesta, lo que indica que la conectividad de capa 3 tampoco está operativa.
- Se registra de forma reiterada en el campo motivo de las tareas de Troubleshooting proactivo.
- Aparece asociado a puertos e interfaces concretas de equipos de la red, como `sw1fortinesuio.telconet.net Fa0/33`, `sw1sanfernandogiron-ten.telconet.net Gi1/0/10` y `sw3gasparuio-tengig.telconet.net Gi2/0/9`.
- Presenta una variante registrada como "Puerto not connected", observada en `uce-agronomiatumbaco`.
- Actúa como disparador de la clasificación y del envío automático de correos de notificación a los APs.

## Aplicaciones

- **Clasificación de tareas de Troubleshooting proactivo:** el texto del síntoma permite categorizar automáticamente las tareas en función del tipo de fallo detectado.
- **Notificación automatizada a los APs:** cuando se detecta el síntoma, el flujo de trabajo envía correos de notificación a los responsables.
- **Diagnóstico de enlaces caídos o mal configurados:** la combinación de estado *connected* sin aprendizaje MAC y sin respuesta de ping orienta la revisión hacia problemas de configuración, VLAN o VRF más que hacia una caída física.
- **Correlación con la telemetría de monitoreo:** el síntoma se apoya en los datos recogidos por la plataforma de monitoreo de la infraestructura.
- **Seguimiento de reincidencias por equipo e interfaz:** la repetición del síntoma en distintos dispositivos permite identificar patrones recurrentes en la red.

## Conceptos relacionados

- [[concepts/reasignartarea|reasignarTarea]]
- [[concepts/motivo|motivo]]
- [[concepts/login-aux|login aux]]

## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/zabbix|Zabbix]]

## Menciones en la fuente

- "UM: sw1fortinesuio.telconet.net Fa0/33. Puerto connected, no aprende MAC y no ahi ping vrf." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "UM: sw1allcomp1-ten.telconet.net Gi1/0/11. Puerto connected, no aprende MAC" — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]
- "UM: sw1cipresesuio-tengig.telconet.net Gi2/0/7. Puerto not connected." — [[Work/101. Telcos - Zabbix optimizaciones|101. Telcos - Zabbix optimizaciones]]