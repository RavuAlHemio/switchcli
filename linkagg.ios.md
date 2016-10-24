    switch# configure terminal
    switch(config)# interface Port-channel 1
    switch(config-if)# switchport mode access
    switch(config-if)# switchport access vlan 131
    switch(config-if)# exit
    switch(config)# interface GigabitEthernet 0/5
    switch(config-if)# channel-group 1 mode on
    switch(config-if)# exit
    switch(config)# interface GigabitEthernet 0/6
    switch(config-if)# channel-group 1 mode on
    switch(config-if)# exit
    switch(config)# interface Port-channel 2
    switch(config-if)# switchport mode trunk
    switch(config-if)# switchport trunk allowed vlan 131,242,464
    switch(config-if)# no switchport trunk native vlan
    switch(config-if)# exit
    switch(config)# interface GigabitEthernet 0/7
    switch(config-if)# channel-group 2 mode active
    switch(config-if)# exit
    switch(config)# interface GigabitEthernet 0/8
    switch(config-if)# channel-group 2 mode active
    switch(config-if)# exit
