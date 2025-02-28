# Pilot VM windows server 2025 locally

## Setup machine & Netwrok locally

This is a short report on installing our first vulnerable VM, in a local vm network setting.

Windows Server 2025 iso from https://www.microsoft.com/en-us/evalcenter/download-windows-server-2025


For piloting purposes, this host is locally installed and ran on virtualbox, virtual disk greater than 12gb, choose skip unattended install to enable version selection & choosing desktop experience

![](assets/1740729776755.png)

Encountered error installing to selected partition on default settings, after deleting default partition and choosing unnallocated space, the install could continue.

![](assets/1740730000109.png)

During install, only options to change was updates to manual, and remote enabled

![](assets/1740730151147.png)

![](assets/1740730244125.png)


Enable icmpv4 pinging as per steps here https://www.server-world.info/en/note?os=Windows_Server_2025&p=initial_conf&f=6

![](assets/1740731731138.png)

Now network is setup between attack vm and target vm

![](assets/1740735147226.png)


## Add some vulnerability (smb share)

install smb1, create vulnerable share

![](assets/1740733114467.png)


Enable Guest user on the server with following commands

```
Get-LocalUser Guest

Enable-LocalUser -Name Guest

net user Guest /active:yes
```
Grant rights on VulnShare
```
icacls "C:\VulnShare" /grant Everyone:F /T /C /Q
icacls "C:\VulnShare" /grant "ANONYMOUS LOGON":F /T /C /Q
```

restart smb
```
Restart-Service LanmanServer
```

![](assets/1740734959080.png)

Now shares are discoverable, and the Shared & VulnShare folders are readable