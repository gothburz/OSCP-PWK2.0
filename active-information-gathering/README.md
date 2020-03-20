# Tools
Download [AutoRecon](https://github.com/Tib3rius/AutoRecon) this will save you a lot of time. 
Be sure to have python3 installed, you may need to install pip as well, I had issues on Kali2020. To install pip for python3:
```
wget https://bootstrap.pypa.io/get-pip.py
sudo python3 get-pip.py
```

# Process
It's important to develop an process on how you approach a pentest. This should include detailed note and screenshots in order to develop an organized report.
## Finding Hosts (L3 Enumeration)
Find out which hosts respond to pings in the network.
```
nmap -sn 10.11.1.1-254 -oG ping-sweep.txt
```
Filter out IP Addresses
```
cat ping-sweep.txt | grep "Up" | awk -F " " '{print $2}' > up-hosts.txt
```
## Port Enumeration (L4 Enumertion)
Be sure to have [AutoRecon](https://github.com/Tib3rius/AutoRecon) installed.
```angular2
./autorecon.py -t up-hosts.txt -o autorecon_scan
```