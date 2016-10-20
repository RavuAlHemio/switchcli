Note: to be able to access privileged exec mode via an SSH connection, a
password must be set using `enable secret` in configuration mode.

    switch# configure terminal
    switch(config)# ip domain name switches.example.com
    switch(config)# crypto key generate rsa modulus 4096
    The name for the keys will be: switch.switches.example.com
    
    % The key modulus size is 4096 bits
    % Generating 4096 bit RSA keys, keys will be non-exportable...
    [OK] (elapsed time was 401 seconds)
    switch(config)# aaa new-model
    switch(config)# username switchadmin password 0 adminswitch
    switch(config)# exit
    switch#
