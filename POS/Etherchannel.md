[[VLAN]]
# Přidání interfaců do channel-group
```
interface range <interface> <range>
channel-group 1 mode on
exit
```
# Nastavení port-channelu
*`interface`* - port-channel 1
![[VLAN#Povolení vlan na trunk switchportu]]

> [!important]
> Na L3 switchi nepůjde nastavit trunk než udělám tohle: (v interface port-channel)
> ```
> switchport trunk encapsulation dot1q
> ```