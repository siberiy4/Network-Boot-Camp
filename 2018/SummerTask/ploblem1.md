192.168.1.0/24
PCX .2|RouterX .1
192.168.2.0/24
RouterX.1 |RouterY .2
192.168.3.0/24
RuterY .1 | PCY .2


RouterX(1841)
```
enable

configure terminal

hostname RouterX

service dhcp

ip dhcp pool hoge

network 192.168.1.0 255.255.255.0

default-router 192.168.1.1


router rip

version 2

network 192.168.1.0

network 192.168.2.0

interface fastethernet 0/0

no shutdown

ip address 192.168.1.1 255.255.255.0

interface serial 0/0/0

no shutdown

ip address 192.168.2.1 255.255.255.0




```


RouterY(1841)
```
enable

configure terminal

hostname RouterY

service dhcp

ip dhcp pool hoge

network 192.168.3.0 255.255.255.0

default-router 192.168.3.1


router rip

version 2

network 192.168.2.0

network 192.168.3.0

interface fastethernet 0/0

no shutdown

ip address 192.168.3.1 255.255.255.0

interface serial 0/0/0

no shutdown

ip address 192.168.2.2 255.255.255.0


```



