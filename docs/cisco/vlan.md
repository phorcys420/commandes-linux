# VLANs & Trunks

## Création d'un VLAN

=== "Version humaine"

    ```
    enable
    config terminal

    vlan <vid>
    name <nom>

    interface vlan <vid>
    ip address <ip> <msr>
    no shutdown

    interface FastEthernet 0/1
    switchport mode access
    switchport access vlan <vid>
    no shutdown

    copy running-config startup-config
    ```

=== "Version sans âme"

    ```
    en
    conf t

    vl <vid>
    na <nom>

    in vlan <vid>
    ip a <ip> <msr>
    no sh

    in fa0/1
    sw m a
    sw a v <vid>
    no sh

    wr
    ```
