---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "Red Privada Virtual"
  - "Virtual Private Network"
  - "VPN de Cedia"
generation_complete: true
---

# VPN

## Definición

La VPN (Red Privada Virtual, del inglés *Virtual Private Network*) es el mecanismo de acceso remoto seguro utilizado para conectarse a las herramientas de gestión de red. En el contexto del documento, constituye la vía de acceso al [[SAM CLIENT]] a través de la VPN de [[CEDIA]], y representa un requisito previo indispensable para ejecutar los diagnósticos y monitoreos descritos.

## Características clave

- **Acceso remoto seguro**: permite alcanzar herramientas de gestión de red internas desde fuera de la red local.
- **Autenticación mediante credenciales**: el flujo de conexión requiere seleccionar `Username and Password` como método de autenticación.
- **Credenciales específicas por VPN**: para la VPN de Cedia se emplea el usuario `userTelco` con la contraseña `Telc0VPN`.
- **Múltiples implementaciones**: el documento menciona además otras VPN, como CheckPoint VPN, cada una con sus propias credenciales.
- **Dependencia operativa**: las credenciales de VPN son un requisito previo para la ejecución de los diagnósticos y monitoreos.

## Aplicaciones

- Conexión al [[SAM CLIENT]] para tareas de gestión, diagnóstico y monitoreo de red.
- Acceso a herramientas internas de [[CEDIA]] desde ubicaciones remotas.
- Uso alternativo de otras plataformas VPN (por ejemplo, CheckPoint VPN) según las credenciales disponibles.
- Escenarios de soporte y verificación de enlaces, donde el acceso previo por VPN condiciona la obtención de resultados como el [[link loss]].

## Conceptos relacionados

- [[concepts/informe-ejecutivo|Informe Ejecutivo]]
- [[concepts/link-loss|link loss]]

## Entidades relacionadas

- [[entities/sam-client|SAM CLIENT]]
- [[entities/cedia|CEDIA]]

## Menciones en la fuente

- "Para acceder al SAM CLIENT se debe conectarse a la VPN de Cedia con las siguientes credenciales" — [[Work/4 Cedia|4 Cedia]]
- "ii. En el método de autenticación seleccionamos “Username and Password”" — [[Work/4 Cedia|4 Cedia]]
- "3. Para conectarse a la VPN usaremos como usuario: userTelco y como contraseña Telc0VPN" — [[Work/4 Cedia|4 Cedia]]