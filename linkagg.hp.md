    switch# configure
    switch(config)# trunk ethernet 5,6 trk1 trunk
    switch(config)# vlan 131 untagged trk1
    switch(config)# trunk ethernet 7,8 trk2 lacp
    switch(config)# vlan 131 tagged trk2
    switch(config)# vlan 242 tagged trk2
    switch(config)# vlan 464 tagged trk2
    switch(config)# exit
