# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

---

# DESIGN STEPS

## Step 1
Install Kali Linux either in a partition, VirtualBox, or live mode.

## Step 2
Investigate the various categories of Metasploit tools and modules.

## Step 3
Open the terminal and execute Kali Linux and Metasploit commands.

---

# EXECUTION STEPS AND USAGE

## 1. Find the Attacker System IP Address
Open the Kali Linux terminal and identify the IP address of the attacker machine.

```bash
ifconfig
```

Or:

```bash
ip a
```

### Usage
This command helps identify the local machine IP address connected to the network.

---

## 2. Start Metasploit Framework
Launch the Metasploit console.

```bash
msfconsole
```

### Usage
Loads the Metasploit Framework environment used for scanning, reconnaissance, and exploitation.

---

## 3. Display Available Commands
Inside `msfconsole`, type:

```bash
help
```

Or:

```bash
?
```

### Usage
Displays all available Metasploit commands and their functionalities.

---

## 4. Perform TCP Port Scanning
Scan the local network for open ports between 1 and 1000.

```bash
nmap -sT 192.168.181.0/24 -p1-1000
```

### Usage
Performs a TCP connect scan to identify active systems and open ports in the network.

---

## 5. Scan and Save Results into Metasploit Database
Use the `db_nmap` command.

```bash
db_nmap 192.168.181.0/24
```

### Usage
Stores scan results directly into Metasploit’s PostgreSQL database for later use during exploitation.

---

## 6. Access Auxiliary Scanner Modules
Navigate to the Metasploit auxiliary modules directory.

```bash
cd /usr/share/metasploit-framework/modules/auxiliary
```

List the available modules:

```bash
ls -l
```

### Usage
Auxiliary modules contain scanners and enumeration tools for services like FTP, SMB, HTTP, and MySQL.

---

## 7. Search for Exploit Modules
Search for Microsoft-related exploit modules.

```bash
search name:Microsoft type:exploit
```

### Usage
Search helps locate exploits, scanners, or auxiliary modules related to specific platforms or services.

---

# MYSQL ENUMERATION

## 8. Start PostgreSQL and Initialize Database
Before using database features, start PostgreSQL and initialize the Metasploit database.

```bash
systemctl start postgresql
```

```bash
msfdb init
```

### Usage
Enables Metasploit database support for storing scan and enumeration results.

---

## 9. Scan MySQL Service
Scan port 3306 on the target machine.

```bash
db_nmap -sV -sC -p 3306 <target-ip>
```

### Usage
Detects MySQL service version and runs default NSE scripts for enumeration.

---

## 10. Search for MySQL Auxiliary Modules

```bash
search type:auxiliary mysql
```

### Usage
Lists all MySQL-related auxiliary modules available in Metasploit.

---

## 11. Use MySQL Version Scanner Module

```bash
use auxiliary/scanner/mysql/mysql_version
```

Or:

```bash
use 11
```

### Usage
Loads the MySQL version scanner module to identify MySQL server details.

---

## 12. Set Target IP Address

```bash
set RHOSTS <target-ip>
```

### Usage
Specifies the target machine IP address for scanning.

---

## 13. Configure Password Wordlist

```bash
set PASS_FILE /usr/share/wordlists/rockyou.txt
```

### Usage
Sets the password dictionary file used for brute-force login attempts.

---

## 14. Enable Blank Password Checking

```bash
set BLANK_PASSWORDS true
```

### Usage
Checks whether the MySQL root account has an empty password configured.

---


## OUTPUT:

<img width="712" height="550" alt="image" src="https://github.com/user-attachments/assets/0fe6e2ae-aa14-4cb3-bebc-edb9ada50b04" />
<img width="670" height="773" alt="image" src="https://github.com/user-attachments/assets/e270b80f-4813-4e0b-bbb0-3d6aac093317" />
<img width="688" height="389" alt="image" src="https://github.com/user-attachments/assets/f8eb525f-e50a-4c44-b01b-c86452a8b989" />


## OUTPUT:

<img width="714" height="455" alt="image" src="https://github.com/user-attachments/assets/ca85318a-97fe-4301-a195-e0bc809e0ae0" />


<img width="760" height="669" alt="image" src="https://github.com/user-attachments/assets/0a7cc726-e873-4b9b-9da8-ce6938b9b847" />

<img width="726" height="840" alt="image" src="https://github.com/user-attachments/assets/51c2f119-9dfc-4076-b441-3ed497033dbc" />



<img width="930" height="601" alt="image" src="https://github.com/user-attachments/assets/964d523c-0d08-4743-aa78-ec588543cd7f" />

<img width="768" height="150" alt="image" src="https://github.com/user-attachments/assets/39a04b19-af3f-47d7-bb50-0ad3a72b9b1b" />

<img width="943" height="638" alt="image" src="https://github.com/user-attachments/assets/f800b372-4bff-4c80-a234-11aa3f015b2c" />


<img width="870" height="507" alt="image" src="https://github.com/user-attachments/assets/3c864c5f-9327-41db-aec1-cff476e5c71f" />

<img width="930" height="570" alt="image" src="https://github.com/user-attachments/assets/fe5d2015-fe92-4910-8597-d94667858bae" />

<img width="810" height="180" alt="image" src="https://github.com/user-attachments/assets/a33f7297-ec68-4536-846e-d172c647da5a" />




## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
