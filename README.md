## Name: Blessing Jeffrey YL
## Reg.no: 212223220014

# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="1920" height="936" alt="Screenshot_2025-09-28_16_09_29" src="https://github.com/user-attachments/assets/d67e681b-9bf8-4a5b-8f20-de008d502a94" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="1920" height="936" alt="Screenshot_2025-09-28_16_09_29" src="https://github.com/user-attachments/assets/eac33ec4-6f86-4a4c-8c99-4ed07e6f57e1" />
<img width="1920" height="936" alt="Screenshot_2025-09-28_16_09_35" src="https://github.com/user-attachments/assets/9739b0bd-9032-4194-a79f-9ce2edb8e2cb" />


**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="1920" height="936" alt="Screenshot_2025-09-28_16_09_44" src="https://github.com/user-attachments/assets/f3f44a89-dc98-4a42-8b67-d4e8099d9ead" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="1920" height="936" alt="Screenshot_2025-09-28_16_09_59" src="https://github.com/user-attachments/assets/17d708b7-a242-4e0c-b575-89e28440ad19" />


**6. Send the generated link to the victim.**
<img width="1920" height="936" alt="Screenshot_2025-09-28_16_11_30" src="https://github.com/user-attachments/assets/4cdecc9d-3b0a-4d77-899e-2e48acac0481" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="1920" height="936" alt="Screenshot_2025-09-28_16_12_14" src="https://github.com/user-attachments/assets/287a5816-9c35-4495-bb70-1b8b22d89482" />



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
