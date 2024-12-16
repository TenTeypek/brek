scanuje 1000 nejpoužívanějších portů TCP
`-sn` nescanuje porty
`-p <port|seznam|rozsah>` scanuje určité porty
`-p-` scanuje všechny porty
`-sU` scanuje UDP, pomalé
`-sV` pokusí se rozeznat služby a verzi, pomalé

TCP relace: `syn` -> `syn`, `ack` -> `ack`
## Porty
`1-1023` - well known
	`80` - http
	`443` - https
	todo: dns port
`1024-49151` - registrované
`49152-65635` - dynamické
