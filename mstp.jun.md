    switch# configure terminal
    switch(config)# spanning-tree mode mst

    {master:0}
    root@switch> configure

    {master:0}[edit]
    root@switch# delete protocols mstp disable

    {master:0}[edit]
    root@switch# commit
    configuration check succeeds
    commit complete

    {master:0}[edit]
    root@switch# quit

    {master:0}
    root@switch>
