Nejdřiv vlany na switchi:
![[VLAN#Založení vlan]]
![[VLAN#Přidání access switchportu do vlany]]
Povolení vlan pro router (na switchi):
![[VLAN#Povolení vlan na trunk switchportu]]

Na routeru zapnu interface:
```
interface <interface>
no shutdown
exit
```
Pak založím subinterface pro každou vlanu:
```
interface <interface>.<cislo-subinterface>
encapsulation dot1Q <cislo-subinterface>
ip address <ip-routeru> <maska>
exit
```
Příklad: 
```
interface GigabitEthernet 0/0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
exit
```

Když chci [[DHCP]] tak na router
