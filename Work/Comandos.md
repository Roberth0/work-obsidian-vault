


# BGP
```
display bgp vpnv4 vpn-instance telconet peer 63.222.78.13 verbose

```

![[Pasted image 20240930185637.png]]

# STP

Ver hace cuanto tiempo se produjo un cambio de topologia
```
show spanning-tree detail
```




![[Pasted image 20240930182550.png]]


![[Pasted image 20241202111918.png]]


<rointernetgye1h>display interface 100GE4/0/14 | i esc  
Description: PCCW/100GIGA/CIRION_SID_81-5569V0E-CRM500361398/PCCW-SR233574/PIT  
<rointernetgye1h>  
  
<rointernetgye1h>display interface 100GE4/0/14 | inc Rx  
Rx Warning range: [-13.001,  3.999]dBm, Tx Warning range: [-4.000,  3.999]dBm  
Rx0 Power:  -4.13dBm, Tx0 Power:   1.64dBm  
Rx1 Power:  -4.79dBm, Tx1 Power:   2.13dBm  
Rx2 Power:  -5.06dBm, Tx2 Power:   1.62dBm




```
disp ip routing-table vpn-instance telconet 0.0.0.0 0
```