```bash
 sudo nmap -A -sS -sV -O -p- -T4 --reason -Pn --source-port 4444 10.2.10.10/24
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-11-12 10:15 EST
Nmap scan report for 10.2.10.10
Host is up, received arp-response (0.00048s latency).
Not shown: 65504 closed tcp ports (reset)
PORT      STATE SERVICE       REASON          VERSION
53/tcp    open  domain        syn-ack ttl 128 Simple DNS Plus
80/tcp    open  http          syn-ack ttl 128 Microsoft IIS httpd 10.0
| http-methods:
|_  Potentially risky methods: TRACE
|_http-title: IIS Windows Server
|_http-server-header: Microsoft-IIS/10.0
88/tcp    open  kerberos-sec  syn-ack ttl 128 Microsoft Windows Kerberos (server time: 2024-11-12 15:16:18Z)
135/tcp   open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 128 Microsoft Windows netbios-ssn
389/tcp   open  ldap          syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=kingslanding.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:kingslanding.sevenkingdoms.local
| Not valid before: 2024-11-09T21:19:28
|_Not valid after:  2025-11-09T21:19:28
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
445/tcp   open  microsoft-ds? syn-ack ttl 128
464/tcp   open  kpasswd5?     syn-ack ttl 128
593/tcp   open  ncacn_http    syn-ack ttl 128 Microsoft Windows RPC over HTTP 1.0
636/tcp   open  ssl/ldap      syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=kingslanding.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:kingslanding.sevenkingdoms.local
| Not valid before: 2024-11-09T21:19:28
|_Not valid after:  2025-11-09T21:19:28
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
3268/tcp  open  ldap          syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=kingslanding.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:kingslanding.sevenkingdoms.local
| Not valid before: 2024-11-09T21:19:28
|_Not valid after:  2025-11-09T21:19:28
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
3269/tcp  open  ssl/ldap      syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=kingslanding.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:kingslanding.sevenkingdoms.local
| Not valid before: 2024-11-09T21:19:28
|_Not valid after:  2025-11-09T21:19:28
3389/tcp  open  ms-wbt-server syn-ack ttl 128 Microsoft Terminal Services
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=kingslanding.sevenkingdoms.local
| Not valid before: 2024-11-08T20:41:36
|_Not valid after:  2025-05-10T20:41:36
5985/tcp  open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
5986/tcp  open  ssl/http      syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| tls-alpn:
|_  http/1.1
| ssl-cert: Subject: commonName=WIN2019-SRV-X64
| Subject Alternative Name: DNS:WIN2019-SRV-X64, DNS:WIN2019-SRV-X64
| Not valid before: 2024-11-07T19:54:57
|_Not valid after:  2034-11-05T19:54:57
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
9389/tcp  open  mc-nmf        syn-ack ttl 128 .NET Message Framing
47001/tcp open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49664/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49665/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49666/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49672/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49675/tcp open  ncacn_http    syn-ack ttl 128 Microsoft Windows RPC over HTTP 1.0
49676/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49679/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49680/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49685/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49702/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49718/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49777/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
MAC Address: BC:24:11:52:92:72 (Unknown)
Device type: general purpose
Running: Microsoft Windows 2019
OS details: Microsoft Windows Server 2019
Network Distance: 1 hop
Service Info: Host: KINGSLANDING; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode:
|   3:1:1:
|_    Message signing enabled and required
|_nbstat: NetBIOS name: KINGSLANDING, NetBIOS user: <unknown>, NetBIOS MAC: bc:24:11:52:92:72 (unknown)
| smb2-time:
|   date: 2024-11-12T15:19:07
|_  start_date: N/A
|_clock-skew: mean: -3s, deviation: 0s, median: -3s

TRACEROUTE
HOP RTT     ADDRESS
1   0.48 ms 10.2.10.10

Nmap scan report for 10.2.10.11
Host is up, received arp-response (0.00043s latency).
Not shown: 65506 closed tcp ports (reset)
PORT      STATE SERVICE       REASON          VERSION
53/tcp    open  domain        syn-ack ttl 128 Simple DNS Plus
88/tcp    open  kerberos-sec  syn-ack ttl 128 Microsoft Windows Kerberos (server time: 2024-11-12 15:16:24Z)
135/tcp   open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 128 Microsoft Windows netbios-ssn
389/tcp   open  ldap          syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=winterfell.north.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:winterfell.north.sevenkingdoms.local
| Not valid before: 2024-11-10T05:57:19
|_Not valid after:  2025-11-10T05:57:19
445/tcp   open  microsoft-ds? syn-ack ttl 128
464/tcp   open  kpasswd5?     syn-ack ttl 128
593/tcp   open  ncacn_http    syn-ack ttl 128 Microsoft Windows RPC over HTTP 1.0
636/tcp   open  ssl/ldap      syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=winterfell.north.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:winterfell.north.sevenkingdoms.local
| Not valid before: 2024-11-10T05:57:19
|_Not valid after:  2025-11-10T05:57:19
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
3268/tcp  open  ldap          syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=winterfell.north.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:winterfell.north.sevenkingdoms.local
| Not valid before: 2024-11-10T05:57:19
|_Not valid after:  2025-11-10T05:57:19
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
3269/tcp  open  ssl/ldap      syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: sevenkingdoms.local0., Site: Default-First-Site-Name)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=winterfell.north.sevenkingdoms.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:winterfell.north.sevenkingdoms.local
| Not valid before: 2024-11-10T05:57:19
|_Not valid after:  2025-11-10T05:57:19
3389/tcp  open  ms-wbt-server syn-ack ttl 128 Microsoft Terminal Services
| ssl-cert: Subject: commonName=winterfell.north.sevenkingdoms.local
| Not valid before: 2024-11-08T20:54:17
|_Not valid after:  2025-05-10T20:54:17
| rdp-ntlm-info:
|   Target_Name: NORTH
|   NetBIOS_Domain_Name: NORTH
|   NetBIOS_Computer_Name: WINTERFELL
|   DNS_Domain_Name: north.sevenkingdoms.local
|   DNS_Computer_Name: winterfell.north.sevenkingdoms.local
|   DNS_Tree_Name: sevenkingdoms.local
|   Product_Version: 10.0.17763
|_  System_Time: 2024-11-12T15:19:11+00:00
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
5985/tcp  open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
5986/tcp  open  ssl/http      syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
| tls-alpn:
|_  http/1.1
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
| ssl-cert: Subject: commonName=WIN2019-SRV-X64
| Subject Alternative Name: DNS:WIN2019-SRV-X64, DNS:WIN2019-SRV-X64
| Not valid before: 2024-11-07T19:54:57
|_Not valid after:  2034-11-05T19:54:57
9389/tcp  open  mc-nmf        syn-ack ttl 128 .NET Message Framing
47001/tcp open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49664/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49665/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49666/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49669/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49672/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49675/tcp open  ncacn_http    syn-ack ttl 128 Microsoft Windows RPC over HTTP 1.0
49676/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49681/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49682/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49687/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49711/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49819/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
MAC Address: BC:24:11:C0:7E:C9 (Unknown)
Device type: general purpose
Running: Microsoft Windows 2019
OS details: Microsoft Windows Server 2019
Network Distance: 1 hop
Service Info: Host: WINTERFELL; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode:
|   3:1:1:
|_    Message signing enabled and required
|_clock-skew: mean: -3s, deviation: 0s, median: -3s
|_nbstat: NetBIOS name: WINTERFELL, NetBIOS user: <unknown>, NetBIOS MAC: bc:24:11:c0:7e:c9 (unknown)
| smb2-time:
|   date: 2024-11-12T15:19:11
|_  start_date: N/A

TRACEROUTE
HOP RTT     ADDRESS
1   0.43 ms 10.2.10.11

Nmap scan report for 10.2.10.12
Host is up, received arp-response (0.00036s latency).
Not shown: 65508 closed tcp ports (reset)
PORT      STATE SERVICE       REASON          VERSION
53/tcp    open  domain        syn-ack ttl 128 Simple DNS Plus
88/tcp    open  kerberos-sec  syn-ack ttl 128 Microsoft Windows Kerberos (server time: 2024-11-12 15:16:46Z)
135/tcp   open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 128 Microsoft Windows netbios-ssn
389/tcp   open  ldap          syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: essos.local, Site: Default-First-Site-Name)
| ssl-cert: Subject: commonName=meereen.essos.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:meereen.essos.local
| Not valid before: 2024-11-09T21:19:49
|_Not valid after:  2025-11-09T21:19:49
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
445/tcp   open  microsoft-ds  syn-ack ttl 128 Windows Server 2016 Standard Evaluation 14393 microsoft-ds (workgroup: ESSOS)
464/tcp   open  kpasswd5?     syn-ack ttl 128
593/tcp   open  ncacn_http    syn-ack ttl 128 Microsoft Windows RPC over HTTP 1.0
636/tcp   open  ssl/ldap      syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: essos.local, Site: Default-First-Site-Name)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=meereen.essos.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:meereen.essos.local
| Not valid before: 2024-11-09T21:19:49
|_Not valid after:  2025-11-09T21:19:49
3268/tcp  open  ldap          syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: essos.local, Site: Default-First-Site-Name)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=meereen.essos.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:meereen.essos.local
| Not valid before: 2024-11-09T21:19:49
|_Not valid after:  2025-11-09T21:19:49
3269/tcp  open  ssl/ldap      syn-ack ttl 128 Microsoft Windows Active Directory LDAP (Domain: essos.local, Site: Default-First-Site-Name)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=meereen.essos.local
| Subject Alternative Name: othername: 1.3.6.1.4.1.311.25.1::<unsupported>, DNS:meereen.essos.local
| Not valid before: 2024-11-09T21:19:49
|_Not valid after:  2025-11-09T21:19:49
3389/tcp  open  ms-wbt-server syn-ack ttl 128 Microsoft Terminal Services
| rdp-ntlm-info:
|   Target_Name: ESSOS
|   NetBIOS_Domain_Name: ESSOS
|   NetBIOS_Computer_Name: MEEREEN
|   DNS_Domain_Name: essos.local
|   DNS_Computer_Name: meereen.essos.local
|   DNS_Tree_Name: essos.local
|   Product_Version: 10.0.14393
|_  System_Time: 2024-11-12T15:19:06+00:00
| ssl-cert: Subject: commonName=meereen.essos.local
| Not valid before: 2024-11-08T20:41:40
|_Not valid after:  2025-05-10T20:41:40
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
5985/tcp  open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
5986/tcp  open  ssl/http      syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
| ssl-cert: Subject: commonName=WIN2016-SRV-X64
| Subject Alternative Name: DNS:WIN2016-SRV-X64, DNS:WIN2016-SRV-X64
| Not valid before: 2024-11-07T19:37:09
|_Not valid after:  2034-11-05T19:37:09
| tls-alpn:
|   h2
|_  http/1.1
|_http-server-header: Microsoft-HTTPAPI/2.0
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
9389/tcp  open  mc-nmf        syn-ack ttl 128 .NET Message Framing
47001/tcp open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49664/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49665/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49666/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49669/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49670/tcp open  ncacn_http    syn-ack ttl 128 Microsoft Windows RPC over HTTP 1.0
49671/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49674/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49679/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49696/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49747/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
MAC Address: BC:24:11:6B:17:53 (Unknown)
No exact OS matches for host (If you know what OS is running on it, see https://nmap.org/submit/ ).
TCP/IP fingerprint:
OS:SCAN(V=7.94SVN%E=4%D=11/12%OT=53%CT=1%CU=38419%PV=Y%DS=1%DC=D%G=Y%M=BC24
OS:11%TM=673371FD%P=x86_64-pc-linux-gnu)SEQ(SP=109%GCD=1%ISR=106%TI=I%CI=I%
OS:II=I%SS=S%TS=A)SEQ(SP=109%GCD=4%ISR=106%TI=I%CI=I%II=I%SS=S%TS=A)OPS(O1=
OS:M5B4NW8ST11%O2=M5B4NW8ST11%O3=M5B4NW8NNT11%O4=M5B4NW8ST11%O5=M5B4NW8ST11
OS:%O6=M5B4ST11)WIN(W1=2000%W2=2000%W3=2000%W4=2000%W5=2000%W6=2000)ECN(R=Y
OS:%DF=Y%T=80%W=2000%O=M5B4NW8NNS%CC=Y%Q=)T1(R=Y%DF=Y%T=80%S=O%A=S+%F=AS%RD
OS:=0%Q=)T2(R=Y%DF=Y%T=80%W=0%S=Z%A=S%F=AR%O=%RD=0%Q=)T3(R=Y%DF=Y%T=80%W=0%
OS:S=Z%A=O%F=AR%O=%RD=0%Q=)T4(R=Y%DF=Y%T=80%W=0%S=A%A=O%F=R%O=%RD=0%Q=)T5(R
OS:=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)T6(R=Y%DF=Y%T=80%W=0%S=A%A=O%F
OS:=R%O=%RD=0%Q=)T7(R=Y%DF=Y%T=80%W=0%S=Z%A=S+%F=AR%O=%RD=0%Q=)U1(R=Y%DF=N%
OS:T=80%IPL=164%UN=0%RIPL=G%RID=G%RIPCK=G%RUCK=G%RUD=G)IE(R=Y%DFI=N%T=80%CD
OS:=Z)

Network Distance: 1 hop
Service Info: Host: MEEREEN; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb-os-discovery:
|   OS: Windows Server 2016 Standard Evaluation 14393 (Windows Server 2016 Standard Evaluation 6.3)
|   Computer name: meereen
|   NetBIOS computer name: MEEREEN\x00
|   Domain name: essos.local
|   Forest name: essos.local
|   FQDN: meereen.essos.local
|_  System time: 2024-11-12T10:19:09-05:00
| smb2-time:
|   date: 2024-11-12T15:19:07
|_  start_date: 2024-11-09T22:07:11
|_nbstat: NetBIOS name: MEEREEN, NetBIOS user: <unknown>, NetBIOS MAC: bc:24:11:6b:17:53 (unknown)
| smb2-security-mode:
|   3:1:1:
|_    Message signing enabled and required
|_clock-skew: mean: 29m57s, deviation: 1h34m53s, median: -3s
| smb-security-mode:
|   account_used: <blank>
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: required

TRACEROUTE
HOP RTT     ADDRESS
1   0.35 ms 10.2.10.12

Nmap scan report for 10.2.10.22
Host is up, received arp-response (0.00043s latency).
Not shown: 65516 closed tcp ports (reset)
PORT      STATE SERVICE       REASON          VERSION
80/tcp    open  http          syn-ack ttl 128 Microsoft IIS httpd 10.0
| http-methods:
|_  Potentially risky methods: TRACE
|_http-title: Site doesn't have a title (text/html).
|_http-server-header: Microsoft-IIS/10.0
135/tcp   open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 128 Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds? syn-ack ttl 128
1433/tcp  open  ms-sql-s      syn-ack ttl 128 Microsoft SQL Server 2019 15.00.2000.00; RTM
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ms-sql-ntlm-info:
|   10.2.10.22:1433:
|     Target_Name: NORTH
|     NetBIOS_Domain_Name: NORTH
|     NetBIOS_Computer_Name: CASTELBLACK
|     DNS_Domain_Name: north.sevenkingdoms.local
|     DNS_Computer_Name: castelblack.north.sevenkingdoms.local
|     DNS_Tree_Name: sevenkingdoms.local
|_    Product_Version: 10.0.17763
| ms-sql-info:
|   10.2.10.22:1433:
|     Version:
|       name: Microsoft SQL Server 2019 RTM
|       number: 15.00.2000.00
|       Product: Microsoft SQL Server 2019
|       Service pack level: RTM
|       Post-SP patches applied: false
|_    TCP port: 1433
| ssl-cert: Subject: commonName=SSL_Self_Signed_Fallback
| Not valid before: 2024-11-09T22:07:11
|_Not valid after:  2054-11-09T22:07:11
3389/tcp  open  ms-wbt-server syn-ack ttl 128 Microsoft Terminal Services
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=castelblack.north.sevenkingdoms.local
| Not valid before: 2024-11-08T21:08:34
|_Not valid after:  2025-05-10T21:08:34
5985/tcp  open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
5986/tcp  open  ssl/http      syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
| tls-alpn:
|_  http/1.1
| ssl-cert: Subject: commonName=WIN2019-SRV-X64
| Subject Alternative Name: DNS:WIN2019-SRV-X64, DNS:WIN2019-SRV-X64
| Not valid before: 2024-11-07T19:54:57
|_Not valid after:  2034-11-05T19:54:57
47001/tcp open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
49664/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49665/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49666/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49669/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49670/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49671/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49672/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49802/tcp open  ms-sql-s      syn-ack ttl 128 Microsoft SQL Server 2019 15.00.2000.00; RTM
| ms-sql-ntlm-info:
|   10.2.10.22:49802:
|     Target_Name: NORTH
|     NetBIOS_Domain_Name: NORTH
|     NetBIOS_Computer_Name: CASTELBLACK
|     DNS_Domain_Name: north.sevenkingdoms.local
|     DNS_Computer_Name: castelblack.north.sevenkingdoms.local
|     DNS_Tree_Name: sevenkingdoms.local
|_    Product_Version: 10.0.17763
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ms-sql-info:
|   10.2.10.22:49802:
|     Version:
|       name: Microsoft SQL Server 2019 RTM
|       number: 15.00.2000.00
|       Product: Microsoft SQL Server 2019
|       Service pack level: RTM
|       Post-SP patches applied: false
|_    TCP port: 49802
| ssl-cert: Subject: commonName=SSL_Self_Signed_Fallback
| Not valid before: 2024-11-09T22:07:11
|_Not valid after:  2054-11-09T22:07:11
MAC Address: BC:24:11:B4:00:73 (Unknown)
Device type: general purpose
Running: Microsoft Windows 2019
OS details: Microsoft Windows Server 2019
Network Distance: 1 hop
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode:
|   3:1:1:
|_    Message signing enabled but not required
|_clock-skew: mean: -2s, deviation: 0s, median: -3s
| smb2-time:
|   date: 2024-11-12T15:19:12
|_  start_date: N/A
|_nbstat: NetBIOS name: CASTELBLACK, NetBIOS user: <unknown>, NetBIOS MAC: bc:24:11:b4:00:73 (unknown)

TRACEROUTE
HOP RTT     ADDRESS
1   0.43 ms 10.2.10.22

Nmap scan report for 10.2.10.23
Host is up, received arp-response (0.00040s latency).
Not shown: 65515 closed tcp ports (reset)
PORT      STATE SERVICE       REASON          VERSION
80/tcp    open  http          syn-ack ttl 128 Microsoft IIS httpd 10.0
| http-methods:
|_  Potentially risky methods: TRACE
|_http-server-header: Microsoft-IIS/10.0
|_http-title: IIS Windows Server
135/tcp   open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
139/tcp   open  netbios-ssn   syn-ack ttl 128 Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds? syn-ack ttl 128
1433/tcp  open  ms-sql-s      syn-ack ttl 128 Microsoft SQL Server 2019 15.00.2000.00; RTM
| ssl-cert: Subject: commonName=SSL_Self_Signed_Fallback
| Not valid before: 2024-11-09T22:07:12
|_Not valid after:  2054-11-09T22:07:12
| ms-sql-info:
|   10.2.10.23:1433:
|     Version:
|       name: Microsoft SQL Server 2019 RTM
|       number: 15.00.2000.00
|       Product: Microsoft SQL Server 2019
|       Service pack level: RTM
|       Post-SP patches applied: false
|_    TCP port: 1433
| ms-sql-ntlm-info:
|   10.2.10.23:1433:
|     Target_Name: ESSOS
|     NetBIOS_Domain_Name: ESSOS
|     NetBIOS_Computer_Name: BRAAVOS
|     DNS_Domain_Name: essos.local
|     DNS_Computer_Name: braavos.essos.local
|     DNS_Tree_Name: essos.local
|_    Product_Version: 10.0.17763
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
3389/tcp  open  ms-wbt-server syn-ack ttl 128 Microsoft Terminal Services
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=braavos.essos.local
| Not valid before: 2024-11-08T21:08:34
|_Not valid after:  2025-05-10T21:08:34
5985/tcp  open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
5986/tcp  open  ssl/http      syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
| tls-alpn:
|_  http/1.1
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
|_http-server-header: Microsoft-HTTPAPI/2.0
|_http-title: Not Found
| ssl-cert: Subject: commonName=WIN2019-SRV-X64
| Subject Alternative Name: DNS:WIN2019-SRV-X64, DNS:WIN2019-SRV-X64
| Not valid before: 2024-11-07T19:54:57
|_Not valid after:  2034-11-05T19:54:57
47001/tcp open  http          syn-ack ttl 128 Microsoft HTTPAPI httpd 2.0 (SSDP/UPnP)
|_http-title: Not Found
|_http-server-header: Microsoft-HTTPAPI/2.0
49664/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49665/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49666/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49667/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49668/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49669/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49670/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49671/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49672/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49735/tcp open  msrpc         syn-ack ttl 128 Microsoft Windows RPC
49876/tcp open  ms-sql-s      syn-ack ttl 128 Microsoft SQL Server 2019 15.00.2000.00; RTM
| ms-sql-info:
|   10.2.10.23:49876:
|     Version:
|       name: Microsoft SQL Server 2019 RTM
|       number: 15.00.2000.00
|       Product: Microsoft SQL Server 2019
|       Service pack level: RTM
|       Post-SP patches applied: false
|_    TCP port: 49876
|_ssl-date: 2024-11-12T15:19:21+00:00; -3s from scanner time.
| ssl-cert: Subject: commonName=SSL_Self_Signed_Fallback
| Not valid before: 2024-11-09T22:07:12
|_Not valid after:  2054-11-09T22:07:12
| ms-sql-ntlm-info:
|   10.2.10.23:49876:
|     Target_Name: ESSOS
|     NetBIOS_Domain_Name: ESSOS
|     NetBIOS_Computer_Name: BRAAVOS
|     DNS_Domain_Name: essos.local
|     DNS_Computer_Name: braavos.essos.local
|     DNS_Tree_Name: essos.local
|_    Product_Version: 10.0.17763
MAC Address: BC:24:11:E7:C6:B9 (Unknown)
Device type: general purpose
Running: Microsoft Windows 2019
OS details: Microsoft Windows Server 2019
Network Distance: 1 hop
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode:
|   3:1:1:
|_    Message signing enabled but not required
| smb2-time:
|   date: 2024-11-12T15:19:10
|_  start_date: N/A
|_nbstat: NetBIOS name: BRAAVOS, NetBIOS user: <unknown>, NetBIOS MAC: bc:24:11:e7:c6:b9 (unknown)
|_clock-skew: mean: -3s, deviation: 0s, median: -3s

TRACEROUTE
HOP RTT     ADDRESS
1   0.40 ms 10.2.10.23

Nmap scan report for 10.2.10.254
Host is up, received arp-response (0.00034s latency).
Not shown: 65532 closed tcp ports (reset)
PORT     STATE    SERVICE     REASON              VERSION
22/tcp   filtered ssh         port-unreach ttl 64
53/tcp   open     domain      syn-ack ttl 64      Unbound
3000/tcp open     nagios-nsca syn-ack ttl 64      Nagios NSCA
MAC Address: BC:24:11:1D:9C:48 (Unknown)
Device type: general purpose
Running: Linux 4.X|5.X
OS CPE: cpe:/o:linux:linux_kernel:4 cpe:/o:linux:linux_kernel:5
OS details: Linux 4.15 - 5.8
Network Distance: 1 hop

TRACEROUTE
HOP RTT     ADDRESS
1   0.34 ms 10.2.10.254

Nmap scan report for JD-kali (10.2.10.99)
Host is up, received user-set (0.000033s latency).
Not shown: 65529 closed tcp ports (reset)
PORT      STATE SERVICE          REASON         VERSION
22/tcp    open  ssh              syn-ack ttl 64 OpenSSH 9.9p1 Debian 3 (protocol 2.0)
| ssh-hostkey:
|   256 08:74:c5:3c:73:a1:48:fe:6c:79:a1:0b:5e:88:6b:c7 (ECDSA)
|_  256 04:9b:11:ab:9a:2d:53:a4:c1:32:93:0e:2f:3b:74:16 (ED25519)
443/tcp   open  ssl/https        syn-ack ttl 64
| http-title: Wazuh
|_Requested resource was /app/login?
| tls-alpn:
|_  http/1.1
| fingerprint-strings:
|   FourOhFourRequest:
|     HTTP/1.1 401 Unauthorized
|     osd-name: JD-kali
|     x-frame-options: sameorigin
|     content-type: application/json; charset=utf-8
|     cache-control: private, no-cache, no-store, must-revalidate
|     set-cookie: security_authentication=; Max-Age=0; Expires=Thu, 01 Jan 1970 00:00:00 GMT; Secure; HttpOnly; Path=/
|     content-length: 77
|     Date: Tue, 12 Nov 2024 15:19:38 GMT
|     Connection: close
|     {"statusCode":401,"error":"Unauthorized","message":"Authentication required"}
|   GetRequest:
|     HTTP/1.1 302 Found
|     location: /app/login?
|     osd-name: JD-kali
|     x-frame-options: sameorigin
|     cache-control: private, no-cache, no-store, must-revalidate
|     set-cookie: security_authentication=; Max-Age=0; Expires=Thu, 01 Jan 1970 00:00:00 GMT; Secure; HttpOnly; Path=/
|     content-length: 0
|     Date: Tue, 12 Nov 2024 15:19:38 GMT
|     Connection: close
|   HTTPOptions:
|     HTTP/1.1 404 Not Found
|     osd-name: JD-kali
|     x-frame-options: sameorigin
|     content-type: application/json; charset=utf-8
|     cache-control: private, no-cache, no-store, must-revalidate
|     content-length: 60
|     Date: Tue, 12 Nov 2024 15:19:38 GMT
|     Connection: close
|     {"statusCode":404,"error":"Not Found","message":"Not Found"}
|   RPCCheck, tor-versions:
|     HTTP/1.1 400 Bad Request
|   RTSPRequest:
|     HTTP/1.1 404 Not Found
|     osd-name: JD-kali
|     x-frame-options: sameorigin
|     content-type: application/json; charset=utf-8
|     cache-control: private, no-cache, no-store, must-revalidate
|     content-length: 60
|     Date: Tue, 12 Nov 2024 15:19:43 GMT
|     Connection: close
|_    {"statusCode":404,"error":"Not Found","message":"Not Found"}
| ssl-cert: Subject: commonName=wazuh-dashboard/organizationName=Wazuh/countryName=US
| Subject Alternative Name: IP Address:127.0.0.1
| Not valid before: 2024-11-09T16:21:12
|_Not valid after:  2034-11-07T16:21:12
|_ssl-date: TLS randomness does not represent time
1514/tcp  open  fujitsu-dtcns?   syn-ack ttl 64
1515/tcp  open  tcpwrapped       syn-ack ttl 64
8444/tcp  open  ssl/pcsync-http? syn-ack ttl 64
|_ssl-date: TLS randomness does not represent time
| ssl-cert: Subject: commonName=kali
| Subject Alternative Name: DNS:kali
| Not valid before: 2024-11-08T16:17:28
|_Not valid after:  2034-11-06T16:17:28
55000/tcp open  unknown          syn-ack ttl 64
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port443-TCP:V=7.94SVN%T=SSL%I=7%D=11/12%Time=6733720A%P=x86_64-pc-linux
SF:-gnu%r(GetRequest,157,"HTTP/1\.1\x20302\x20Found\r\nlocation:\x20/app/l
SF:ogin\?\r\nosd-name:\x20JD-kali\r\nx-frame-options:\x20sameorigin\r\ncac
SF:he-control:\x20private,\x20no-cache,\x20no-store,\x20must-revalidate\r\
SF:nset-cookie:\x20security_authentication=;\x20Max-Age=0;\x20Expires=Thu,
SF:\x2001\x20Jan\x201970\x2000:00:00\x20GMT;\x20Secure;\x20HttpOnly;\x20Pa
SF:th=/\r\ncontent-length:\x200\r\nDate:\x20Tue,\x2012\x20Nov\x202024\x201
SF:5:19:38\x20GMT\r\nConnection:\x20close\r\n\r\n")%r(HTTPOptions,13E,"HTT
SF:P/1\.1\x20404\x20Not\x20Found\r\nosd-name:\x20JD-kali\r\nx-frame-option
SF:s:\x20sameorigin\r\ncontent-type:\x20application/json;\x20charset=utf-8
SF:\r\ncache-control:\x20private,\x20no-cache,\x20no-store,\x20must-revali
SF:date\r\ncontent-length:\x2060\r\nDate:\x20Tue,\x2012\x20Nov\x202024\x20
SF:15:19:38\x20GMT\r\nConnection:\x20close\r\n\r\n{\"statusCode\":404,\"er
SF:ror\":\"Not\x20Found\",\"message\":\"Not\x20Found\"}")%r(FourOhFourRequ
SF:est,1C4,"HTTP/1\.1\x20401\x20Unauthorized\r\nosd-name:\x20JD-kali\r\nx-
SF:frame-options:\x20sameorigin\r\ncontent-type:\x20application/json;\x20c
SF:harset=utf-8\r\ncache-control:\x20private,\x20no-cache,\x20no-store,\x2
SF:0must-revalidate\r\nset-cookie:\x20security_authentication=;\x20Max-Age
SF:=0;\x20Expires=Thu,\x2001\x20Jan\x201970\x2000:00:00\x20GMT;\x20Secure;
SF:\x20HttpOnly;\x20Path=/\r\ncontent-length:\x2077\r\nDate:\x20Tue,\x2012
SF:\x20Nov\x202024\x2015:19:38\x20GMT\r\nConnection:\x20close\r\n\r\n{\"st
SF:atusCode\":401,\"error\":\"Unauthorized\",\"message\":\"Authentication\
SF:x20required\"}")%r(tor-versions,1C,"HTTP/1\.1\x20400\x20Bad\x20Request\
SF:r\n\r\n")%r(RTSPRequest,13E,"HTTP/1\.1\x20404\x20Not\x20Found\r\nosd-na
SF:me:\x20JD-kali\r\nx-frame-options:\x20sameorigin\r\ncontent-type:\x20ap
SF:plication/json;\x20charset=utf-8\r\ncache-control:\x20private,\x20no-ca
SF:che,\x20no-store,\x20must-revalidate\r\ncontent-length:\x2060\r\nDate:\
SF:x20Tue,\x2012\x20Nov\x202024\x2015:19:43\x20GMT\r\nConnection:\x20close
SF:\r\n\r\n{\"statusCode\":404,\"error\":\"Not\x20Found\",\"message\":\"No
SF:t\x20Found\"}")%r(RPCCheck,1C,"HTTP/1\.1\x20400\x20Bad\x20Request\r\n\r
SF:\n");
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6.32
OS details: Linux 2.6.32
Network Distance: 0 hops
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Post-scan script results:
| clock-skew:
|   -3s:
|     10.2.10.23
|     10.2.10.22
|     10.2.10.10
|     10.2.10.11
|_    10.2.10.12
OS and Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 256 IP addresses (7 hosts up) scanned in 363.83 seconds
```