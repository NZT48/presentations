---
marp: true
theme: gaia
_class: lead
paginate: true
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

# DESCON CTF
![](https://pbs.twimg.com/profile_banners/3392424538/1569000939/600x200) 

---
# CTF
* Capture the flag
* Game designed to let you learn to hack in a safe, rewarding environment
* Where: ctf.descon.me
* Style: jeopardy
* Flag format: DCTF{flag}
* Categories:
  * Web, Misc, Crypto, RE, Stegano, IoT
  
---
# Don't forget to have fun!
![w:1000 h:500](https://embeddedworldhome.files.wordpress.com/2019/05/icons_ctf_1.png?w=1250)

---

### Lightning talk:
# IOT SECURITY VULNERABILITIES

![w:1000 h:400](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSHN7NZwlmpZ8L2dpiWibPdfyFwu6ezRMdR2IAehj90VoVzSQByXg)

---
![w:1000 h:600](https://img.deusm.com/darkreading/2014/05/1269204/Cartoon-IOT.jpeg)

---

# OWASP IOT Top 10 (1-5)
  1. Weak, Guessable or Hardcoded passwords
  2. Insecure network services
  3. Insecure ecosystem interfaces
  4. Lack of secure update mehanism
  5. Use of insecure components

---
# OWASP IOT Top 10 (6-10)
  6. Insufficient privacy protection
  7. Insecure data transfer and storage
  8. Lack of device management
  9. Insecure default settings
  10. Lack of physical hardening

---

# Bad passwords
* Types of bad passwords:
  * Weak
  * Guessable
  * Hardcoded 
  * Default
  
* Used in couple CTF challenges
---

![w:1000 h:600](https://img.deusm.com/darkreading/MarilynCohodas/jknewcartoon0814.jpg)

---

![w:1000 h:600](https://www.hackread.com/wp-content/uploads/2016/10/iot-devices-mirai-malware-source-code-2.jpg)


---
* Vatican has the highest botnet density in Europe
  * One bot for every 5 internet users

![w:800 h:400](https://cdn.theatlantic.com/media/mt/science/popecomputer.jpg)

---
# Username Enumeration
* Ability to collect a set of valid usernames by interacting with the authentication mechanism

# Account Lockout
* Ability to continue sending authentication attempts after 3 - 5 failed login attempts

---

# Insecure Network Services
* Unneeded or insecure network services running on the device itself that compromise the confidentiality, integrity, or availability of information or allow unauthorized remote control
  * Vulnerable Services
  * Buffer Overflow
  * Open Ports via UPnP
  * Exploitable UDP Services
  * Denial-of-Service
  * DoS via Network Device Fuzzing

---

# Example
* Ports open to the internet possibly without the user's knowledge via UPnP.

```Port 80 and 443 exposed to the internet via a home router.```

* In the cases above, the attacker is able to disable the device completely with an HTTP GET or access the device via the internet over port 80 and/or port 443.

---

# Shodan.io
![](https://routersecurity.org/pix/Shodan.Network.Camera.jpg)

---
# Insecure Web Interface
  * Account Enumeration
  * Weak Default Credentials
  * Credentials Exposed in Network Traffic
  * Cross-site Scripting (XSS)
  * SQL-Injection
  * Session Management
  * Weak Account Lockout Settings
  
---

# Lack of Transport Encryption
* Username and password are transmitted in the clear over the network

```http://www.xyzcloud.com/login.php?userid=3&password=1234```

* In the cases above, the attacker has the ability to view sensitive data in the clear due to lack of transport encryption
* Used in one ctf challenge

---

# MQTT
* publish subscribe based message passing protocol
* the HTTP of IOT
  * shares all of the vulnerabilities that HTTP and other old insecure protocols have
* By default:
  * without authentication
  * password sent in cleartext

---
# MQTT Architecture

 ![w:1000 h:400](https://miro.medium.com/max/858/1*sIxvchdgHSqAGebJjFHBAg.png)

---

# Message example
![w:500 h:400](https://miro.medium.com/max/249/1*CMUr3uV0lG-oyktoD5JDUw.png)

---

![w:800 h:600](https://i.ibb.co/jzkWWRM/Screenshot-2019-10-02-23-59-35.png)
 
---

![w:1000 h:600](https://miro.medium.com/max/1901/1*KfwKClUBZ3-gcyibVppxtw.png)

---

# Lack of ability to securely update the device

* Update sent without encryption
* Updates not signed
* Update location writable
* Update verification
* Malicious update
* Missing update mechanism
* No manual update mechanism

---
# Poor Physical Security

* Access to Software via USB Ports
* Obtaining console access via serial interfaces (SPI / UART)
* Removal of Storage Media
* NFC 
* Even QR codes can be used as input vector
* Used in couple ctf challenges
---

![w:800 h:600](https://img.deusm.com/darkreading/2017/01/1327898/Klossner-IoT-Backup.jpg)

---

# Final idea
* Tomorrow, after workshops, let's check together the security aspects of Klimamerko
* What we can do:
  * Review the administrative interface of the device 
  * Identify all data types that are being collected 
  * Check how the passwords are stored
  * Check web and cloud interface
  * Code audit
  * Check physical security: USB port, Serial port, SD card...

---

# Useful links:
* https://www.researchgate.net/publication/324149744_A_Comprehensive_IoT_Attacks_Survey_based_on_a_Building-blocked_Reference_Mode
* https://www.owasp.org/index.php/OWASP_Internet_of_Things_Project
* https://www.corero.com/resources/ddos-attack-types/mirai-botnet-ddos-attack
* https://www.sba-research.org/wp-content/uploads/publications/QR_Code_Security.pdf
