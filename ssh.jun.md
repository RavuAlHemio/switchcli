Note: Junos OS does not accept lowercase-only passwords when setting them thus.

    {master:0}
    root@switch> configure

    {master:0}[edit]
    root@switch# edit system login user switchadmin

    {master:0}[edit system login user switchadmin]
    root@switch# set authentication plain-text-password
    New password: [no output]
    Retype new password: [no output]

    {master:0}[edit system login user switchadmin]
    root@switch# set class super-user

    {master:0}[edit system login user switchadmin]
    root@switch# top

    {master:0}[edit]
    root@switch# set system services ssh

    {master:0}[edit]
    root@switch# commit
    configuration check succeeds
    commit complete

    {master:0}[edit]
    root@switch# exit

    {master:0}
    root@switch>
