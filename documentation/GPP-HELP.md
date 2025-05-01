# 🛠️ GPP Password Extraction and Decryption (Windows Client + Kali Linux)

## 🎯 Objective

You have access to a **Windows domain-joined client**, and afterwards you're using **Kali Linux** to decrypt the stored GPP password. Your task:

1. Find the `Groups.xml` file on the client.
2. Transfer it to Kali.
3. Decrypt the password using `gpp-decrypt`.

---

### 1. Log in to the Windows client machine.
### 2. Open **File Explorer** and go to:
`\\WINDOWSSERVER2025\SYSVOL\sigismund.kuttenberg\Policies\Machine\Preferences\Groups\Groups.xml`

- The file should look like this

![image](https://github.com/user-attachments/assets/81ca2dcf-b066-4c6b-a73c-89c152f8e6aa)

- We only need the part which includes the cpassword, you might have to type it manually to extract it this time

### 3. Decoding the cpassword (https://github.com/t0thkr1s/gpp-decrypt/blob/master/README.md)
- We are using t0thkr1s's gpp-decrypt script. Here are quick steps for installing on Kali Linux:

```
# Step 1: Install dependencies
pip3 install pycryptodome colorama

# Step 2: Clone the tool
git clone https://github.com/t0thkr1s/gpp-decrypt
```

Finally we run the tool
```
cd gpp-decrypt

python3 gpp-decrypt.py -c '<encrypted-password-here>'
```

- If all is done correctly, you should get a response from the script that the decoded password was "flag> Kuttenberg"

## References
- https://github.com/t0thkr1s/gpp-decrypt/blob/master/README.md
- https://www.mindpointgroup.com/blog/privilege-escalation-via-group-policy-preferences-gpp
