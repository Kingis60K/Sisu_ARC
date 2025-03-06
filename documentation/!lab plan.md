## SisuARC lab structure

![alt text](assets/lab-schema.png)

1. **Misplaced groups.xml with GPP key (WS1)**  
   - Group Policy Preferences (GPP) voi tallentaa salasanoja **groups.xml**-tiedostoon, joka voi löytyä **SYSVOL-kansiosta**.  
   - Hyökkääjä voi purkaa AES-salauksen ja saada hallintatason tunnukset.  
