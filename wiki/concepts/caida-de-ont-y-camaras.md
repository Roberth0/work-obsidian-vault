---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Caída de ONT y cámaras"
  - "Caída puntual de ONT y cámaras"
  - "Falla de ONT y cámaras"
generation_complete: true
---

# Caida de ONT y camaras

## Definición

La **caída de ONT y cámaras** es un incidente operativo de red en el que los equipos de cliente final —la ONT (terminación de red óptica) y las cámaras asociadas al servicio— pierden conectividad. Puede presentarse de forma **masiva** (afectando a un conjunto amplio de usuarios o a una caja completa) o de forma **puntual** (limitada a uno o pocos casos). Su diagnóstico se realiza revisando el estado de la OLT en el OSS.

## Características clave

- **Alcance variable:** el incidente puede ser masivo o puntual; su clasificación depende del estado de las OLTs involucradas.
- **Criterio de clasificación:** si todas las OLTs de la caja están caídas, se trata de un problema masivo o [[Caida de caja]]; si al menos una OLT permanece activa, el problema es puntual.
- **Diagnóstico centralizado:** el estado de la OLT se verifica en el [[OSS]].
- **Afectación de servicios:** la caída compromete la ONT del cliente y las cámaras que dependen de ese enlace.
- **Flujo de gestión definido:** ante un problema puntual se crea un caso con tarea hacia [[Andy Enrique Barberan Cortez]] y se asigna el caso a L1 Adrian Bonilla.
- **Registro de seguimiento:** se documentan los motivos NOC y OSS, junto con datos como login aux, IP y la UM correspondiente.
- **Notificación:** el aviso del incidente se envía por correo electrónico.

## Aplicaciones

- **Diagnóstico de incidentes de acceso óptico:** permite determinar rápidamente si la pérdida de servicio de una ONT y sus cámaras corresponde a una falla puntual del cliente o a una afectación mayor de la red.
- **Triaje y escalamiento en NOC:** sirve como criterio de decisión para crear casos, asignar tareas y derivar el incidente al nivel correspondiente.
- **Desambiguación frente a otros cortes:** ayuda a distinguir esta falla de eventos de infraestructura como el [[Corte de Fibra]] o el [[Corte de ultima Milla]].
- **Trazabilidad operativa:** el registro de motivos y datos de acceso facilita el seguimiento, la auditoría y el análisis posterior del incidente.

## Conceptos relacionados

- [[concepts/caida-de-caja|Caida de caja]]
- [[concepts/corte-de-fibra|Corte de Fibra]]
- [[concepts/corte-de-ultima-milla|Corte de ultima Milla]]
- [[concepts/motivo-noc-y-motivo-oss|Motivo NOC y Motivo OSS]]

## Entidades relacionadas

- [[entities/oss|OSS]]
- [[entities/olt|OLT]]
- [[entities/ont|ONT]]
- [[entities/andy-enrique-barberan-cortez|Andy Enrique Barberan Cortez]]

## Menciones en la fuente

- "Se debe verificar el tipo de caida, si todos las OLTs de la caja se encuentran caidas se debe a un problema masivo / caida de caja. Si ahi alguna OLT activa significa que el problema es puntual." — [[Work/2.1 CSCG|2.1 CSCG]]
- "Mediante monitoreo se verifica ONT caído, asociado al login aux: cscgvidanalit-mapa95mz17_1. IP: 10.211.16.15. Se envia vía mail la notificación. UM: olt-hw-1-mapasingue6-gye 1/8." — [[Work/2.1 CSCG|2.1 CSCG]]