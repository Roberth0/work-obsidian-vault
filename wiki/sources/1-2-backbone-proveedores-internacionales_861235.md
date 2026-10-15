---
type: source
created: 2026-09-23
updated: 2026-09-23
source_file: "[[Work/1.2 Backbone Proveedores Internacionales.md]]"
tags: [backbone]
aliases: ["Proveedores Internacionales de Backbone", "Backbone Proveedores Internacionales"]
sources:
  - "[[entities/akamai]]"
  - "[[entities/cables-&-wireless]]"
  - "[[entities/sparkle]]"
  - "[[entities/claro]]"
  - "[[entities/cnt]]"
  - "[[entities/telconet]]"
  - "[[entities/arelion]]"
  - "[[entities/backbone]]"
  - "[[concepts/rfo]]"
  - "[[concepts/escalamiento]]"
  - "[[concepts/salidas-internacionales]]"
  - "[[concepts/caso-técnico]]"
  - "[[concepts/tarea-de-seguimiento]]"
  - "[[concepts/tis-id]]"
  - "[[concepts/pid]]"
  - "[[concepts/login-de-circuito]]"
contentHash: 94a-1b5086a5
generation_complete: true
---

# 1.2 Backbone Proveedores Internacionales - Resumen

## Fuente

- Archivo original: [[Work/1.2 Backbone Proveedores Internacionales.md]]
- Ingerido: 2026-09-23

## Contenido principal

Este documento reúne la información operativa de contacto y escalamiento para los proveedores internacionales de [[entities/backbone|backbone]] de [[entities/telconet|Telconet]]. Su punto de partida es el enlace a la herramienta de monitoreo NetFlow de [[concepts/salidas-internacionales|salidas internacionales]], utilizado para revisar el estado de los enlaces troncales hacia el exterior. El texto define el flujo de gestión de incidentes: **crear una [[concepts/tarea-de-seguimiento|tarea de seguimiento]] asignada al perfil del operador** y, una vez resuelto el incidente, **generar una tarea de [[concepts/rfo|RFO]]** (informe de causa de la interrupción). Además, se documentan los niveles y procedimientos de [[concepts/escalamiento|escalamiento]] de varios proveedores, entre ellos [[entities/akamai|Akamai]], [[entities/cables-&-wireless|Cables & Wireless (C&W)]], PCCW, [[entities/sparkle|Sparkle]], [[entities/claro|Claro]] y [[entities/cnt|CNT]], con sus correos y plantillas de contacto. También se detallan logins de circuito, el circuito UFINET, el Portal [[entities/arelion|Arelion]] y el nodo PE05CAR.

## Entidades clave

- [[entities/telconet|Telconet]] — operador propietario del backbone y perspectiva organizadora del documento.
- [[entities/akamai|Akamai]] — proveedor CDN; contacto `nocc-shift@akamai.com` con copia a `mmuniz@akamai.com`.
- [[entities/cables-&-wireless|Cables & Wireless (C&W)]] — niveles de escalamiento y reporte de CID.
- [[entities/sparkle|Sparkle]] — escalamiento vía Contact Center (`contactcenter.tis@tisparkle.com`).
- [[entities/claro|Claro]] — múltiples contactos de la mesa TIC (`@claro.com.ec`).
- [[entities/cnt|CNT]] — gestión por login y caso técnico sobre el ID de circuito.
- [[entities/arelion|Arelion]] — Portal de autoservicio para gestión de circuitos.

## Conceptos clave

- [[entities/backbone|Backbone]] — infraestructura troncal internacional y sus procedimientos operativos.
- [[concepts/rfo|RFO]] — informe de causa obligatorio al cerrar un incidente.
- [[concepts/escalamiento|Escalamiento]] — procedimiento de contacto y subida de nivel por proveedor.
- [[concepts/salidas-internacionales|Salidas Internacionales]] — enlaces del backbone hacia el exterior (NetFlow).
- [[concepts/caso-técnico|Caso técnico]] — mecanismo formal de escalamiento con CNT.
- [[concepts/tarea-de-seguimiento|Tarea de seguimiento]] — tarea interna para contabilizar el tiempo de resolución.
- [[concepts/tis-id|TIS-ID]] — identificador de ticket de Sparkle.
- [[concepts/pid|PID]] — referencia obligatoria al escalar con Claro.
- [[concepts/login-de-circuito|Login de circuito]] — denominación de enlace CNT sobre la que se abre el caso.

## Puntos principales

- **Flujo de gestión**: para casos de backbone se crea una tarea asignada al perfil del operador para medir el tiempo de solventación; al resolver, se crea una tarea de [[concepts/rfo|RFO]].
- El enlace de NetFlow (`aplicaciones.telconet.ec/netflow/salidasInternacionales`) es el punto de partida para diagnosticar las [[concepts/salidas-internacionales|salidas internacionales]].
- **Akamai**: reportes de nodos CDN se envían a `nocc-shift@akamai.com`, con copia a `mmuniz@akamai.com`.
- **C&W y PCCW**: niveles de escalamiento documentados mediante capturas de pantalla.
- **Sparkle**: escalamiento vía Contact Center usando plantilla con `TIS-ID`, `Start Date` y zona horaria GTM-5; número 0018669365668 (Sparkle Argentina).
- **Claro**: escalamiento mediante contactos de la mesa TIC y plantilla en español que requiere el `PID`.
- **CNT**: se debe generar un [[concepts/caso-técnico|caso técnico]] sobre el [[concepts/login-de-circuito|login]] correspondiente al ID de circuito de Telconet (`cnt-burts`, `cnt-inaquito-bogota`, `tn-cnt-salinas`, `tn-cnt-manta`).
- En el login `cnt-inaquito-bogota`, CNT reporta los IDs de Telconet y Telconet reporta los CID de C&W.
- Se registran además el circuito UFINET ECCOTEL10267004C (asociado a Edge uno), las credenciales del Portal [[entities/arelion|Arelion]] (`noc@telconet.ec`) y la referencia al nodo PE05CAR.

## Menciones en la fuente

- "solo un recordatorio de que para reportes de nodos de las regiones CDN de Akamai en Telconet la lista de contacto a utilizar es [nocc-shift@akamai.com](mailto:nocc-shift@akamai.com)." — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Adicional tambien incluir tacto: mmuniz@akamai.com" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Cables & Wireless (C&W)" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Para este login, CNT reporta los IDs de Telconet y nosotros reportamos los CID  C&W con Cables and Wireless" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "PCCW" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Niveles de Escalamiento" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- ""Contact Center" <contactcenter.tis@tisparkle.com>;" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Dear Sparkle" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "0018669365668 Sparkle Argentina" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- ""EXT TIC HTS Wilmer Vargas" <HTSWVART@claro.com.ec>;" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- ""TIC NOC" <noc@claro.com.ec>;" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Estimados Claro" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]
- "Se debe genera un ~={red}caso tecnico =~ sobre el login que corresponda de acuerdo al ID de circuito de TELCONET" — [[Work/1.2 Backbone Proveedores Internacionales|1.2 Backbone Proveedores Internacionales]]