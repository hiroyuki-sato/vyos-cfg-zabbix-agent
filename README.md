## Zabbix agent commands for VyOS

Zabbix agent commands for VyOS


## Install zabbix-agent

In build-iso directory.

    git clone http://github.com/vyos/build-iso
    cd build-iso/pkgs
    wget 'http://repo.zabbix.com/zabbix/2.2/debian/pool/main/z/zabbix/zabbix-agent_2.2.4-1+squeeze_amd64.deb'
    cd .. # top of build-ios
    echo "zabbix-agent"  >> livecd/config.vyatta/chroot_local-packageslists/vyatta-extra.list

## Build vyos-cfg-zabbix-agent

    git clone http://github.com/hiroyuki-sato/vyos-cfg-zabbix-agent
    debuild -us -uc
    cd ..
    cp vyos-cfg-zabbix-agent_0.0.1_amd64.deb build-iso/pkgs
    cd build-iso # top of build-iso
    echo "vyos-cfg-zabbix-agent" >> livecd/config.vyatta/chroot_local-packageslists/vyatta-extra.list

and build iso image.


## Command reference.

    set system zabbix-agent
    set system zabbix-agent debug_level
    set system zabbix-agent enable_remote_commands
    set system zabbix-agent hostname
    set system zabbix-agent listen_port
    set system zabbix-agent log_file_size
    set system zabbix-agent log_remote_commands
    set system zabbix-agent server
    set system zabbix-agent server_active
