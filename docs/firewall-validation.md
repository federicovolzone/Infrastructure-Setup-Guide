root@il-mio-server:~# nmap -sV -p- 207.154.205.28
Starting Nmap 7.94SVN ( https://nmap.org ) at 2026-05-28 13:03 UTC
Nmap scan report for il-mio-server (207.154.205.28)
Host is up (0.000011s latency).
Not shown: 65532 closed tcp ports (reset)
PORT     STATE    SERVICE      VERSION
22/tcp   open     ssh          OpenSSH 9.6p1 Ubuntu 3ubuntu13.16 (Ubuntu Linux; protocol 2.0)
2222/tcp filtered EtherNetIP-1
8000/tcp open     http         SimpleHTTPServer 0.6 (Python 3.12.3)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 9.49 seconds
