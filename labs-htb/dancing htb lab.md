OS Windows 

SMB -> Server Message Block

┌─[✗]─[root@htb-2vpcpdop5g]─[/home/kaiky0ffsec/Desktop]
└──╼ #nmap -sS -O -sV 10.129.97.160
Starting Nmap 7.94SVN ( https://nmap.org ) at 2026-01-19 18:36 CST
Nmap scan report for 10.129.97.160
Host is up (0.0091s latency).
Not shown: 997 closed tcp ports (reset)
PORT    STATE SERVICE       VERSION
135/tcp open  msrpc         Microsoft Windows RPC
139/tcp open  netbios-ssn   Microsoft Windows netbios-ssn
445/tcp open  microsoft-ds? =: SMB Port
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=1/19%OT=135%CT=1%CU=34876%PV=Y%DS=2%DC=I%G=Y%TM=696
OS:ECE1D%P=x86_64-pc-linux-gnu)SEQ(SP=101%GCD=1%ISR=10F%TI=I%CI=I%TS=U)SEQ(
OS:SP=101%GCD=1%ISR=10F%TI=I%CI=I%II=I%SS=S%TS=U)OPS(O1=M552NW8NNS%O2=M552N
OS:W8NNS%O3=M552NW8%O4=M552NW8NNS%O5=M552NW8NNS%O6=M552NNS)WIN(W1=FFFF%W2=F
OS:FFF%W3=FFFF%W4=FFFF%W5=FFFF%W6=FF70)ECN(R=Y%DF=Y%T=80%W=FFFF%O=M552NW8NN
OS:S%CC=Y%Q=)T1(R=Y%DF=Y%T=80%S=O%A=S+%F=AS%RD=0%Q=)T2(R=Y%DF=Y%T=80%W=0%S=
OS:Z%A=S%F=AR%O=%RD=0%Q=)T3(R=Y%DF=Y%T=80%W=0%S=Z%A=O%F=AR%O=%RD=0%Q=)T4(R=
OS:Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD=0%Q=)T5(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=A
OS:R%O=%RD=0%Q=)T6(R=Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=8
OS:0%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%DF=N%T=80%IPL=164%UN=0%RIPL=G%RID=
OS:G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=80%CD=Z)

Network Distance: 2 hops
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 17.38 seconds


smbclient -I 10.129.97.160 -L

What is the 'flag' or 'switch' that we can use with the smbclient utility to 'list' the available shares on Dancing?
	-L (list)

`smbclient \\\\10.129.97.160\\WorkShares (acesso sem precisar inserir senha)`

