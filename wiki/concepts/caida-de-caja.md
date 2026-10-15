---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "caída de caja"
  - "problema masivo"
  - "caída masiva de caja"
generation_complete: true
---

# Caida de caja

## Definición

La **caída de caja** es un incidente masivo de red en el que **todas las OLTs asociadas a una caja se encuentran caídas**. Se trata de un evento de alcance colectivo —no de un fallo aislado de un equipo— cuya detección y gestión sigue un procedimiento específico de verificación, notificación y escalamiento definido en la operación.

## Características clave

- **Alcance masivo:** la condición que la define es que *todas* las OLTs vinculadas a una misma caja estén caídas de forma simultánea.
- **Criterio de distinción:** se diferencia de los **problemas puntuales**, que ocurren cuando al menos una OLT permanece activa. La caída de caja exige que ninguna de las OLTs de la caja esté operativa.
- **Verificación en el OSS:** la confirmación del evento se realiza consultando el [[OSS]] antes de activar el procedimiento.
- **Notificación a [[OPU GYE]]:** la comunicación se dirige a OPU GYE según la **ubicación de la caja** afectada.
- **Generación de caso en [[Zabbix]]:** el caso se crea por la caída de la [[ONT]].
- **Escalamiento obligatorio:** el caso se crea de forma normal y debe escalarse, con la tarea dirigida a [[Escalamiento a TS y L1|TS]] y el caso a [[Escalamiento a TS y L1|L1]], siguiendo la distribución de zonas de GYE.
- **Distribución de la atención telefónica:** el atendimiento telefónico se reparte por horario entre Miguel Angel Montoya, Erick Uscocovich y Marlon Brito.

## Aplicaciones

El concepto se aplica en la operación de monitoreo y mesa de ayuda (NOC) para resolver incidentes de alcance colectivo:

1. **Detección:** identificar mediante monitoreo que todas las OLTs de una caja están caídas.
2. **Verificación:** confirmar en el [[OSS]] que se trata efectivamente de una caída de caja y no de un problema puntual.
3. **Notificación:** llamar a [[OPU GYE]] de acuerdo con la ubicación de la caja.
4. **Registro:** crear el caso en [[Zabbix]] por la caída de la [[ONT]].
5. **Escalamiento:** crear el caso de forma normal y escalarlo, enviando la tarea a [[Escalamiento a TS y L1|TS]] y el caso a [[Escalamiento a TS y L1|L1]], respetando la distribución de zonas de GYE.
6. **Cobertura telefónica:** distribuir la atención telefónica por horario entre Miguel Angel Montoya, Erick Uscocovich y Marlon Brito.

## Conceptos relacionados

- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]
- [[concepts/escalamiento-a-ts-y-l1|Escalamiento a TS y L1]]
- [[concepts/corte-de-fibra|Corte de Fibra]]
- [[concepts/corte-de-ultima-milla|Corte de ultima Milla]]

## Entidades relacionadas

- [[entities/oss|OSS]]
- [[entities/zabbix|Zabbix]]
- [[entities/olt|OLT]]
- [[entities/ont|ONT]]
- [[entities/opu-gye|OPU GYE]]

## Menciones en la fuente

- "Se debe crear el caso desde el zabbix por la caida de la ONT" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Al verificar en el OSS que se tiene una caida de caja se debe llamar a OPU GYE para ello se tiene la siguiente distrubucion de acuerdo a la ubicacion de la caja" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Se debe verificar el tipo de caida, si todos las OLTs de la caja se encuentran caidas se debe a un problema masivo / caida de caja." — [[Work/2.1 CSCG|2.1 CSCG]]