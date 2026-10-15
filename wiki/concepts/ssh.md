---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/1-backbone_5939cb]]"
tags:
aliases:
  - "Secure Shell"
  - "respuesta SSH"
generation_complete: true
---

# SSH

## Definición

SSH (Secure Shell) es el protocolo de acceso remoto utilizado para validar y administrar equipos de la red. En el contexto de la fuente, constituye uno de los dos mecanismos de verificación de disponibilidad y acceso descritos, junto con [[ICMP]].

## Características clave

- **Protocolo de acceso remoto**: permite iniciar sesión y administrar equipos de red de forma remota.
- **Verificación de acceso**: la existencia o ausencia de respuesta SSH funciona como comprobación del estado y del acceso a un equipo.
- **Criterio de escalamiento**: la falta de respuesta SSH se trata como un criterio de escalamiento — si no se tiene respuesta SSH, la tarea debe escalarse a [[NW]].
- **Autenticación por operador**: el acceso se realiza indicando un operador específico mediante el parámetro `-l`, lo que permite trazabilidad de quién ejecuta la gestión.
- **Complementario a ICMP**: mientras [[ICMP]] verifica alcanzabilidad de red, SSH verifica capacidad de acceso y administración.

## Aplicaciones

- **Administración de equipos de red**: acceso a dispositivos para validación y gestión operativa.
- **Acceso a equipos Hillstone**: por ejemplo, mediante el comando `ssh -l noc-operator` sobre [[Hillstone]].
- **Login Metrovia**: por ejemplo, mediante el comando `ssh -l ipccl2-gye1` sobre [[Login Metrovia]].
- **Diagnóstico y escalamiento**: cuando un equipo no responde a SSH, se determina el escalamiento de la tarea hacia [[NW]].
- **Verificación de disponibilidad**: usado junto con [[ICMP]] como mecanismo de comprobación en procedimientos operativos.

## Conceptos relacionados

- [[concepts/icmp|ICMP]]

## Entidades relacionadas

- [[entities/nw|NW]]
- [[entities/hillstone|Hillstone]]

## Menciones en la fuente

- "Si no se tiene respuesta SSH se debe escalar la tarea a NW" — [[Work/1. Backbone|1. Backbone]]
- "`ssh -l noc-operator fwhdcgye1`" — [[Work/1. Backbone|1. Backbone]]
- "`ssh -l ipccl2-gye1`" — [[Work/1. Backbone|1. Backbone]]