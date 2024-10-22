 > [!info]
> Vlany by měly být založeny ve všech zařízeních kde budou protékat

> [!caution]
> Na router se vlan nezakládá - používáme [[#Subinterface pro vlan na router|subinterface]]
# Založení vlan
```
vlan <cislo>
name <name>
exit
```
# Přidání access switchportu do vlany
```
interface <interface>
switchport mode access
switchport access vlan <cislo>
exit
```
# Povolení vlan na trunk switchportu
```
interface <interface>
switchport mode trunk
switchport trunk allowed vlan <cislo>[,<cislo>]...
exit
```
# Subinterface pro vlan na router
```
interface <interface>
no shutdown
exit

interface <interface>.<cislo-vlan>
encapsulation dot1Q <cislo-vlan>
ip address <ip-routeru> <maska>
exit