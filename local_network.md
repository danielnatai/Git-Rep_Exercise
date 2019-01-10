Here is configs done in our Local gateway
#int g0/0
int#ip add 172.16.15.1 255.255.255.0
Local Subnet 172.16.15.0
Subnet Mask /24

ip dhcp pool LAN
network 172.16.15.0
default router 172.16.15.1
ip dhcp excluded-address 172.16.15.1 172.16.15.20

Add VLAN
Vlan 20
vlan name Operation
ip add 172.16.16.1 255.255.255.0

ip dhcp pool OPERATION
network 172.16.16.0
default router 172.16.16.1
ip dhcp excluded-address 172.16.16.1 172.16.16.20
