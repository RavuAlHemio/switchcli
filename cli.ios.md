The initial mode (`switch` is the hostname) is *user exec mode*:

    switch>

More privileged is *privileged exec mode*:

    switch#

Finally, there is the multi-level *configuration mode*:

    switch(config)#

User exec mode → privileged exec mode:

    switch> enable
    switch#

Privileged exec mode → user exec mode:

    switch# disable
    switch>

Privileged exec mode → configuration mode:

    switch# configure terminal
    switch(config)#

Entering a deeper level of configuration mode (here: configuring Gigabit
Ethernet interface 0/1):

    switch(config)# interface GigabitEthernet 0/1
    switch(config-if)#

Returning to a shallower level of configuration mode:

    switch(config-if)# exit
    switch(config)#

Configuration mode → privileged exec mode (immediately):

    switch(config-if)# end
    switch#

To protect privileged exec mode using the password `adminswitch`:

    switch# configure terminal
    switch(config)# enable secret 0 adminswitch

To ensure that the running configuration persists across reboots:

    switch# copy running-config startup-config
    Destination filename [startup-config]? ↲
    Building configuration...
    [OK]
    switch#
