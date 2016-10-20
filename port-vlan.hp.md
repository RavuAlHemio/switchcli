    switch# configure
    switch(config)# interface ethernet 1
    switch(eth-1)# untagged vlan 131
    switch(eth-1)# exit
    switch(config) interface ethernet 2
    switch(eth-2)# tagged vlan 131,242
    switch(eth-2)# exit
    switch(config) interface ethernet 3
    switch(eth-3)# tagged vlan 131,242
    switch(eth-3)# untagged vlan 464
    switch(eth-3)# exit
    switch(config)# exit
    switch#
