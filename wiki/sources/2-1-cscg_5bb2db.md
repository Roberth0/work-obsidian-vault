---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/2.1 CSCG.md]]"
tags: [gye, camaras, vips]
aliases: ["2.1 CSCG", "Procedimientos CSCG"]
contentHash: 1015-11332840
generation_complete: true
---

# 2.1 CSCG - Resumen

## Fuente

- Archivo original: [[Work/2.1 CSCG.md]]
- Ingerido: 2026-09-23

## Contenido principal

Este documento describe los procedimientos operativos de monitoreo y gestión de incidencias del área **CSCG**, vinculada a la red de VIPS. Detalla cómo gestionar distintos tipos de alertas provenientes del sistema [[entities/zabbix|Zabbix]] y del [[entities/oss|OSS]]: caída de [[entities/olt|OLT]] y [[entities/camaras|Camaras]] en Machala y Salinas, [[concepts/caida-de-caja|caída de caja]], [[concepts/temperatura-elevada|temperatura elevada]] en [[entities/ont|ONT]] y caída puntual de ONT o cámaras. Para cada escenario especifica pasos concretos: crear el caso, escalar la tarea o el caso a los niveles L1 y TS mediante el [[concepts/escalamiento-a-ts-y-l1|escalamiento]], verificar el estado de puertos y OLTs, y notificar por el chat de [[entities/monitoreo-cscg|Monitoreo CSCG]]. También incluye la [[concepts/distribucion-zonas|distribución de zonas de GYE]], los formatos de [[concepts/motivo-noc-y-motivo-oss|motivo NOC y motivo OSS]] y el tratamiento del [[concepts/error-300|error 300]] de Inteligencia Artificial.

## Entidades clave

- [[entities/zabbix|Zabbix]] — plataforma de monitoreo donde se originan los casos y tareas.
- [[entities/oss|OSS]] — sistema de gestión de red para diagnosticar el estado de las OLTs y cajas.
- [[entities/olt|OLT]] — equipo óptico terminal cuyo estado determina el tipo de incidencia.
- [[entities/ont|ONT]] — equipo óptico de cliente sujeto a caídas y alertas de temperatura.
- [[entities/opu-gye|OPU GYE]] — equipo operativo contactado ante caídas de caja.
- [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]] — responsable de tareas por temperatura elevada y caídas puntuales de OLT.
- [[entities/gye|GYE]] — zona operativa de Guayaquil que organiza los escalamientos.
- [[entities/monitoreo-cscg|Monitoreo CSCG]] — grupo de WhatsApp para notificar y coordinar tareas.
- [[entities/camaras|Camaras]] — dispositivos de videovigilancia monitoreados.

## Conceptos clave

- [[concepts/caida-de-caja|Caída de caja]] — incidente masivo cuando todas las OLTs de una caja están caídas.
- [[concepts/caida-de-ont-y-camaras|Caída de ONT y cámaras]] — incidente masivo o puntual según el estado de la OLT.
- [[concepts/temperatura-elevada|Temperatura elevada]] — alerta gestionada solo después de las 18H00.
- [[concepts/corte-de-fibra|Corte de Fibra]] — causa registrada como motivo NOC.
- [[concepts/corte-de-ultima-milla|Corte de última milla]] — causa registrada como motivo OSS.
- [[concepts/error-300|Error 300]] — falla de Inteligencia Artificial por grabación incorrecta.
- [[concepts/motivo-noc-y-motivo-oss|Motivo NOC y Motivo OSS]] — campos obligatorios en el seguimiento de tareas.
- [[concepts/escalamiento-a-ts-y-l1|Escalamiento a TS y L1]] — método de distribución de casos y tareas.
- [[concepts/caida-de-camaras|Caída de cámara/s]] — pérdida de una o varias cámaras de videovigilancia.
- [[concepts/sin-respuesta-icmp|Sin respuesta ICMP]] — motivo OSS que confirma la caída de una cámara.
- [[concepts/distribucion-zonas|Distribución de zonas de GYE]] — criterio de enrutamiento geográfico y horario.
- [[concepts/status-puertos|Status puertos]] — opción del OSS para localizar puerto y caja.
- [[concepts/inventario-del-zabbix|Inventario del zabbix]] — opción para obtener la IP de una cámara antes del ping.

## Puntos principales

