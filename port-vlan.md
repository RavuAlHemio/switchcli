# Assigning VLANs to ports

Most modern managed switches work in terms of VLANs, which means a switch port
is always assigned to a VLAN. To emulate the configuration of an unmanaged
switch, all ports can be assigned to the same VLAN.

With regard to VLANs, switch traffic can be either tagged or untagged. Tagged
traffic contains a header (generally according to IEEE 802.1Q) identifying the
VLAN to which the traffic belongs. Untagged traffic does not contain such a
header and it is up to the switch to decide the VLAN to which it belongs.

In this example, we activate tagging according to IEEE 802.1Q and assign the
following:
* First gigabit port: untagged traffic belongs to VLAN 131, tagged traffic is
  dropped.
* Second gigabit port: tagged traffic from VLANs 131 and 242 belongs to these
  VLANs, tagged traffic from other VLANs and untagged traffic are dropped.
* Third gigabit port: tagged traffic from VLANs 131 and 242 belongs to these
  VLANs, tagged traffic from other VLANs is dropped, untagged traffic belongs to
  VLAN 464 (and will not be tagged).
