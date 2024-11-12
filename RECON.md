# Reconnaisance
## Initial Discovery


### Netdiscover
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

### Nmap

[Nmap results](./results/nmap-results.md) (nmap -A -sS -sV -O -p- -T4 --reason -Pn --source-port 4444 10.2.10.10/24)

Explanation of the options:
- **A**: Enables OS detection, version detection, script scanning, and traceroute.
- **sS**: Performs a TCP SYN scan (stealth scan).
- **sV**: Detects service versions.
- **O**: Enables OS detection.
- **p**-: Scans all 65535 ports.
- **T4**: Sets the speed template to a faster scan (T4) while balancing accuracy.
- **--reason**: Shows the reason Nmap believes a port is open, closed, or filtered.
- **Pn**: Skips host discovery, assuming all hosts are up.
- **--source-port 4444**: Sets the source port to 4444, which can sometimes bypass certain firewall rules.