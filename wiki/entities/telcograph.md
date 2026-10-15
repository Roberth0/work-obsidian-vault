---
type: entity
created: 2026-09-23
updated: 2026-09-23
generation_complete: true
sources:
  - "[[sources/4-cedia_d7cef1]]"
  - "[[sources/4-1-telcograph_4a563a]]"
tags:
  - "organization"
aliases:
  - "Telcograph Clientes"
---

# Telcograph

## Descripción

Telcograph es una plataforma de monitoreo y gestión de red utilizada por [[Telconet]] para dar seguimiento a clientes y a los enlaces asociados a cada uno de ellos. Dentro del flujo operativo documentado, Telcograph aparece vinculada al dashboard de backbone, por lo que funciona como punto de consulta del estado de la infraestructura y de los servicios contratados. El documento dedica una sección específica al cambio de usuario en Telcograph: para efectuarlo es necesario registrar el nuevo correo como contacto técnico en [[Telcos]], tanto en la figura de contacto cliente como en la de contacto punto. Adicionalmente, se incluyen credenciales de acceso a la instancia **Telcograph Clientes**, cuyo usuario corresponde a `noc`, lo que evidencia su uso compartido por parte del equipo de operaciones. Su aplicación se extiende a la gestión de casos de clientes corporativos como [[Cedia|CEDIA]], donde el seguimiento de enlaces resulta crítico. En conjunto, Telcograph se posiciona como una de las herramientas operativas centrales del rol que la emplea.

En el plano operativo, Telcograph figura como un cliente cuyo volumen supera las 500M, por lo que el documento abre con la advertencia ">[!warning] Cliente supera las 500M, se debe cambiar de plantilla a; ### Union de Razones Sociales". La gestión de este cliente implica precisamente la **Unión de Razones Sociales**: cancelar los puntos de la razón social antigua en *Informacion recibida de sistemas*, actualizar los datos de SERVER IP, Name ZG ORG e ID Grafana en *Razones sociales* y crear los nuevos puntos con los cambios aplicados. Asimismo, el *Ingresos de APs (Hasta 5)* se realiza con la IP de ingreso 172.24.27.27 y los datos requeridos (AP, login auxiliar, nombre en la controladora, MAC e IP de controladora), cambiando el hostname a login/mac y actualizando las MACROS; si la controladora es RUCKUS debe agregarse "6." adelante, además de verificarse el grupo y realizarse la modificación en la sección inventory (Host Router y Name).
## Entidades relacionadas

- [[entities/telcos|Telcos]]
- [[entities/4-cedia|CEDIA]]
- [[entities/telconet|Telconet]]
- [[entities/ruckus|RUCKUS]]

## Conceptos relacionados

- [[concepts/vpn|VPN]]
- [[concepts/union-de-razones-sociales|Union de Razones Sociales]]
- [[concepts/ingresos-de-aps|Ingresos de APs]]
- [[concepts/macros|MACROS]]

## Menciones en la fuente

- "### Cambio de usuario telcograph" — [[Work/4 Cedia|4 Cedia]]
- "El nuevo correo debe estar registrado como contacto tecnio en telcos, desde el menu comercial, tanto como *contacto cliente* y *contacto punto*" — [[Work/4 Cedia|4 Cedia]]
- "- Telcograph Clientes
	- noc // VCzrk"kUr3xMH~E10" — [[Work/4 Cedia|4 Cedia]]