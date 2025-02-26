## Preparing hardware

### Background

Inherited server hardware from previous project, no knowledge of user/password data.

### Specs



### Booting up servers

Servers couldnt be reached via dhcp, iDRAC settings dont seem to be default. 

Figured best & fastest solution is to connect monitor&keyboard&mouse to the server for resetting settings.

![alt text](assets/image-22.png)

Navigating from bios to iDRAC reset settings:

![alt text](assets/image-19.png)

![alt text](assets/image-20.png)

![alt text](assets/image-21.png)

![alt text](assets/image-18.png)

Resetting to default

### iDRAC web interface

Finally when settings were reset, the iDRAC port was given ip from dhcp on router

![alt text](assets/image.png)

Tried default passwords root/calvin, not working.

Server was initially ordered with secure addon, meaning password was printed on the plastic id tag on the server

![alt text](assets/image-23.png)

After login, we need to download the proxmox assets/image:

![alt text](assets/image-1.png)

To install the assets/image, we add a virtual cd&/dvd drive to the iDRAC:

![alt text](assets/image-2.png)

![alt text](assets/image-3.png)

![alt text](assets/image-4.png)

![alt text](assets/image-5.png)


![alt text](assets/image-6.png)


![alt text](assets/image/assets/image-7.png)

![alt text](assets/image-8.png)

![alt text](assets/image-9.png)

install location

![alt text](assets/image-10.png)


# Router setup

edgerouter pro 8

Aquired used hardware, password unknown, from ubuquiti manual trying Resetting

![resetpw](assets/image-11.png)

this works, user ubnt pw ubnt 

Updating firmware:

![alt text](assets/image-12.png)


![alt text](assets/image-13.png)



# Trying VDI connection to school lab environment

Our teacher Harto mentioned that our ip-space for the server would be accessable through the vdi connection, however we could not access the router through vdi:

![alt text](assets/image-16.png)


![alt text](assets/image-17.png)

Sending inquiry about vdi to teachers via email.