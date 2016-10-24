    {master:0}
    root@switch> configure

    {master:0}[edit]
    root@switch# set vlans corp vlan-id 131

    {master:0}[edit]
    root@switch# set vlans outside vlan-id 242

    {master:0}[edit]
    root@switch# set vlans dmz vlan-id 464

    {master:0}[edit]
    root@switch# set vlans test vlan-id 353

    {master:0}[edit]
    root@switch# commit
    configuration check succeeds
    commit complete

    {master:0}[edit]
    root@switch# delete vlans test

    {master:0}[edit]
    root@switch# commit
    configuration check succeeds
    commit complete

    {master:0}[edit]
    root@switch# exit

    {master:0}
    root@switch>
