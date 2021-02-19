# Oak-SecureKids-Container

## QNAP Container Config
    Item	Value
    Name	oak-pihole
    Entrypoint	/s6-init
    Auto start	Enable
    CPU Limit	25 %
    Memory Limit	512 MB
    Environment	DNSMASQ_USER=root
    FTL_CMD=no-daemon
    IPv6=False
    PATH=/opt/pihole:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
    PHP_ENV_CONFIG=/etc/lighttpd/conf-enabled/15-fastcgi-php.conf
    PHP_ERROR_LOG=/var/log/lighttpd/error.log
    PIHOLE_ARCH=amd64
    PIHOLE_INSTALL=/root/ph_install.sh
    S6_BEHAVIOUR_IF_STAGE2_FAILS=2
    S6_KEEP_ENV=1
    S6_LOGGING=0
    S6OVERLAY_RELEASE=https://github.com/just-containers/s6-overlay/releases/download/v2.1.0.2/s6-overlay-amd64.tar.gz
    ServerIP=192.168.1.253
    VERSION=v5.2.4
    WEBPASSWORD=xxxxxxx
    TZ=Europe/London
    Network Mode	Bridge (Use static IP)
    Use Interface	Adapter 1+2 (Virtual Switch 3)
    IP Address	192.168.1.253
    Netmask	255.255.255.0
    Gateway	192.168.1.254
    Volume from host	
    Host Path	Mount Point
    /Container/container-station-data/application/PiHole/etc-pihole	/etc/pihole
    /Container/container-station-data/application/PiHole/etc-dnsmasq.d	/etc/dnsmasq.d

Run this command on the Container Console

    apt update   
    apt upgrade         
    apt install python3-pip
    pip3 install pihole5-list-tool --upgrade
    pihole5-list-tool

add this URK to the Web interface -> Group Management -> Adlist

    https://raw.githubusercontent.com/StevenBlack/hosts/master/alternates/fakenews-gambling-porn/hosts

Run this command on the Container Console

    pihole -g

 
References:  
https://hub.docker.com/r/pihole/pihole  
https://github.com/pi-hole/docker-pi-hole
https://github.com/jessedp/pihole5-list-tool  
https://github.com/StevenBlack/hosts/blob/master/alternates/fakenews-gambling-porn-social/readme.md  
