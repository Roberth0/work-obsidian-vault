#huawei

```bash
enable
config 

snmp-agent sys-info version 1
snmp-agent community read public

undo system snmp-user password security
```

___
OID for get stats
https://ixnfo.com/en/oid-and-mib-for-huawei-olt-and-onu.html
https://ixnfo.com/en/snmp-oid-and-mib-for-interfaces.html

---

```bash
snmp-agent sys-info
	version
	v2c

snmp-agent community 
	read
	public

snmp-agent community write private
```

If your gonna used trapps use the following comands:
```bash
snmp-agent target-host
	trap-paramsname
	huaweiNMS
	v2c
	securityname
	private
snmp-agent target-host
	trap-hostname
	<hostname>
	address
	<ip server address>
	trap-paramsname
	huaweiNMS
	
snmp-agent trap enable standard

# snmp-agent trap source
#	meth
#	0
```


```bash
snmpwalk -v2c -c <communityStream> <targetIP>
```


Add clients [[Add new client OLT]]