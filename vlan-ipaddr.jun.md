    {master:0}
    root@switch> configure

    {master:0}[edit]
    root@switch# set vlans corp l3-interface vlan.131

    {master:0}[edit]
    root@switch# set interfaces vlan unit 131 family inet address 192.168.69.10/24

    {master:0}[edit]
    root@switch# commit
    configuration check succeeds
    commit complete

    {master:0}[edit]
    root@switch# exit

    {master:0}
    root@switch>
