---
type: concept
created: 2026-09-23
updated: 2026-09-23
sources:
  - "[[sources/4-cedia_d7cef1]]"
tags:
aliases:
  - "Autenticación Usuario y Contraseña"
  - "Username/Password"
  - "Usuario y contraseña"
generation_complete: true
---

# Username and Password

## Definición

**Username and Password** es el método de autenticación que debe seleccionarse en el cliente VPN para establecer la conexión con la red corporativa de [[Telconet|Telconet/Cedia]]. Consiste en elegir la opción de autenticación basada en credenciales y, a continuación, introducir el nombre de usuario y la contraseña asignados (`userTelco` / `Telc0VPN`) para completar la negociación con el servidor de acceso remoto.

## Características clave

- **Selección explícita en el cliente:** no es un mecanismo automático; el usuario debe escoger la opción *Username and Password* entre los métodos de autenticación disponibles en el cliente VPN.
- **Basado en credenciales estáticas:** requiere un par usuario/contraseña previamente provisto por el administrador de la red.
- **Paso obligatorio del flujo de conexión:** sin esta selección y el posterior ingreso de credenciales, el túnel no se establece y no se obtiene acceso a la red corporativa.
- **Credenciales específicas del entorno:** en el procedimiento documentado se emplean el usuario `userTelco` y la contraseña `Telc0VPN`.
- **Dependiente del canal seguro:** opera conjuntamente con el [[VPN|cliente VPN]]; su correcta configuración condiciona la disponibilidad del resto del procedimiento.

## Aplicaciones

- **Conexión a la VPN corporativa:** escenario principal, donde el técnico o colaborador debe autenticarse antes de trabajar sobre la infraestructura de Telconet/Cedia.
- **Acceso a herramientas internas:** una vez autenticado, el usuario puede alcanzar los sistemas y aplicaciones de gestión alojados en la red privada.
- **Administración de equipos gestionados:** habilita la conexión remota a dispositivos monitoreados, lo que permite diagnóstico, configuración y soporte.
- **Diagnóstico de fallos de conectividad:** una autenticación incorrecta o una selección errónea del método puede manifestarse como imposibilidad de acceso, un síntoma que conviene distinguir de una [[link loss|pérdida de enlace]] en la red.

## Conceptos relacionados

- [[concepts/vpn|VPN]]
- [[concepts/link-loss|link loss]]

## Entidades relacionadas

- [[entities/telconet|Telconet]]

## Menciones en la fuente

- "ii. En el método de autenticación seleccionamos “Username and Password”" (ii. En el método de autenticación seleccionamos “Username and Password”) — [[Work/4 Cedia|4 Cedia]]
- "3. Para conectarse a la VPN usaremos como usuario: userTelco y como contraseña Telc0VPN" (3. Para conectarse a la VPN usaremos como usuario: userTelco y como contraseña Telc0VPN) — [[Work/4 Cedia|4 Cedia]]