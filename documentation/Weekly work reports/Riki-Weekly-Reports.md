# Riki - Hours spent on course

**Total: 368 hours** including classes & presentation

Team & guidance meetings 	**50h**

On-prem environment		    **155h**

Webapp / cloud		    **118h**

Learning / studying		    **45h**


Took over the architecture part of the project when we lost members.

We had weekly meetings within the team, usually 1-3 hours.
Most weeks we also had a meeting with our teacher ~30min.

## Week 3

Campus course day

**3 hours**

## Week 4

Campus course day
Preparing potential hardware

**5 Hours total**

## Week 5
Campus course day
Initial planning  
Budget and Schedule first concepts  
Ideas about the scope of the project and execution  
Preparing(resetting) hardware, setting up idrac, installing proxmox & ubiquiti router

https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/Hardware_setup_phase1.md

**30 hours of work**

---

## Week 6
Meetup & Planning with SisuCTF @ Pasila  
Installing hardware @ Pasila
Finishing up the plan  
Determining final scope and schedule  
Making the presentation  

Trying to connect to the on-prem server, without success, not even vdi
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/Hardware_setup_phase1.md#trying-vdi-connection-to-school-lab-environment

**30 hours of work**

---

## Week 7
Online meetup with Tero & sisuCTF Notes  
Goal set -> have a working SMB demo by week 9  

Setting up CSC account, creating servers, having issues with certificates

**15 hours of work**

---

## Week 8
Vacation week  
Minor documentation and some research done  

**5 hours of work**

---

## Week 9

Practicing & Studying AD vulnerabilities
 - "Active" machine on hackthebox
 https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/active_writeup.md

Creating a Pilot VM with SMB vulnerability on Windows Server 2025 locally
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/PilotVM.md

**20 hours of work**

---

## Week 10
Setting up echoCTF.RED on hetzner (multiple times)

https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/echoCTF_setup.md

Setting up mxroute & webmail mail.sisuctf.com (required for the webapp)
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/MailServerSetup.md

Acquiring sisuctf.com domain.

Setting up coming soon landing page hosted on vercel, first time trying out v0 ai to create websites.

https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/countdown_landingpage.md

Setting up dns records & nameserver moved from namecheap to hetzner.

**40 hours of work**

---

## Week 11

Had several issues with EchoCTF.RED, talked to the solo developer on discord he suggested to try openBSD
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/BSD_setup.md

However this wasnt so easy since it was not a default image on hetzner and required installing through "recovery"  mode.

After some trial and error started to look into alternatives, noticed on the echoctf.red discord that the framework was very unstable.

**20 hours of work**

---

## Week 12

Made the switch for CTFd framework, initial setup:
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/ctfd_setup.md

Also setting up smtp on CTFd
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/MailServerSetup.md

Troubleshooting and setting up dns records
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/MailServerSetup.md#webmail-send--recieve

Participated in the Cyber Apocalypse CTF, completed some challenges related to our project (windows forensics)

**25 hours of work**

---

## Week 13

Ran into several problems trying to do TLS "right" with automatic renewals (preferably a separate docker).

Ended up switching the docker setup from normal docker to a docker swarm, with loadbalancing tls
https://github.com/chrisandoryan/ScaledCTFd/tree/main

Setting it up on a fresh vm and re-doing previous configurations with smtp, themes, plugins etc.

https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/ctfd_part2.md

This week had email conversations with Tero & Vesa from school IT department about finally getting our public ip/ports forwarded.

**!still no ip/route!**

**35 hours of work**

---

## Week 14
Conversations with Vesa continued, full day at campus on monday trying to get IP routes to work without success.
(turned out later this week they were not routed correctly, my configurations were fine.. a day wasted)

On friday after meeting with Tero the ip routes were finally fixed by the IT department.
Full night on friday and saturday setting up proxmox remotely. accounts, firewalls(ufw), fail2ban.
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/notes_proxmox.md

Sunday installing and configuring wireguard.
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/notes_proxmox_pt2.md


**40 hours of work**

---

## Week 15
Our site officially launched

Setting up storage & images for vms, wireguard accounts & how to meeting for team members.
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/notes_proxmox_pt3.md

setting up vlan and test vm from install image
https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/notes_proxmox_pt4.md

**25 hours of work**

---

## Week 16

Setting(trying to setup) up openVPN for players

Tried several different plugins, tried to create my own plugin, ran into several different issues.

https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/openvpn_server.md


**30 hours of work**

---

## Week 17

Going for a manual setup of openVPN

https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/openvpn_part2.md

Participated Hacking Active Directory with Nikita @Pasila

**15 hours of work**

---

## Week 18

Setting up OpenVPN for players in the form of a challenge, super easy one just to give them the ovpn profile file

**10 hours of work**

---

## Week 19
Final report  
Final presentation  
Group assessment  

Validation Inquiry

**20 hours of work**

---


Project done

**Total: 368 hours**

---
