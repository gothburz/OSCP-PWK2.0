# nmap
nmap is a network exploration tool and security / port scanner.

[nmap(1) - Linux man page](https://linux.die.net/man/1/nmap)

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
# Selecting Ports
### TCP Connect Scan (-sT)
* relies on the completion of TCP 3-Way handshake.
```
nmap -sT 192.168.1.1
```
### TCP SYN Scan (-sS)
* This is the default scan mode
```
nmap -sS 192.168.1.1
```
### Scan UDP ports
```
nmap -sU -p 123,161,162 192.168.1.1
```
### Scan Ports - Ignore Host Discovery
```
nmap -Pn -F 192.168.1.1
```