## Identificar equipo sin registrar

---
```bash
display ont autofind all
	serial
	
config

int gpon 0/1
ont confirm 3 ontid 9 --sn-auth <serial_number> omci ont-line profile-id 10 ont-srv profile-id 10 desc SITEC_ONT219

quit
```

---
## Una vez indentificado y asignado los perfiles al equipo se le debe asignar un puerto

---

```bash
service-port 219 vlan 1 gpon 0/1/3 ont 9 gemport 1 multi-service user-vlan 1

```

---


## Sitec VPN Connection

![[Pasted image 20210906131427.png]]

Password: Roberthromero1

authentication mschap2