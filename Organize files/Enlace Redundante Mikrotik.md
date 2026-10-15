Primero se debe configurar la direccion IP de red en la interfaz para ello se le asigna un nombre asumeinto que se utilizara la interfaz ether10

```bash
/interface ethernet set [ find default-name=ether10 ] name=WAN2
/ip address add address=10.10.10.1/28 interface=WAN2 network=10.10.10.0
```

Posteriormente se configura la direccion IP asignada por el proveedor para el ejempo se utiliza la direccion 10.10.10.1.



Se debe habilitar el nateo a traves de dicha interfaz en la configuracion del firewall

```bash
/ip firewall nat add action=masquerade chain=srcnat out-interface=WAN2
```

Posteriormente se configura el balanceo de cargas a traves de las  interfaces para no desperdiciar el ancho de banda mientras las dos proveedores esten activos.

```bash
/ip firewall mangle
add action=mark-connection chain=input in-interface=WAN1 new-connection-mark=WAN1_conn
add action=mark-connection chain=input in-interface=WAN2 new-connection-mark=WAN2_conn

add action=mark-routing chain=ouput connection-mark=WAN1_CONN new-routing-mark=to_WAN1
add action=mark-routing chain=ouput connection-mark=WAN2_CONN new-routing-mark=to_WAN2

add chain=prerouting dst-address=192.168.10.0/24 in-interface=LAN
add chain=prerouting dst-address=192.168.0.0/24 in-interface=LAN

add action=mark-connection chain=prerouting dst-address-type=!local in-interface=LAN new-connection-mark=WAN1_conn per-connection-classifier=both-addresses:2/0

add action=mark-connection chain=prerouting dst-address-type=!local in-interface=LAN new-connection-mark=WAN2_conn per-connection-classifier=both-addresses:2/1

add action=mark-routing chain=prerouting connection-mark=WAN1_conn in-interface=LAN new-routing-mark=to_WAN1
add action=mark-routing chain=prerouting connection-mark=WAN2_conn in-interface=LAN new-routing-mark=to_WAN2
```

Una vez configurado el balanceo de cargas se establece el fail-over que se ejecuta en base a la condicion de los enlaces WAN para poder redireccionar el trafico en caso de que uno de los dos enlaces se caiga.


```bash 
/ip route
add check-gateway=ping distance=1 dst-address=10.0.0.1/32 gateway=8.8.8.8 scope=10
add check-gateway=ping distance=1 dst-address=10.0.0.2/32 gateway=8.8.4.4 scope=10

add check-gateway=ping distance=1 gateway=8.8.8.8 routing-mark=to_WAN1
add check-gateway=ping distance=2 gateway=8.8.4.4 routing-mark=to_WAN2

add distance=1 gateway=10.0.0.1 routing-mark=to_WAN1
add distance=2 gateway=10.0.0.2 routing-mark=to_WAN2

add distance=1 gateway=10.0.0.1
add distance=2 gateway=10.0.0.2

add distance=1 dst-address=8.8.4.4/32 gateway=<IPWAN1> scope=10
add distance=1 dst-address=8.8.8.8/32 gateway=<IPWAN2> scope=10



```