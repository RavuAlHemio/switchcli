    switch# configure
    switch(config)# vlan 131
    switch(vlan-131)# name corp
    switch(vlan-131)# exit
    switch(config)# vlan 242
    switch(vlan-242)# name outside
    switch(vlan-242)# exit
    switch(config)# vlan 464
    switch(vlan-464)# name dmz
    switch(vlan-464)# exit
    switch(config)# vlan 353
    switch(vlan-353)# name test
    switch(vlan-353)# exit
    switch(config)# no vlan 353
    switch(config)# exit
    switch#
