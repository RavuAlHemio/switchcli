    {master:0}
    root@switch> configure

    {master:0}[edit]
    root@switch# set chassis aggregated-devices ethernet device-count 2

    {master:0}[edit]
    root@switch# edit interfaces ae0 unit 0 family ethernet-switching

    {master:0}[edit interfaces ae0 unit 0 family ethernet-switching]
    root@switch# set port-mode access

    {master:0}[edit interfaces ae0 unit 0 family ethernet-switching]
    root@switch# set vlan members corp

    {master:0}[edit interfaces ae0 unit 0 family ethernet-switching]
    root@switch# top edit interfaces ae1

    {master:1}[edit interfaces ae1]
    root@switch# set ae1 aggregated-ether-options lacp active

    {master:1}[edit interfaces ae1]
    root@switch# edit unit 0 family ethernet-switching

    {master:0}[edit interfaces ae1 unit 0 family ethernet-switching]
    root@switch# set port-mode trunk

    {master:0}[edit interfaces ae1 unit 0 family ethernet-switching]
    root@switch# set vlan members [ corp outside dmz ]

    {master:0}[edit interfaces ae1 unit 0 family ethernet-switching]
    root@switch# delete native-vlan-id

    {master:0}[edit interfaces ae1 unit 0 family ethernet-switching]
    root@switch# top edit interfaces

    {master:0}[edit interfaces]
    root@switch# delete ge-0/0/4 unit 0

    {master:0}[edit interfaces]
    root@switch# set ge-0/0/4 ether-options 802.3ad ae0

    {master:0}[edit interfaces]
    root@switch# delete ge-0/0/5 unit 0

    {master:0}[edit interfaces]
    root@switch# set ge-0/0/5 ether-options 802.3ad ae0

    {master:0}[edit interfaces]
    root@switch# set ae1 aggregated-ether-options lacp active

    {master:0}[edit interfaces]
    root@switch# delete ge-0/0/6 unit 0

    {master:0}[edit interfaces]
    root@switch# set ge-0/0/6 ether-options 802.3ad ae1

    {master:0}[edit interfaces]
    root@switch# delete ge-0/0/7 unit 0

    {master:0}[edit interfaces]
    root@switch# set ge-0/0/7 ether-options 802.3ad ae1

    {master:0}[edit interfaces]
    root@switch# commit
    configuration check succeeds
    commit complete

    {master:0}[edit interfaces]
    root@switch# exit
