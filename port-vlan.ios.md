    switch# configure terminal
    switch(config)# interface GigabitEthernet 0/1
    switch(config-if)# switchport mode access
    switch(config-if)# switchport access vlan 131
    switch(config-if)# exit
    switch(config) interface GigabitEthernet 0/2
    switch(config-if)# switchport mode trunk
    switch(config-if)# switchport trunk allowed vlan 131,242
    switch(config-if)# exit
    switch(config) interface GigabitEthernet 0/3
    switch(config-if)# switchport mode trunk
    switch(config-if)# switchport trunk allowed vlan 131,242
    switch(config-if)# switchport trunk native vlan 464
    switch(config-if)# exit
    switch(config)# exit
    switch#
