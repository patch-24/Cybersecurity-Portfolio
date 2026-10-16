# My Enterprise Cybersecurity Home Lab

## 🌐 Network Architecture
To safely practice security testing, I built an isolated virtual network environment.
* **Hypervisor:** VMware & UTM
* **Network Type:** Host-Only (isolated from the physical home network and the internet) & Bridged Adapter

## 🖥️ System Inventory
* **Attacking Machine:** Parrot OS & Kali Linux (Fully updated with offensive security tools) 
* **Jeopardy-Style (Black Box) Vulnerable VMs:** 
  * Metasploitable 2
  * Kioptrix Level 1, Level 2 & Level 3
  * Metasploitable 3
  * Troll 1 & 2
  * Mr Robot CTF

* **WEbsite PenTesting Vulnerable Endpoints:**
  * Alpine - a VM that I use to host docker containers containing several vulnerable Web Applications.
   Below are the Application and ports:
    * crAPI: 8888 & (crAPI)Mailhog: 8025
    * VulnBank: 5000
    * Juiceshop: 3000
    * DVWP (wordpress): 31338 & DVWP(31339) : phpMyAdmin & DVWP(31340) : Mailpit & DVWP (31341) : Adminer
    * OWASP WebGoat: 8080 & WebWolf: 9090
    * Mutillidae: 4380 & Mutillidae(Scan Port): 4388 & Mutillidae HTTPS: 4343 & Mutillidae PhpMyAdmin: 4381 & Mutillidae phpLDAPAdmin: 4382
    * DVGA: 4513
    * BWAPP: 4514
  

