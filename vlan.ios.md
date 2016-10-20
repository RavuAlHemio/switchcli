    switch# configure terminal
    switch(config)# vlan 131
    switch(config-vlan)# name corp
    switch(config-vlan)# exit
    switch(config)# vlan 242
    switch(config-vlan)# name outside
    switch(config-vlan)# exit
    switch(config)# vlan 464
    switch(config-vlan)# name dmz
    switch(config-vlan)# exit
    switch(config)# vlan 353
    switch(config-vlan)# name test
    switch(config-vlan)# exit
    switch(config)# no vlan 353
    switch(config)# exit
    switch#
