# nmap
nmap is a network exploration tool and security / port scanner.

[nmap(1) - Linux man page](https://linux.die.net/man/1/nmap)
## Host Discovery 
### Network Sweeping 
```
nmap -sn 192.168.1.1-254
```
### Network Sweeping to File
* use the `-oG` option to save to greppable format.
```
nmap -sn 10.11.1.1-254 -oG ping-sweep.txt
```
### Filtering Only Live Hosts
```
grep Up ping-sweep.txt | cut -d " " -f 2
```
## Selecting Targets
### Scan a single IP	

```
nmap 192.168.1.1
```
### Scan a host	
```
nmap www.testhostname.com
```
### Scan a range of IPs
```
nmap 192.168.1.1-254
```
### Scan a subnet
```
nmap 192.168.1.0/24
```
### Scan targets from a text file
```
nmap -iL up-hosts.txt
```
## Selecting Ports
### TCP Connect Scan (-sT)
* relies on the completion of TCP 3-Way handshake, `SYN`, `SYN-ACK`, `ACK`.
```
nmap -sT 192.168.1.1
```
### TCP SYN Scan (-sS)
* This is the default scan mode.
* To qualify as an open port a `SYN-ACK` should be sent back, final `ACK` is ignored.
```
nmap -sS 192.168.1.1
```
### Scan UDP ports
* Uses standard `ICMP Port Unreachable` method.
* Scan may be tailored depending on port-protocol, for example a SNMP packet will be sent to a SNMP port.
```
nmap -sU -p 123,161,162 192.168.1.1
```
### Scan Ports - Ignore Host Discovery
```
nmap -Pn -F 192.168.1.1
```
### Combining TCP & UDP Scans
```
nmap -sS -sU 192.168.1.1
```