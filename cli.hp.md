The initial mode (`switch` is the hostname) is *operator level*:

    switch>

More privileged is *manager level*:

    switch#

Finally, there is the multi-level *configuration level*:

    switch(config)#

Operator level → manager level:

    switch> enable
    switch#

Manager level → operator level:

    switch# exit
    switch>

Manager level → configuration level:

    switch# configure
    switch(config)#

Entering a deeper level of configuration level (here: configuring Ethernet
interface 1):

    switch(config)# interface ethernet 1
    switch(eth-1)#

Returning to a shallower level of configuration level:

    switch(eth-1)# exit
    switch(config)#

Configuration mode → privileged exec mode (immediately):

    switch(eth-1)# end
    switch#

To protect manager level using the username `switchadmin` and password
`adminswitch`:

    switch(config)# password operator user-name switchadmin plaintext adminswitch

To ensure that the running configuration persists across reboots:

    switch# write memory
