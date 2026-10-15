---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/2-1-cscg_5bb2db]]"
tags:
aliases:
  - "Motivo NOC"
  - "Motivo OSS"
  - "NOC Reason and OSS Reason"
generation_complete: true
---

# Motivo NOC y Motivo OSS

## Definición

**Motivo NOC y Motivo OSS** son los dos campos obligatorios que se registran en el seguimiento de tareas al momento de documentar incidencias de CSCG. El primero corresponde al motivo presente en la alerta de [[Zabbix]], es decir, la causa tal como la reporta el Centro de Operaciones de Red (NOC); el segundo corresponde al motivo presente en la interfaz del [[OSS]], esto es, la causa observada directamente en el sistema de soporte de operaciones.

Ambos campos se capturan de forma conjunta y complementaria: no se trata de dos nombres para un mismo dato, sino de dos perspectivas distintas sobre una misma incidencia —la reportada por la herramienta de monitoreo y la verificada en el sistema de gestión— que en conjunto permiten clasificar y dar trazabilidad a la causa raíz.

## Características clave

- **Registro dual y obligatorio:** toda incidencia documentada en el seguimiento de tareas de CSCG requiere que se ingresen ambos motivos; ninguno es opcional ni sustituye al otro.
- **Origen diferenciado de cada campo:** el *Motivo NOC* proviene de la alerta emitida por [[Zabbix]]; el *Motivo OSS* proviene de lo observado en la interfaz del [[OSS]].
- **Formato de par de valores:** se documentan como una dupla separada por barra inclinada (`Motivo NOC / Motivo OSS`), lo que facilita su lectura y comparación inmediata.
- **Estandarización mediante plantillas:** existen combinaciones de ejemplo predefinidas para los escenarios más frecuentes, lo que reduce la ambigüedad en el registro.
- **Valor diagnóstico comparativo:** el contraste entre ambos motivos permite detectar discrepancias entre lo que reporta el monitoreo y lo que confirma el OSS, por ejemplo cuando una alerta de red corresponde en realidad a un corte de fibra o a un equipo apagado.
- **Aplicable a distintos tipos de incidencia:** cubre fallas eléctricas, cortes de fibra, cortes de última milla y caídas de cámaras, entre otras.

## Aplicaciones

- **Documentación de incidencias de CSCG:** llenado obligatorio de los campos en el seguimiento de tareas cada vez que se registra un caso.
- **Clasificación de causa raíz:** permite agrupar y analizar incidencias por tipo (eléctrica, fibra, última milla, cámara) para detectar patrones recurrentes.
- **Escenarios con plantilla predefinida:**
  - `Problema Electrico / Equipo Apagado` — falla de energía que resulta en un equipo sin operación.
  - `Corte de Fibra / Corte de UM` — corte reportado en la alerta que se confirma como corte de última milla en el OSS.
  - `Camara Down / Sin respuesta ICMP` — cámara caída cuya verificación en el OSS no obtiene respuesta a ICMP.
- **Escalamiento y coordinación:** al contar con ambos motivos, los equipos de NOC y de operaciones OSS comparten un lenguaje común para el traspaso de casos.
- **Trazabilidad y reportería:** la consistencia del par de campos habilita históricos comparables y métricas de recurrencia por tipo de falla.

## Conceptos relacionados

- [[concepts/corte-de-fibra|Corte de Fibra]]
- [[concepts/corte-de-ultima-milla|Corte de ultima Milla]]
- [[concepts/caida-de-ont-y-camaras|Caida de ONT y camaras]]

## Entidades relacionadas

- [[entities/zabbix|Zabbix]]
- [[entities/oss|OSS]]

## Menciones en la fuente

- "En el seguimiento de la tarea se debe ingresar el motivo presente en la alerta de zabbix y el motivo presente el la interfaz del OSS" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Motivo NOC: Problema Electrico
Motivo OSS: Equipo Apagado" — [[Work/2.1 CSCG|2.1 CSCG]]
- "Motivo NOC: Camara Down
Motivo OSS: Sin respuesta ICMP" — [[Work/2.1 CSCG|2.1 CSCG]]