    switch# configure
    switch(config)# vlan 131
    switch(vlan-131)# ip address 192.168.69.10 255.255.255.0
    switch(vlan-131)# exit
    switch(config)# ip default-gateway 192.168.69.1
    switch(config)# exit
    switch#
