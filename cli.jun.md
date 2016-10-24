The default mode when connecting over the network is *operational mode*:

    {master:0}
    root@switch>

Then there is the multi-level *configuration mode*:

    {master:0}[edit]
    root@switch#

Thanks to the underlying FreeBSD system, there are two shells; the *C shell*
(which is the default when connecting via the serial console):

    root@switch:RE:0%

and the *Bourne shell*:

    #

C shell (serial console) → operational mode:

    root@switch:RE:0% cli
    
    {master:0}
    root@switch>

Operational mode → C shell (serial console):

    {master:0}
    root@switch> quit

    root@switch:RE:0%

Operational mode → Bourne shell:

    {master:0}
    root@switch> start shell sh
    #

Bourne shell → operational mode:

    # exit

    {master:0}
    root@switch>

Operational mode (network connection) → C shell:

    {master:0}
    root@switch> start shell csh
    root@switch:RE:0%

C shell → operational mode (network connection):

    root@switch:RE:0% exit
    exit

    {master:0}
    root@switch>

Operational mode → configuration mode:

    {master:0}
    root@switch> config
    
    {master:0}[edit]
    root@switch#

Configuration mode → operational mode:

    {master:0}[edit]
    root@switch# exit configuration-mode
    Exiting configuration mode

    {master:0}
    root@switch>

Entering a deeper level of configuration mode (here: configuring Gigabit
Ethernet interface 0/0/1):

    {master:0}[edit]
    root@switch# edit interfaces ge-0/0/0

    {master:0}[edit interfaces ge-0/0/0]
    root@switch#

Returning to a shallower level of configuration mode:

    {master:0}[edit interfaces ge-0/0/0]
    root@switch# up

    {master:0}[edit interfaces]
    root@switch#

Returning to the top level of configuration mode:

    {master:0}[edit interfaces ge-0/0/0]
    root@switch# top

    {master:0}[edit]
    root@switch#

To protect the root account using the password `AdminSwitch` (Junos OS does not
accept lowercase-only passwords when setting them thus):

    {master:0}[edit]
    root@switch# set system root-authentication plain-text-password
    New password: [no output]
    Retype new password: [no output]

    {master:0}[edit]
    root@switch# commit
    configuration check succeeds
    commit complete

To save the current configuration as the rescue configuration (to which the
switch can be rolled back if necessary):

    {master:0}
    root@switch> request system configuration rescue save
