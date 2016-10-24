# Link Aggregation

Switches allow links to be "tied" together to provide failover and/or increase
throughput. These are known as aggregation groups, trunks, channels, bonds,
teams, bundles and by other names, depending on the vendor's preference. This
document shall refer to them as "aggregated links".

In this example, the following aggregated links are created:
* The fifth and sixth Gigabit Ethernet port are aggregated statically and
  transmit untagged traffic in the `corp` VLAN (131).
* The seventh and eighth Gigabit Ethernet port and aggregated using LACP and
  transmit tagged traffic in the `corp` (131), `outside` (242) and `dmz` (464)
  VLANs.
