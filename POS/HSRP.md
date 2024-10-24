Na oba routery ipiny.
Na obou routerech:
```
interface <interface>
standby 1 ip <virtualni-ip-redundantni-gatewaye>
standby 1 priority <priorita>
standby 1 preempt
exit
```
*`priorita`* - většinou 150 a 100
`preempt` - přebírá zpět
Máme 2 sítě takže i standby 2
Zobrazení - `show standby` (v enablu)
