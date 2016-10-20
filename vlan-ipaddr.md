# Giving the switch an IP address on a VLAN

To have the switch actively participate in traffic (e.g. store its configuration
on a server or download firmware updates), it must be assigned an IP address.
IP addresses are generally assigned per VLAN.

In this example, we assign IP address 192.168.69.10/24 (= netmask 255.255.255.0)
to VLAN 131 (`corp`) and assign 192.168.69.1 as the switch's default gateway.
