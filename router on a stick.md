když dělam router on a sticc tak nejdřiv na switchi založim vlany

pak zalozim subinterface na routeru:
```
interface <interface>.<cislo-subinterface>
encapsulation dot1Q <cislo-subinterface>
ip address <ip-routeru> <mask>
exit
```
příklad: 
```
interface GigabitEthernet 0/0/0.10
encapsulation dot1Q 10
ip address 192.168.10.1 255.255.255.0
exit
```

kdyz chci dhcp tak ho najebu na router
