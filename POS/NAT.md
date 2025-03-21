# Statická NAT
```
interface <vnitrni>
ip nat inside
exit
interface <vnejsi>
ip nat outside
exit

ip nat inside source static <lokalni-ip-zarizeni> <verejna-ip-zarizeni>
```

# Dynamická NAT
## Router u serveru
[[#Statická NAT]]
## Router u počítače
```
interface <vnitrni>
ip nat inside
exit
interface <vnejsi>
ip nat outside
exit

ip nat pool <nazev-poolu> <vnejsi-rozsah-min> <vnejsi-rozsah-max> netmask 255.255.255.0
access-list 1 permit <vnitrni-id> 0.0.0.255
ip nat inside source list 1 pool <nazev-poolu>
```

# PAT
## Router u serveru
[[#Statická NAT]]
## Router u počítače
```
interface <vnitrni>
ip nat inside
exit
interface <vnejsi>
ip nat outside
exit

access-list 1 permit <vnitrni-id> 0.0.0.255
ip nat inside source list 1 interface <vnejsi> overload
```

`access-list 1 permit any` - povolí vše co přijde do NATky