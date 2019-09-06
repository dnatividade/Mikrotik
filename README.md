# Mikrotik
Mikrotik tutorials and scripts

### Mikrotik fasttrack connection
```
/ip firewall filter add chain=forward action=fasttrack-connection connection-state=established,related
/ip firewall filter add chain=forward action=accept connection-state=established,related
```
