# 🏠 My Enterprise Cybersecurity Home Lab

> *Where I break things on purpose, so I don't break them by accident in real life.* 😎

---

## 🌐 Network Architecture

To safely practice security testing, I built an isolated virtual network environment.

| ⚙️ Component | 📋 Details |
|---|---|
| **Hypervisors** | VMware & UTM |
| **Isolated Network** | Host-Only, cut off from my physical home network and the internet |
| **Bridged Network** | Bridged Adapter, used only for the Docker host (Alpine) and updates |

---

## ⚔️ Attacking Machines

| 🖥️ Machine | 📝 Notes |
|---|---|
| **Parrot OS** 🦜 | Fully updated with offensive security tools |
| **Kali Linux** 🐉 | Fully updated with offensive security tools |

---

## 🎯 Vulnerable VMs (Boot2Root / Black Box)

Every machine below has been **pwned** ✅. Click a name to read the write-up.

### 🕶️ Black Box: Enumerate Everything
| 🖥️ Machine | 🌍 Source |
|---|---|
| [Metasploitable 2](./labs/metasploitable2-walkthrough.md) 💀 | Rapid7 |
| [Metasploitable 2(Web Server)](./labs/Web-Server-Penetration-Testing.md) 💀 | Rapid7 |
| [Metasploitable 3](./labs/metasploitable3-walkthrough.md) 💀 | Rapid7 |
| [Kioptrix Level 1](./labs/kioptrix-lv1-walkthrough.md) 🌱 | VulnHub |
| [Kioptrix Level 2](./labs/kioptrix-lv2-walkthrough.md) 🌿 | VulnHub |
| [Kioptrix Level 3](./labs/kioptrix-lv3-walkthrough.md) 🌳 | VulnHub |
| [Basic Pentesting 1](./labs/basic-pentesting-1-walkthrough.md) | VulnHub |
| [Stapler 1](./labs/stapler-1-walkthrough.md) | VulnHub |
| [LazySysAdmin](./labs/lazysysadmin-walkthrough.md) | VulnHub |
| [Moria 1.1](./labs/moria-1.1-walkthrough.md) | VulnHub |
| [Lord of the Root 1.0.1](./labs/lord-of-the-root-walkthrough.md) | VulnHub |

### 🌐 Web-Focused Boxes
| 🖥️ Machine | 🌍 Source |
|---|---|
| [Mr. Robot](./labs/mr-robot-walkthrough.md) 🤖 | VulnHub |
| [DC: 1](./labs/dc-1-walkthrough.md) | VulnHub |
| [DC: 9](./labs/dc-9-walkthrough.md) | VulnHub |
| [SickOs 1.1](./labs/sickos-1.1-walkthrough.md) | VulnHub |
| [PwnLab: init](./labs/pwnlab-init-walkthrough.md) | VulnHub |
| [Zico2](./labs/zico2-walkthrough.md) | VulnHub |
| [Lampiao](./labs/lampiao-walkthrough.md) 🐄 | VulnHub |
| [Billu Box 2](./labs/billu-box-2-walkthrough.md) | VulnHub |
| [Node: 1](./labs/node-1-walkthrough.md) | VulnHub |

### 💥 Binary Exploitation & Buffer Overflows
| 🖥️ Machine | 🌍 Source |
|---|---|
| [Brainpan 1](./labs/brainpan-1-walkthrough.md) | VulnHub |
| [Brainpan 2](./labs/brainpan-2-walkthrough.md) | VulnHub |
| [Pinky's Palace v1](./labs/pinkys-palace-v1-walkthrough.md) | VulnHub |

### 🔀 Pivoting & Multi-Host Networks
| 🖥️ Machine | 🌍 Source |
|---|---|
| [Symfonos 2](./labs/symfonos-2-walkthrough.md) | VulnHub |
| [Wintermute 1](./labs/wintermute-1-walkthrough.md) | VulnHub |

### 🧩 Puzzle & Mind Games
| 🖥️ Machine | 🌍 Source |
|---|---|
| [Tr0ll 1](./labs/troll-1-walkthrough.md) 🧌 | VulnHub |
| [Tr0ll 2](./labs/troll-2-walkthrough.md) 🧌 | VulnHub |

### ☁️ Online Platforms
*These live on someone else's servers, so they're not in my local lab, but they're part of the journey.*

| 🖥️ Machine | 🌍 Platform |
|---|---|
| [Wreath](./labs/wreath-walkthrough.md) | TryHackMe |
| [Brainfuck](./labs/brainfuck-walkthrough.md) 🧠 | Hack The Box |

---

## 🕸️ Website Pentesting Vulnerable Endpoints

I hosted these on **Alpine**.

**Alpine:** a lightweight VM that hosts Docker containers running several intentionally vulnerable web applications.

| 🎯 Application | 🔌 Service | 🚪 Port |
|---|---|---|
| [**crAPI**](./Vulnerable-Web-Applications/crapi.md) | Web app | 8888 |
| | Mailhog | 8025 |
| [**VulnBank**](./Vulnerable-Web-Applications/vulnbank.md) | Web app | 5000 |
| [**Juice Shop**](./Vulnerable-Web-Applications/juice-shop.md) 🧃 | Web app | 3000 |
| [**DVWP**](./Vulnerable-Web-Applications/dvwp.md) (WordPress) | Web app | 31338 |
| | phpMyAdmin | 31339 |
| | Mailpit | 31340 |
| | Adminer | 31341 |
| [**OWASP WebGoat**](./Vulnerable-Web-Applications/webgoat.md) | WebGoat | 8080 |
| | WebWolf | 9090 |
| [**Mutillidae**](./Vulnerable-Web-Applications/mutillidae.md) | Web app | 4380 |
| | Scan port | 4388 |
| | HTTPS | 4343 |
| | phpMyAdmin | 4381 |
| | phpLDAPAdmin | 4382 |
| [**DVGA**](./Vulnerable-Web-Applications/dvga.md) (GraphQL) | Web app | 4513 |
| [**bWAPP**](./Vulnerable-Web-Applications/bwapp.md) 🐝 | Web app | 4514 |

---

<div align="center">

### 🔐 Break it. Document it. Fix it. Repeat. 🔐

</div>
