
- reference: https://www.voip-info.org/asterisk-agi/

You can pass arguments via:

```
AGI(script.agi, arg1, arg2, …)
```

for php scripts you could retrieve the arguments like: 

```php
$argv[1]
$argv[2]
```

The file in you have to include the config via issabel/elastic/freepbx is *extensions_custom.conf*


```
exten => 5679,1,Answer
exten => 5679,n,Wait(1)
exten => 5679,n,Set(TIMEOUT_LOOPCOUNT=0)
exten => 5679,n(start),Set(TIMEOUT(digit)=3)
exten => 5679,n,WaitExten(1,)
exten => 5679,n,Read(numero,custom/atencion,,,,) ;solicito numero de atencion
exten => 5679,n,NoOp(${numero})
exten => 5679,n,AGI(retrieveData.php,${numero}) ; envió el numero al AGI para ser consultado
exten => 5679,n,NoOp(${RESPUESTA}) ;variable que uso para recibir la respuesta del agi.
exten => 5679,n,GotoIf($["${RESPUESTA}" = "0"]?nexist) ; comparo la respuesta devuelta por el AGI
exten => 5679,n,Goto(ext-group,601,1) ; si no es igual a cero se ejecuta esta instrucción
exten => 5679,n(nexist),Playback(custom/noexiste) ;si es igual a cero se ejecuta esta instrucción
exten => 5679,n,Set(TIMEOUT_LOOPCOUNT=$[${TIMEOUT_LOOPCOUNT}+1])
exten => 5679,n,GotoIf($[${TIMEOUT_LOOPCOUNT} > 4]?final)
exten => 5679,n,Goto(5679,start) ; vuelve al inicio de ser menor a 4 los intentos
exten => 5679,n(final),Playback(vm-goodbye)
exten => 5679,n,Goto(app-blackhole,hangup,1)
```


### Credenciales maquina virtual vmware: 

*admin:12*

Iniciar asterisk cli: 
```
asterisk -r
```

- [I] Para ver en detalle la ejecución del AGI, activamos en el CLI

```
agi set debug on
```


- Directorio donde se guardan los archivos del AGI 
	/var/lib/asterisk/agi-bin/

- Start asterisk cli in verbose mode 
```
asterisk -vvvvvr 
```
![[Pasted image 20250910192958.png]]


### Sound directory 

```
/var/lib/asterisk/sounds/
```

### Enabling TTS Engines

TTS -> Text to Speech
Options: 
	- Festival
	- Flite
	- Google/AWS/etc

#### Flite

```
yum install flite
```

load module to `/etc/asterisk/modules.conf`and add `load => app_flite.so`


### TTS GOOGLE
free tier - 4 million characters per month

### ssh user@vps

-L local:80:remoto:80
-R remoto:80:local:80


enable GatewayPorts on sshd configuration
