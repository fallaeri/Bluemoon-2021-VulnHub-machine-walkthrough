# Bluemoon-2021-VulnHub-machine-walkthrough


 📌 Description

> Bluemoon: 2021 VulnHub walkthrough covering scanning, exploitation, and privilege escalation to root.

---

## 📖 README.md (Short Version)

````markdown
# 🔐 Bluemoon: 2021 Walkthrough

A concise penetration testing walkthrough of the Bluemoon VulnHub machine.

## 🛠️ Tools
Nmap, Gobuster, FTP, Hydra, SSH, Docker

## 🔍 Steps
1. **Scan Network**
   ```bash
   nmap -sn 192.168.56.0/24
   nmap -sV -p- <target-ip>
````

2. **Web Enumeration**

   * Gobuster → found hidden directory
   * QR code → FTP credentials

3. **FTP Access**

   * Downloaded password list

4. **SSH Brute Force**

   ```bash
   hydra -l robin -P p_lists.txt ssh://<target-ip>
   ```

5. **Privilege Escalation**

   * Exploit `feedback.sh` → user `jerry`
   * Docker exploit → root access

## 🏁 Result

* user1.txt ✅
* user2.txt ✅
* root.txt ✅

## ⚠️ Disclaimer

For educational purposes only.

```

---

```
