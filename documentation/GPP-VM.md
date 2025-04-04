## This is a documentation of the creation of a VirtualMachine with a GPP misconfiguration

### 1. Installation and network configuration
- First of all download the image files. This time I decided to use: 
  - Windows 10 Pro (https://www.microsoft.com/en-us/software-download/windows10?msockid=0d1a47f1d26963fc37db5342d3416219)
  - Windows Server 2025 (https://www.microsoft.com/en-us/evalcenter/download-windows-server-2025?msockid=0d1a47f1d26963fc37db5342d3416219)

- Then make sure you choose to install the Pro version of Windows 10 and Standard Evaluation (Desktop Experience) version of the Windows Server 2025
- After installation it is time to put both computers on the same internet

![](assets/GPP-network-settings.png)
![](assets/GPP-network-settings2.png)
![](assets/GPP-network-settings3.png)
![](assets/GPP-network-settings4.png)

- Above are the network card settings
- You also need to set both computers to the 'Host-only Adapter' network
- I left the Windows Server 2025 also with NAT networking since I might need to access the internet from it

### 2. ICMPv4 enabling
- In order to verify connection between the computers we should be able to send ICMP packets
- This is normally disabled so using the this line of code ``netsh advfirewall firewall add rule name="Allow ICMPv4" protocol=icmpv4 dir=in action=allow`` we can enable it

![](assets/GPP-ICMPv4-toggle.png)

- Above there is also ping test ran from the 2025 server pinging the Win10 machine
- It is a success so there is a working connection between the computers

### 3. DNS and Domain basics
- In order for our computer to connect to the domain they must use the DNS server offered by our Domain Controller hosted on Windows Server 2025

![](assets/GPP-dns-settings.png)
![](assets/GPP-win10-home-cannot-be-added-to-a-domain.png)

- Above is the DNS configuration used in our environment
- But things cannot run smoothly so while doing the configuration I noticed that Win10 Home machines cannot be added to a domain
- I asked you from the start to install the Win10 Pro version to avoid this issue

![](assets/GPP-domain-successful.png)

- Well when you have done things once it doesn't take that long to replicate
- I successfully added the Win10 Pro computer to the domain ``sigismund.kuttenberg``

### 4. Domain user and group configuration
- I did a lot of research and looking around, there was so much interesting stuff

![](assets/GPP-domain-user.png)
![](assets/GPP-domain-group.png)

- I decided to do a user and a group to add that user in
- This would enable me to inspect files in the domain from the Win10 Pro computer using these credentials
- This would lead us eventually to be able to inspect the vulnerable group.xml file which would contain an encoded but unencrypted password

### 5. GPP misconfiguration



## References
- https://www.server-world.info/en/note?os=Windows_Server_2025&p=initial_conf&f=6
- 