- Ante caídas de OLT y cámaras en Machala y Salinas se debe crear un caso normal y escalar la tarea a la TS y el caso a L1.
- Ante [[concepts/caida-de-caja|caída de caja]] se crea el caso desde [[entities/zabbix|Zabbix]] por la caída de la [[entities/ont|ONT]], se escala la tarea según la [[concepts/distribucion-zonas|distribución de zonas de GYE]] y el caso a L1, y se llama a [[entities/opu-gye|OPU GYE]] según la ubicación de la caja.
- La atención telefónica por caída de caja se distribuye por horario: 8am-5pm Miguel Angel Montoya, 5pm-11pm Erick Uscocovich y 11pm-7am Marlon Brito.
- La [[concepts/temperatura-elevada|temperatura elevada]] solo se gestiona después de las 18H00; fuera de ese horario se comenta "---No se da gestion de 07H00 a 18H00".
- Para temperatura elevada se crea una tarea hacia [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]] desde Zabbix, se reasigna en el perfil de Telcos y se notifica por el chat de [[entities/monitoreo-cscg|Monitoreo CSCG]].
- La caída de OLT se diagnostica en el [[entities/oss|OSS]] mediante [[concepts/status-puertos|status puertos]]: si todas las OLTs de una caja están caídas es problema masivo; si alguna está activa, es problema puntual.
- En problemas puntuales de caída de OLT se crea un caso con tarea hacia Andy Barberan y se asigna a L1 Adrian Bonilla.
- La caída de cámaras se diagnostica verificando que la OLT esté activa y haciendo ping a la cámara usando el [[concepts/inventario-del-zabbix|inventario del zabbix]]; si no hay respuesta ICMP se crea un caso desde Zabbix.
- El seguimiento de tareas exige registrar el [[concepts/motivo-noc-y-motivo-oss|motivo NOC y motivo OSS]] usando plantillas como "Corte de Fibra / Corte de ultima Milla" o "Camara Down / Sin respuesta ICMP".
- El [[concepts/error-300|error 300]] de Inteligencia Artificial (grabación incorrecta) requiere una tarea para Marjorie Alexandra Chalen Troya, con ejemplo de tarea 107821158 sobre el equipo cscgvidanalit-csrcal52a3_5.
- Existe una tarea RDA por problemas en el OSS con el número 131799124.

## Menciones en la fuente

- "Se debe crear el caso desde el zabbix por la caida de la ONT" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Dentro del horario se debe crear una tarea hacia ***ANDY ENRIQUE BARBERAN CORTEZ*** desde el zabbix de monitoreo" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Si se verifica que no se tiene respuesta ICMP se debe crear un caso por la caida de la camara/s desde el zabbix" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Se debe revisar en el [OSS](https://oss.netlife.net.ec/dashboard) el estado de la OLT, si la OLT esta down se debe realizar el diagnostico" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Al verificar en el OSS que se tiene una caida de caja se debe llamar a OPU GYE para ello se tiene la siguiente distrubucion de acuerdo a la ubicacion de la caja" — [[Work/2.1 CSCG|2.1 CSCG]]
- "En el seguimiento de la tarea se debe ingresar el motivo presente en la alerta de zabbix y el motivo presente el la interfaz del OSS" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Se debe verificar el tipo de caida, si todos las OLTs de la caja se encuentran caidas se debe a un problema masivo / caida de caja. Si ahi alguna OLT activa significa que el problema es puntual." — [[Work/2.1 CSCG|2.1 CSCG]]
- "UM: olt-hw-1-mapasingue6-gye 1/8." — [[Work/2.1 CSCG|2.1 CSCG]]
- "Mediante monitoreo se verifica ONT caído, asociado al login aux: cscgvidanalit-mapa95mz17_1. IP: 10.211.16.15. Se envia vía mail la notificación. UM: olt-hw-1-mapasingue6-gye 1/8." — [[Work/2.1 CSCG|2.1 CSCG]]
- "Estimado @+593 99 871 8125 (Andy Barberan) se asigna la tarea 107853621 || Temperatura elevada ONT: tncto-pasillocoworking-gye VALUE: 51 C" — [[Work/2.1 CSCG|2.1 CSCG]]
- "En horario Laboral por cadida de caja llamar a **Miguel Angel Montoya**" — [[Work/2.1 CSCG|2.1 CSCG]]
- "8am - 5pm Miguel Angel Montoya" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Hasta las 12pm con **Erick Uscocovich**" — [[Work/2.1 CSCG|2.1 CSCG]]
- "5pm -11pm Erick Uscocovich" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Veladas con **Marlon Brito**" — [[Work/2.1 CSCG|2.1 CSCG]]