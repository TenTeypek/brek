```
access-list <cislo> { permit | deny } <typ-protokolu> <ip> [host <ip-hosta>] [eq <port>]
```
`cislo` - používáme 100-199 - extended access list
`typ-protokolu` - `tcp`, `icmp`, `ip` pro vsechno, ...
`ip` - ip koho omezuju nebo `any`
`ip-hosta` - ip kam omezuju přístup
`port` - číslo portu nebo `www`, `ftp`, `telnet`, ...

> [!info]
> `deny` má přednost před `permit`

Příklad: 
```
access-list 101 permit tcp any host 192.168.20.254 eq www
access-list 101 deny ip any host 192.168.20254
access-list 101 permit ip any any
```
zakáže přístup k zařízení přes všechny porty kromě http (80)

## Nastavení access-listu na interface
Na interface směrem k "zákazníkům" které omezuju (ne k serveru):
```
ip access-group <cislo> in
```
