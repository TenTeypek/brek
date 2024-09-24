Nejdřiv všude ipiny
Na obou routerech: (v configu)
```
interface <interface>
ip address <ip> 255.255.255.0
no shutdown
exit
```
na obou routerech: (v configu)
```
interface <interface>
standby 1 ip <virtualni-ip-redundantni-gatewaye>
standby 1 priority <priorita>
standby 1 preempt
exit
```
*priorita* - většinou 150 a 100
*preempt* - přebírá zpět
když máme 2 sítě takže i standby 2
zobrazení - `show standby` (v enablu)
