OS: Windows
IP => 10.129.29.91

What does the 3-letter acronym RDP stand for?
	RDP => Remote Desktop Protocol
	
What is a 3-letter acronym that refers to interaction with the host through a command line interface?
	CLI
	
What about graphical user interface interactions?
	GUI

What is the name of an old remote access tool that came without encryption by default and listens on TCP port 23?
	telnet

What is the name of the service running on port 3389 TCP?
### nmap scan
	PORT     STATE SERVICE       REASON          VERSION
135/tcp  open  msrpc         syn-ack ttl 127 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 127 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds? syn-ack ttl 127
3389/tcp open  ms-wbt-server syn-ack ttl 127 Microsoft Terminal Services
OS fingerprint not ideal because: Timing level 5 (Insane) used
Aggressive OS guesses: Microsoft Windows Server 2019 (96%), Microsoft Windows 10 1709 - 1909 (93%), Microsoft Windows Server 2012 (92%), Microsoft Windows Vista SP1 (92%), Microsoft Windows Longhorn (91%), Microsoft Windows 10 1809 - 2004 (91%), Microsoft Windows Server 2012 R2 (91%), Microsoft Windows Server 2012 R2 Update 1 (91%), Microsoft Windows Server 2016 build 10586 - 14393 (91%), Microsoft Windows 7, Windows Server 2012, or Windows 8.1 Update 1 (91%)
No exact OS matches for host (test conditions non-ideal).
TCP/IP fingerprint:
SCAN(V=7.94SVN%E=4%D=1/20%OT=135%CT=1%CU=41404%PV=Y%DS=2%DC=I%G=N%TM=6970155D%P=x86_64-pc-linux-gnu)
SEQ(SP=103%GCD=1%ISR=106%TI=I%CI=I%II=I%SS=S%TS=U)
OPS(O1=M552NW8NNS%O2=M552NW8NNS%O3=M552NW8%O4=M552NW8NNS%O5=M552NW8NNS%O6=M552NNS)
WIN(W1=FFFF%W2=FFFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)
ECN(R=Y%DF=Y%T=80%W=FFFF%O=M552NW8NNS%CC=Y%Q=)
T1(R=Y%DF=Y%T=80%S=O%A=S+%F=AS%RD=0%Q=)
T2(R=Y%DF=Y%T=80%W=0%S=Z%A=S%F=AR%O=%RD=0%Q=)
T3(R=Y%DF=Y%T=80%W=0%S=Z%A=O%F=AR%O=%RD=0%Q=)
T4(R=Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD=0%Q=)
T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
T6(R=Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD=0%Q=)
T7(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)
U1(R=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)
IE(R=Y%DFI=N%T=80%CD=Z)

Network Distance: 2 hops
TCP Sequence Prediction: Difficulty=259 (Good luck!)
IP ID Sequence Generation: Incremental
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

What is the switch used to specify the target host's IP address when using xfreerdp?
	/client-hostname:name
       /proxy:[proto://][user:password@]host:port
           Server hostname
           Connect to host rdp.contoso.com with user USER and a size of 50
           Connect to host rdp.contoso.com with user CONTOSO\\JohnDoe and
           Connect to host 192.168.1.100 on port 4489 with user JohnDoe,
           Establish a connection to host 192.168.1.100 with user JohnDoe,
           
	─[us-starting-point-vip-1-dhcp]─[10.10.15.3]─[kaiky0ffsec@htb-od9wywk5s8]─[~]
	└──╼ [★]$ man xfreerdp | grep "/v:"
       xfreerdp [file] [options] [/v:server[:port]]
       /v:server[:port]
       xfreerdp /u:USER /size:50%h /v:rdp.contoso.com
       xfreerdp /u:CONTOSO\\JohnDoe /p:Pwd123! /v:rdp.contoso.com
       xfreerdp /u:JohnDoe /p:Pwd123! /w:1366 /h:768 /v:192.168.1.100:4489
       xfreerdp /u:JohnDoe /p:Pwd123! /vmconnect:C824F53E-95D2-46C6-9A18-23A5BB403532 /v:192.168.1.100


What username successfully returns a desktop projection to us with a blank password?
	xfreerdp /v:10.129.29.91:3389 /u:Administrator
[18:07:02:698] [35677:35678] [WARN][com.freerdp.crypto] - Certificate verification failure 'self-signed certificate (18)' at stack position 0
[18:07:02:698] [35677:35678] [WARN][com.freerdp.crypto] - CN = Explosion
Password: 
[18:07:05:432] [35677:35678] [ERROR][com.winpr.timezone] - Unable to find a match for unix timezone: US/Central
[18:07:06:933] [35677:35678] [INFO][com.freerdp.gdi] - Local framebuffer format  PIXEL_FORMAT_BGRX32
[18:07:06:933] [35677:35678] [INFO][com.freerdp.gdi] - Remote framebuffer format PIXEL_FORMAT_BGRA32
[18:07:06:949] [35677:35678] [INFO][com.freerdp.channels.rdpsnd.client] - [static] Loaded fake backend for rdpsnd
[18:07:06:949] [35677:35678] [INFO][com.freerdp.channels.drdynvc.client] - Loading Dynamic Virtual Channel rdpgfx

User administrator entra com a senha vazia
![[Pasted image 20260120210809.png]]

Flag = 951fa96d7830c451b536be5a6be008a0

![[Pasted image 20260120210858.png]]