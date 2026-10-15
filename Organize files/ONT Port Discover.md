```bash
enable
config
interface gpon 0/1
```
```bash
display ont optical-info 15 all
```

## Add ONT

```bash
#ont add [pon] [id] sn-auth [serial] snmp ont-lineprofile-id [vlan] desc [DESCRIPTION]
```
```bash
ont add 15 33 sn-auth 48575443DED4889E snmp ont-lineprofile-id 150 desc SITEC_ONT600
```


```bash
#service-port [port] vlan [vlan] gpon 0/1/[pon] ont [id] gemport 150 multi-service user-vlan [150]
```

```bash
service-port 600 vlan 150 gpon 0/1/15 ont 33 gemport 150 multi-service user-vlan 150
```

```
display ont info by-sn 48575443DED4889E
```