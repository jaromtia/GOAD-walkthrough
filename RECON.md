# GOAD walkthrough

## Description
This lab was set up using [ludus.cloud](https://docs.ludus.cloud). This will help me practice, research, and most importantly, learn about AD environment and how to do internal pentesting. I will be showing all commands, processes, and resources used to figure out how to access and exploit this environment. This "walkthrough" is more of my personal process of learning how to hack. 

Although there is already a schema for this GOAD environment. I will be treating this as if it is a black box, therefor I will not be referencing any schemas given to me. I will build my own instead


## Initial Discovery

sudo netdiscover -R 10.2.10.0/24
```bash
 Currently scanning: Finished!   |   Screen View: Unique Hosts

 6 Captured ARP Req/Rep packets, from 6 hosts.   Total size: 252
 _____________________________________________________________________________
   IP            At MAC Address     Count     Len  MAC Vendor / Hostname
 -----------------------------------------------------------------------------
 10.2.10.10      bc:24:11:52:92:72      1      42  Unknown vendor
 10.2.10.11      bc:24:11:c0:7e:c9      1      42  Unknown vendor
 10.2.10.12      bc:24:11:6b:17:53      1      42  Unknown vendor
 10.2.10.22      bc:24:11:b4:00:73      1      42  Unknown vendor
 10.2.10.23      bc:24:11:e7:c6:b9      1      42  Unknown vendor
 10.2.10.254     bc:24:11:1d:9c:48      1      42  Unknown vendor

 ```

 nmap 