# Install Empire
```aidl
gothburz@kali:~$ cd /opt
gothburz@kali:/opt$ sudo git clone https://github.com/PowerShellEmpire/Empire.git
Cloning into 'Empire'...
remote: Enumerating objects: 12216, done.
remote: Total 12216 (delta 0), reused 0 (delta 0), pack-reused 12216
Receiving objects: 100% (12216/12216), 21.96 MiB | 3.22 MiB/s, done.
Resolving deltas: 100% (8312/8312), done.

gothburz@kali:/opt$ cd Empire/
gothburz@kali:/optEmpire$ sudo ./setup/install.sh
```
# Run
```aidl
gothburz@kali:/optEmpire$ sudo ./empire
```
If you receive an error `ImportError: No module named pefile` then `sudo pip install pefile`.