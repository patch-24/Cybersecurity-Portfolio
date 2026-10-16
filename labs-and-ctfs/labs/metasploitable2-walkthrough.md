# Metasploitable2

# Vulnerability Assessment:

**Target OS:** Linux (Metasploitable 2)  
**Attacking Machine:** Parrot OS  

## 1. Network Reconnaissance (Nmap)
I began by scanning the target IP address to discover open ports and running services.
* **Command used:** `nmap -sV -sC -O <target-IP>`
* **Key Discovery:** Port 21 (FTP) is open and running vsftpd 2.3.4.

## 2. Exploitation (vsftpd 2.3.4 Backdoor)
Researching vsftpd 2.3.4 revealed a known backdoor vulnerability (CVE-2011-2523).
* **Tool Used:** Metasploit Framework (`exploit/unix/ftp/vsftpd_234_backdoor`)
* **Result:** Successfully gained root access to the machine.

## 3. Remediation (How to Fix It)
To secure this system, the administrator should:
1. Update the FTP service to a patched version.
2. Close Port 21 if FTP traffic is not explicitly required.

Below is the Proof of the execution of the payload, at this point the connection on opening a shell listener on port 6200 but metsploit could not get a clean "handshake" from it
<img width="800" height="835" alt="image" src="https://github.com/user-attachments/assets/d2ffe4fc-483b-49c1-ab30-f68182d2d7ec" />

I then decided to grab it manually using netcat and the command was 'nc -nv 192.168.128.2 6200' and connection was successful as seen, I had root priviledges in the machine
Below is the terminal output showing the successful execution of the payload:
<img width="800" height="835" alt="image" src="https://github.com/user-attachments/assets/7f553f22-b394-4c14-b846-b8695011d403" />



# Attacking Web Server: Metasploitable 2
<img width="730" height="570" alt="image" src="https://github.com/user-attachments/assets/c123b035-9161-4b87-8540-529bb2e490fb" />

**Target Service:** 
**Attacking Machine:** Bridged-Adapter Virtual Lab (Parrot OS attacking WordPress Vulnerable Machine)

## 1. Network Enumeration
Using WPsacn, I scanned the target machine to enumarate default users.
* **Tool Used:** WPScan, the command was 'wpscan --url <target's IP> -e u'
* <img width="798" height="623" alt="image" src="https://github.com/user-attachments/assets/64a72f40-a0ed-4e4c-8343-8d8539047779" />


* **Discoveries:** I found out that there was a default user by the name 'admin'

## 2. Bruteforce & Admin Priviledge
Now I am going to bruteforce for the password of the user 'Admin'
* <img width="786" height="726" alt="image" src="https://github.com/user-attachments/assets/aebe182a-6468-43f9-8eb7-04d81c9edde2" />

* **Tool Used:** WPScan
* **Result:** The bruteforce was successful and I was able to obtain the user's password as seen from the result
* <img width="786" height="726" alt="image" src="https://github.com/user-attachments/assets/6bb9db49-4e00-4263-a7e7-77473fabf9b3" />
As seen, I was able to login to the site:
* <img width="786" height="726" alt="image" src="https://github.com/user-attachments/assets/7fc6d1b5-449c-4d8f-b942-b98bb966861d" />

## 3. Remediation & Defense Mapping
**To secure this infrastructure against both WordPress-level and OS-level exploitation, the following controls should be applied:**
1. **Plugin Hygiene:** Remove or update the vulnerable plugins identified during the scan. Implement a policy of "least privilege" for plugins to reduce the attack surface.
2. **Hardening Authentication:** Enable Multi-Factor Authentication (MFA) and implement a plugin like Limit Login Attempts to mitigate the effectiveness of the user enumeration found in Phase 1.
3. **Disable XML-RPC:** Disable xmlrpc.php to prevent amplified brute-force attacks and DDoS potential.
