    {master:0}
    root@switch> configure

    {master:0}[edit]
    root@switch# edit interfaces ge-0/0/0 unit 0 family ethernet-switching

    {master:0}[edit interfaces ge-0/0/0 unit 0 family ethernet-switching]
    root@switch# set port-mode access

    {master:0}[edit interfaces ge-0/0/0 unit 0 family ethernet-switching]
    root@switch# set vlan members corp

    {master:0}[edit interfaces ge-0/0/0 unit 0 family ethernet-switching]
    root@switch# top

    {master:0}[edit]
    root@switch# edit interfaces ge-0/0/1 unit 0 family ethernet-switching

    {master:0}[edit interfaces ge-0/0/1 unit 0 family ethernet-switching]
    root@switch# set port-mode trunk

    {master:0}[edit interfaces ge-0/0/1 unit 0 family ethernet-switching]
    root@switch# set vlan members corp

    {master:0}[edit interfaces ge-0/0/1 unit 0 family ethernet-switching]
    root@switch# set vlan members outside

    {master:0}[edit interfaces ge-0/0/1 unit 0 family ethernet-switching]
    root@switch# top

    {master:0}[edit]
    root@switch# edit interfaces ge-0/0/2 unit 0 family ethernet-switching

    {master:0}[edit interfaces ge-0/0/2 unit 0 family ethernet-switching]
    root@switch# set port-mode trunk

    {master:0}[edit interfaces ge-0/0/2 unit 0 family ethernet-switching]
    root@switch# set vlan members corp

    {master:0}[edit interfaces ge-0/0/2 unit 0 family ethernet-switching]
    root@switch# set vlan members outside

    {master:0}[edit interfaces ge-0/0/2 unit 0 family ethernet-switching]
    root@switch# set native-vlan-id dmz

    {master:0}[edit interfaces ge-0/0/2 unit 0 family ethernet-switching]
    root@switch# commit
    configuration check succeeds
    commit complete

    {master:0}[edit interfaces ge-0/0/2 unit 0 family ethernet-switching]
    root@switch# quit

    {master:0}[edit]
    root@switch# quit

    {master:0}
    root@switch>
