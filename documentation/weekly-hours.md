## Week 5

- The project planning began
- We divided into two groups: SisuCTF and SisuArc
- Discussions and testing of different platforms
- Writing the plan
- weekly lesson

**About 13h of work**

## Week 6

- Presentation prep
- Slideshow on the topic
- Refining the project schedule and goals
- Helping hands with hardware assembly at school
- Creating C-pouta users and testing the platform

  **About 20h of work**

## Week 7

- I started building the platform for the website in the cloud.
- Problems encountered:
    - A virtual machine can be launched in C-Pouta, but it can't be accessed because the session is somehow locked.
    - I tried again on a different machine using PuTTY, but received an error stating that the key is either outdated or doesn't exist.
    - Issues converting the key into the correct file format (.ppk).
- One of the team members dropped the course.
- Meeting with Tero 30 minutes

**About 20h of work**

## Week 8

- Holiday, no progress.

## Week 9

- A decision was made in the project not to use C-Pouta as the base for the website.
- Conducted research on the topic Group Policy file with user/password hash for about 3 hours.
- Meeting with tero 30 minutes.
- Quick meet up with project members.

**About 3h of work**

## Week 10

- We lost another group member, now only three of us remain.
- We held a meeting on the matter and agreed on new areas of responsibility.
- Did an additional hour of research on creating a vulnerable machine.
- A personally tough week due to the rush to finish other courses before the end of the study period.

**About 3h of work**

## Week 11

- Slow week due to the flu.
- 

## Week 12

- 18.3 Downloaded win 10 but something went wrong so had to delete. This took about 2 hours, was at my parents for a little holiday and sick so got no work done.
    - The solution was that during installation, the Pro version had to be selected in order to log in without a key, so the system had to be reinstalled.
There were issues with the internet connection, and the installation of the machine took almost 2 hours.
- 21.3 30 m meeting with tero. about 1h with group.

- 22.3 Started working on the server machine. Somehow downloading this machine took little over 4 h. After that started working on the script. Had some problems on the way but eventually got it running. 1h.

**about 11,5h of work**

## Week 13

- 26.3 Finally had the time to continue the project. But when I opened the server machine everything was black and would not load.
- After about 1 hour of research found out I had the wrong configurations. On the last try I edited the video memory from 16 to 128 MB. This fixed my problem. After making this change loading only took little over 45 minutes, so internet wasn't the problem.
- Everything was running smoothly so started working on the script. This time got it working on the first try. 30 minutes.
- Had some problems with ethernet did some research and with couple changes it was running again. 30 minutes.
- Time to configure GPO.
- had some problems on the way:
      - It was pretty much smooth sailing for an hour until I had to put the script that generates a plaintext password to a test user with admin privilages to the script folder in \\windows\sisu.admin.com\SYSVOL\sisu.admin.com\Policies\GPO-ID\Machine\Scripts\Startup. I got the Script to the right folder but when I went to double check in cmd it wasn't there. With about 1,5h minutes on research I got it up and running.

**About 5 hours of work**  

## Week 14

4.4. - Meeting with tero 30 minutes. Meeting with the team 2 hours.
- Was pretty confused on the topic so did research for 2 hours.

5.-6.4 - Time to connect win11 computer to the server.
    - I tried to join the domain, not possible.
    - Tested connections, only nslookup would work.
    - Did some research for little over an hour.
    - Turns out the problem is with the firewall.
          - enabled criticals, tried again and still not working. More research. 
          - Had to configure firewall. Allowed the domain to join TCP ports 88, 135, 389, 445, 464, 636, 3268, 3269. 
          - Verified the rules and then tested the connections. Firewalls were okay but still not able to join the domain. 
          - Did research on the topic for 2 hours.

6.4.

- Meeting with the group about Proxmox about 2 hours.
- Tested how Proxmox works since it's new to me. 40 minutes.

**About 12 hours of work**

## Week 15



