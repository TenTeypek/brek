# ARP Poisoning
ARP protokol -> ARP tabulka obsahuje IP k MAC adresám (`arp -a`)
Útočník se vydává za jiné zařízení

# DHCP Spoofing
Můžu využít např. na změnu DNS
## DHCP Starving
Vyžeru všechny IP na původním DHCP serveru, aby se klienti připojili na můj server
## DHCP Snooping
Obrana proti [[#DHCP Spoofing]]
```
ip dhcp snooping
interface <trustovane-zarizeni>
ip dhcp snooping trust
```

# VLAN Hopping
TODO: doplň

# VLAN Double tagging
TODO: doplň



```
switchport trunk native vlan 666
```