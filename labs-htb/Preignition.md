OS: Linux
IP => 10.129.29.94
____
Directory Brute-forcing is a technique used to check a lot of paths on a web server to find hidden pages. Which is another name for this? (i) Local File Inclusion, (ii) dir busting, (iii) hash cracking.
	(II) dir busting


O que o Nmap reporta se o serviço identificado estiver em execução na porta 80/tcp?
	──╼ [★]$ nmap -sV -sS -T5 10.129.29.94
	Starting Nmap 7.94SVN ( https://nmap.org ) at 2026-01-20 18:15 CST
	Nmap scan report for 10.129.29.94
	Host is up (0.075s latency).
	Not shown: 999 closed tcp ports (reset)
	PORT   STATE SERVICE VERSION
	80/tcp open  http    nginx 1.14.2
	
	http

Qual opção usamos para especificar ao Gobuster que queremos realizar a busca de diretórios especificamente?
	Wordlists do **dirbuster & gobuster** - /usr/share/wordlists/dirbuster
	Comando para varrer os diretórios: `gobuster dir -u 10.129.29.94 -w /usr/share/wordlists/dirbuster/directory-list-1.0.txt`


When using gobuster to dir bust, what switch do we add to make sure it finds PHP pages?
	-x php

# With file extensions
gobuster dir -u https://example.com -w wordlist.txt -x php,html,js,txt

# With custom headers and cookies
gobuster dir -u https://example.com -w wordlist.txt -H "Authorization: Bearer token" -c "session=value"

# Show response length
gobuster dir -u https://example.com -w wordlist.txt -l

# Filter by status codes
gobuster dir -u https://example.com -w wordlist.txt -s 200,301,302

What page is found during our dir busting activities?
	/admin.php

What is the HTTP status code reported by Gobuster for the discovered page?
	200

ao acessar se depara com a tela de login
USER=admin
PASS=admin


Flag= 6483bee07c1c1d57f14e5b0717503c73

![[Pasted image 20260120213113.png]]