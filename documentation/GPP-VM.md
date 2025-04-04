## This is a documentation of the creation of a VirtualMachine with a GPP misconfiguration

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

