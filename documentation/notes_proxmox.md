# configuring proxmox server remotely pt1

finally gained access to server remotely

trying to update with apt update, its not working

![](assets/1743762939257.png)

ip ping works, but domain ping not. seems dns is misconfigured.

etc/resolv.conf was misconfigured

![](assets/1743763023212.png)

our assigned dns servers also did not work, seems some routing changes were made to the network when trying to give us access

![](assets/1743763209597.png)

resolved issues by using 8.8.8.8 dns


![](assets/1743763249897.png)

some basic hardening for now:

installed fail2ban with configuration:

![](assets/1743763382182.png)

this didnt work, changed config to backend = systemd. and restarted the service.

![](assets/1743763667537.png)

udp echo testing for routed ports 1194 and 51820

![](assets/1743764217077.png)

openvpn works, lets test WG

![](assets/1743764275410.png)

seems to work!

testing fail2ban

![](assets/1743765029804.png)

seems to be active.

now moving to securign other ports from internal lab network access

![](assets/1743772223067.png)

```
apt install ufw

ufw allow ssh

ufw allow 1194/udp

```

checking config to make sure we dont lose ssh access:

![](assets/1743773155127.png)

ufw status

![](assets/1743773109524.png)

