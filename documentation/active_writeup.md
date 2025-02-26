short memo/wriuteup of example easy windws  smb / active directory vulnerability target machine on hackthebox

"Active is an easy to medium difficulty machine, which features two very prevalent techniques to gain privileges within an Active Directory environment."

![](assets/1740570832541.png)



Enumerating the target host


![](assets/1740565114403.png)


found accessable share with anon access

![](assets/1740565174546.png)

browsed through files to find a password (hinted on hackthebox)

![](assets/1740565210606.png)

found groups.xml containing encrypted password 

![](assets/1740565234704.png)

cracked with gpp-decrypt

![](assets/1740565247622.png)

accessed smb share with previously gained user/pw info

found flag file on users desktop

![](assets/1740565738066.png)

User owned, moving on to root

Kerberoasting:

with previouslly gained credentials, scanning for kerberoasting accounts

![](assets/1740566273007.png)


TGS-REP hash found

cracking the hash

`hashcat -m 13100 kbhash.txt /usr/share/wordlists/rockyou.txt --force --attack-mode=0`

![](assets/1740570520035.png)

With the admin credentials, going back to smb share, we now have access to the administrator folder on the share Users

![](assets/1740570768849.png)

root flag found on desktop

![](assets/1740570809338.png)