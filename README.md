# Oak-SecureKids-Container

docker run -d --name pihole --restart=always -p 7080:80 -p 53:53/tcp -p 53:53/udp -e TZ=Continent/City -e WEBPASSWORD=Somepass -e ServerIP=192.168.1.100 -v /mnt/data/pihole/pihole:/etc/pihole -v /mnt/data/pihole/dnsmasq:/etc/dnsmasq.d pihole/pihole:latest

    $ apt update   
    $ apt upgrade         
    $ apt install python  
    $ apt install python3-pip
    $ sudo pip3 install pihole5-list-tool --upgrade
    $ sudo pihole5-list-tool
    $ sudo pihole -a -p
 
References:  
https://hub.docker.com/r/pihole/pihole  
https://github.com/jessedp/pihole5-list-tool  
https://github.com/StevenBlack/hosts/blob/master/alternates/fakenews-gambling-porn-social/readme.md  
