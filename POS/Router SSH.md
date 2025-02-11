```
hostname RT_1
ip domain-name cisco.com
enable secret cisco
username cisco secret cisco
interface g0/0/0
ip address 192.168.0.1 255.255.255.0
no shutdown
exit
interface g0/0/1
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
line console 0
login local
exit
line vty 0 15
login local
transport input ssh
exit
crypto key generate rsa
1024
ip ssh version 2
```