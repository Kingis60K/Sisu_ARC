## Installation of systems and basic startup
- Load a [Windows ISO](https://www.microsoft.com/fi-fi/software-download/windows10) and a [Kali linux premade box](https://www.kali.org/get-kali/#kali-virtual-machines)

![image](https://github.com/user-attachments/assets/0581ffd2-b9f6-46d9-a8c4-997615bb3487)
![image](https://github.com/user-attachments/assets/84287233-e5cb-44ce-a0e0-0002e3dc4a65)
*Launched and network settings*

## Creating a misconfigured folder which contains sensitive data

![image](https://github.com/user-attachments/assets/77494250-ae33-4ad1-9d66-6b24a49785bd)

- Create a folder -> Properties -> Sharing -> Advanced Sharing -> Permissions -> Enable all for everyone

![image](https://github.com/user-attachments/assets/d34412ec-2747-420b-926f-d8bf4cc4a82a)

- Relaxed security settings access all

![image](https://github.com/user-attachments/assets/a9f194f6-e87f-4435-8271-4450bb0ce1dd)

- Firewall settings, click Allow an app or feature through Windows Defender Firewall.

![image](https://github.com/user-attachments/assets/71121bfa-9cb2-4ec3-9bef-1076cb9114d7)

- Ensure File and Printer Sharing is allowed.

![image](https://github.com/user-attachments/assets/ed8bca9f-87c0-47ba-b109-74365b86a08b)

- Ensure from Control Panel that SMB 1.0 is used

![image](https://github.com/user-attachments/assets/bec18942-3fe5-44c0-b901-c7c178172a02)

- So in short i did get access to the folder, but not as a guest.
- We started noticing more and more problems and after fighting with SMB versions we decided to start over
- We installed Windows Server 2016 instead of Windows 10 Home

## Look [PilotVM](https://github.com/Kingis60K/Sisu_ARC/blob/main/documentation/PilotVM.md) for successful implementation
