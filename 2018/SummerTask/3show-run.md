syanai#show run
Building configuration...

Current configuration : 1374 bytes
!
! Last configuration change at 10:21:50 UTC Mon Aug 27 2018
!
version 15.5
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname RouterZ
!
boot-start-marker
boot-end-marker
!
!
!
no aaa new-model
ethernet lmi ce
!
!
!
!
!
!
!
!
ip cef
no ipv6 cef
!
!
license udi pid C841M-4X-JSEC/K9 sn FGL213690P4
!
!
!
redundancy
!
!
!
!
!
!
!
!
!
!
!
!
!
!
interface GigabitEthernet0/0
 no ip address
!
interface GigabitEthernet0/1
 no ip address
!
interface GigabitEthernet0/2
 no ip address
!
interface GigabitEthernet0/3
 no ip address
!
interface GigabitEthernet0/4
 ip address 192.168.0.1 255.255.255.0
 ip nat inside
 ip virtual-reassembly in
 duplex auto
 speed auto
!
interface GigabitEthernet0/5
 ip address 201.1.1.2 255.255.255.252
 ip nat outside
 ip virtual-reassembly in
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
!
router rip
 version 2
 network 200.2.2.0
 network 201.1.1.0
 default-information originate
 no auto-summary
!
ip forward-protocol nd
no ip http server
no ip http secure-server
!
!
ip nat pool nbc 200.2.2.1 200.2.2.254 prefix-length 24
ip nat inside source list 1 pool nbc overload
!
!
!
access-list 1 permit 192.168.0.0 0.0.0.255
access-list 1 permit any
!
 vstack
!
line con 0
 no modem enable
line vty 0 4
 login
 transport input none
!
scheduler allocate 20000 1000
!
end














ISP-2#show run
Building configuration...

Current configuration : 1086 bytes
!
! Last configuration change at 09:46:19 UTC Mon Aug 27 2018
!
version 15.5
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname ISP-2
!
boot-start-marker
boot-end-marker
!
!
!
no aaa new-model
ethernet lmi ce
!
!
!
!
!
!
!
!
ip cef
no ipv6 cef
!
!
license udi pid C841M-4X-JSEC/K9 sn FGL202920X1
!
!
!
redundancy
!
!
!
!
!
!
!
!
!
!
!
!
!
!
interface GigabitEthernet0/0
 no ip address
!
interface GigabitEthernet0/1
 no ip address
!
interface GigabitEthernet0/2
 no ip address
!
interface GigabitEthernet0/3
 no ip address
!
interface GigabitEthernet0/4
 ip address 201.1.1.1 255.255.255.252
 duplex auto
 speed auto
!
interface GigabitEthernet0/5
 ip address 10.0.0.2 255.255.255.0
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
!
router rip
 version 2
 network 10.0.0.0
 network 201.1.1.0
 no auto-summary
!
ip forward-protocol nd
no ip http server
no ip http secure-server
!
!
!
!
!
!
 vstack
!
line con 0
 no modem enable
line vty 0 4
 login
 transport input none
!
scheduler allocate 20000 1000
!
end

ISP-2#show run
Building configuration...

Current configuration : 1086 bytes
!
! Last configuration change at 09:46:19 UTC Mon Aug 27 2018
!
version 15.5
service timestamps debug datetime msec
service timestamps log datetime msec
no service password-encryption
!
hostname ISP-2
!
boot-start-marker
boot-end-marker
!
!
!
no aaa new-model
ethernet lmi ce
!
!
!
!
!
!
!
!
ip cef
no ipv6 cef
!
!
license udi pid C841M-4X-JSEC/K9 sn FGL202920X1
!
!
!
redundancy
!
!
!
!
!
!
!
!
!
!
!
!
!
!
interface GigabitEthernet0/0
 no ip address
!
interface GigabitEthernet0/1
 no ip address
!
interface GigabitEthernet0/2
 no ip address
!
interface GigabitEthernet0/3
 no ip address
!
interface GigabitEthernet0/4
 ip address 201.1.1.1 255.255.255.252
 duplex auto
 speed auto
!
interface GigabitEthernet0/5
 ip address 10.0.0.2 255.255.255.0
 duplex auto
 speed auto
!
interface Vlan1
 no ip address
!
router rip
 version 2
 network 10.0.0.0
 network 201.1.1.0
 no auto-summary
!
ip forward-protocol nd
no ip http server
no ip http secure-server
!
!
!
!
!
!
 vstack
!
line con 0
 no modem enable
line vty 0 4
 login
 transport input none
!
scheduler allocate 20000 1000
!
end




