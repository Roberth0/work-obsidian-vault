---
links:
  - "[[4.1 Telcograph]]"
tags:
  - cedia
---

En este rol se debe aceptar y resolver las tareas que llegan hacia los jefes de areas
- UIO  **Julia Marchan**
- GYE  **Edson Hidalgo**



# Informe Ejecutivo 

Se debe verificar que el informe este bien redactado, se realiza informe ejecutivo cuando ahi una caida de equipo.

>[!tip] Si el informe es por caso interurbano la hora de finalizacion es la hora en la cual los clientes (nedetel, xtrim, claro, etc) afectados validan operatividad

Se debe abrir el caso en Telcos y verificar el seguimiento de las tareas y los campos del informe

- [ ] Verificar datos del informe en base a los siguientes campos

	**Cliente Afectado:** Clientes que dependen del equipo sw1zapallochone 
	**Servicios Afectados:** Internet y Datos
	**Fecha y hora de Inicio:** Hora de apertura del caso (No modificar)
	**Fecha y hora de finalizacion:** Verificar hora de subida del equipo mediante resolucion de alarma en el zabbix
	**NO. Casos/ Tareas:** Caso y tareas generadas (No modificar)
	**Departamento Asignado:** Electrico (Ingresar departamento que solvento)
	**Analisis del problema:** Ingresar detalles del problema ocurrido
	**Acciones correctivas:** Ingresar detalles de la solucion presentada(Buscar informacion en el seguimiento de las tareas)
	**Plan de mejoramiento:** Ingresar posible optimizacion a la solucion/ Si no aplica dejar en blanco
	**Status Actual:** Operativo

- [ ] Descargar PDF Generado del informe
- [ ] Finalizar tarea con:
	Se adjunta informe corregido

Ejemplos Informes
![[Pasted image 20241003145305.png|300]]
![[Pasted image 20241003145327.png|300]]

### SAM CLIENT

Para acceder al SAM CLIENT se debe conectarse a la VPN de Cedia con las siguientes credenciales

Usuario: `JuanGonzalez`
Password:  `Amazonas20mZs9DH`

Nuevas Credenciales 
NOKIA. USER: SoporteTelconet // PASS: `C3d1@Tn$$N0k!@25`


- CheckPoint VPN
	- UserTelco // Alfa.Beta$
- Telcograph Clientes
	- noc // VCzrk"kUr3xMH~E10


---

ESCRITORIOS REMOTOS----------
#Credenciales Fiberhome
IP: 10.18.1.253
Acceso al servidor:
usuario: FIBERHOMEBK\NOCGYE
Clave: nocgye2021  luego Nocgye2021



### CASO CEDIA
Grupos donde se reporta: BB y OTN 

indoamerica-ambato-i
RE: [CEDIA #2405210041] Revisión interfaz con errores	

Estimados buenas tardes, por notificar: 

PROBLEMA: Cedia: ERRORES EN EL ENLACE : PE-AMB-SDH-1 - Interface 1/1/4(to_CPE-AMB-UTI_MS2-1)	
EQUIPOS BACKBONE AFECTADOS: NINGUNO
SERVICIOS AFECTADOS: NINGUNO
CASO ASIGNADO: 20240521-1184		
DEPARTAMENTO ESCALADO: TS AMBATO // @Herrera
TIEMPO ESTIMADO DE SOLUCIÓN: Se asignara personal.





### Verificar Informacion
ii. En el método de autenticación seleccionamos “Username and Password”
3. Para conectarse a la VPN usaremos como usuario: userTelco y como contraseña Telc0VPN


User: AlexFranco
Pass: Moldavia208zWHnE

------CEDIA
dar prioridad a alarmas link loss.

1) Entrar al SAM, buscar los extremos que correspondan al enlace reportado
3) Entrar a los extremos para verificar, empezar por el Concentrador de Ambato
4) Verificar cuantos enlaces tiene, para determinar que realizar

show lag description | match UNIANDES

5) Verificar tiempo en el que se cayo

show port 2/3/2 | match tate



9) Enviar a CEDIA que nos otorgue permisos para la revision del enlace de la red CEDIA / Nokia,
e indicar que esta afectado 1de2 enlaces por lo cual para este caso no hay afectacion de servicios

----------------------------------------------------------------------------------------
rca-uio.telconet.ec   172.24.26.15 NO VALE
telcos.telconet.ec,   172.24.15.70
admin.cisco.telconet.ec, aaaa.telconet.ec, bitacora.telconet.ec   172.24.4.228 
sisred.telconet.net   172.24.4.63 
telcodrive.telconet.net  172.24.5.141
backbonenoc.telconet.ec 172.24.5.126 NO VALE


Route DELETE -p 172.24.15.70 MASK 255.255.255.255  192.168.150.1

Route ADD -p 172.24.5.141 MASK 255.255.255.255  192.168.150.1

#### Ingreso monitoreo OLT

Se debe ingresar en el zabbix de Backbone y en el siguiente dashboard https://monitoreorda.telconet.ec/zabbix/

*Actualmente el ingreso es automatico una vez se ingrese en el dashboard de backbone*

### Cambio de usuario telcograph
El nuevo correo debe estar registrado como contacto tecnio en telcos, desde el menu comercial, tanto como *contacto cliente* y *contacto punto*

![[Pasted image 20250804094233.png|500]]

### Cambio de correo notificacon proactivo

Se debe verificar a que grupo pertence el host en cuestion 

![[Pasted image 20250804104313.png]]

Con el nombre del grupo se debe ingresar en la seccion Administracion del zabbix => Usuarios y buscar el alias de *notificaciones(a-z)* 

![[Pasted image 20250804105216.png]]

alli se abre una nueva subseccion en la cual se selecciona Media, aqui se debe buscar el nombre del grupo obtenido previamente y editar con el nuevo correo.

![[Pasted image 20250804105456.png]]

### Ingreso de monitoreo desde cero en zabbix 
1 crear el nuevo grupo
2 crear el MEDIA TYPE (clonar o new)  
3 crear  el ACTION (clonar o new) en la primera parte se  le añade el host group y en la segunda se le añade en (Update operations
) el media  types

4 vamos a Administracion / Users del zabbix y en el user  de notificacion (el segundo notificaciones2) abrimos y añadimos  el correo del cliente y guardamos.



![[Pasted image 20251217120833.png]]


