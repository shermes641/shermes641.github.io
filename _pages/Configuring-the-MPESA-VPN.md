There are several subtleties to the VPN configuration that are made unfortunate due to EC2 complications.

The first step is to follow this excellent guide : 

https://gist.github.com/kryptek/7683862

You can find all of the relevant configuration files here : 

https://github.com/Powerhive1/Server-Python/tree/master/vpn

You also need to disable source/dest checking for the VPN instance (and maybe for any instances that will connect to the VPN).  This can be done under the EC2 management console - right click on the instance, under networking.

In order for any instance other than the VPN instance to reach the remote endpoint, we also need to add a route to our VPC Routing Table (in AWS) - any traffic to the right subnet should go through the VPN instance.

Finally, on the VPN instance, add the following to rc.local, and execute it on the command line (as root) : 

iptables -t nat -I POSTROUTING -s 172.31.0.0/20 -o eth0 -j MASQUERADE

This allows the VPN instance to proxy any traffic through to the other side from other instances in the VPC.
