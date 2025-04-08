# setting up vlan and test vms

![](assets/1743926238971.png)

setting ipv4 as 10.8.0.1/24

## creating a vm in GUI

creating openvpn vm server

![](assets/1743926706810.png)

also checked start at boot

![](assets/1743926758928.png)

changed storage to zfs-vmlab

![](assets/1743927215226.png)

changed cpu type to host for better performance

![](assets/1743927439137.png)

memory, feeling generous and giving 4gb instead of 2gb

![](assets/1743927540971.png)

network:

![](assets/1743927649509.png)

summary:

![](assets/1743927780844.png)

## issues on first start

![](assets/1743928822783.png)

seems i forgot to apply the network configuration, vmbr1 is active=no

![](assets/1743929114107.png)

now vm is starting and i can continue

![](assets/1743929157667.png)

## openvpn setup on proxmox

![](assets/1743929361048.png)

![](assets/1743929487771.png)

edit dhcp to manual:

![](assets/1743929693950.png)

![](assets/1743929893488.png)

choosing enable ssh 

skip ubuntu pro, install

![](assets/1743930105353.png)

rebooting

![](assets/1743933162023.png)

booting failed, iso image still mounted, removing it under hardware tab

![](assets/1743933250785.png)

now it works


---

Setting up wg for rest of project members

