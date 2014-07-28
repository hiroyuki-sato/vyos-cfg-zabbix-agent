## Zabbix agents commands for VyOS

Zabbix agents commands for VyOS


## Install zabbix-agents

In build-iso directory.

    git clone http://github.com/vyos/build-iso
    cd build-iso/pkgs
    wget 'http://repo.zabbix.com/zabbix/2.2/debian/pool/main/z/zabbix/zabbix-agent_2.2.1-1+wheezy_amd64.deb'
    cd .. # top of build-ios 
    echo "zabbix-agent"  >> livecd/config.vyatta/chroot_local-packageslists/vyatta-extra.list

## Build vyos-cfg-zabbix-agents

    git clone http://github.com/hiroyuki-sato/vyos-cfg-zabbix-agent
    debuild -us -uc 
    cd ..
    cp vyos-cfg-zabbix-agents_0.0.1_amd64.deb build-iso/pkgs    
    cd build-iso # top of build-iso 
    echo "vyos-cfg-zabbix-agents" >> livecd/config.vyatta/chroot_local-packageslists/vyatta-extra.list

and build iso image.


## Command reference.

    set system zabbix-agents
    set system zabbix-agents server 
    set system zabbix-agents server_active

