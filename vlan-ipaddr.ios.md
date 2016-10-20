    switch# configure terminal
    switch(config)# interface Vlan 131
    switch(config-if)# ip address 192.168.69.10 255.255.255.0
    switch(config-if)# exit
    switch(config)# ip default-gateway 192.168.69.1
    switch(config)# exit
    switch#
