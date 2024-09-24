```
hostname SW_1
ip domain-name cisco.com
ip default-gateway 192.168.1.5
enable secret cisco
username cisco secret cisco
banner motd "Zakaz vstupu"
line console 0
login local
exit
line vty 0 15
login local
transport input ssh
exit
crypto key generate rsa
1024
interface vlan 1
ip address 192.168.1.10 255.255.255.0
no shutdown
exit
```