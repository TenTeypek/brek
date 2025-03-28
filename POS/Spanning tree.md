Nastavuje se pro VLANy
```
spanning-tree vlan <cislo> root { primary | secondary }
```

Na porty koncových zařízení, aby se tam zbytečně nevysílalo STP:
```
spanning-tree portfast
spanning-tree bpduguard enable
```
