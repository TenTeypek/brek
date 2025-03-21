## První router
```
router ospf 10
router-id 1.1.1.1
network <id-prvni-site> 0.0.0.255 area 0
network <id-size-mezi> 0.0.0.255 area 0
```
## Druhý router
```
router ospf 10
router-id 2.2.2.2
network <id-druhe-site> 0.0.0.255 area 0
network <id-site-mezi> 0.0.0.255 area 0
```

`default-information originate` - distrubuuje defaultní routu (do config-router)
`ip route 0.0.0.0 0.0.0.0 <ip-routeru-isp>` - všechno co nezná pujde na router ISP