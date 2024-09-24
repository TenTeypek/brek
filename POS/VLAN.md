 > [!info]
> Vlany by měly být založeny ve všech zařízeních kde budou protékat
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