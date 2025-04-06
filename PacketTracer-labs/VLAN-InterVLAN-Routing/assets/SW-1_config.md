! Switch hostname
hostname SW-1

! Spanning Tree Protocol
spanning-tree mode pvst
spanning-tree extend system-id

! VLAN assignment
interface FastEthernet0/1
 switchport access vlan 10
 switchport mode access

interface FastEthernet0/2
 switchport access vlan 10
 switchport mode access

interface FastEthernet0/3
 switchport access vlan 20
 switchport mode access

interface FastEthernet0/4
 switchport access vlan 20
 switchport mode access

! Trunk port to Router
interface GigabitEthernet0/2
 switchport trunk allowed vlan 10,20
 switchport mode trunk
