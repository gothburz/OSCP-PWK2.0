# practical-tools
[socat-shell-cheatsheet](https://github.com/gothburz/PWK-OSCP-Prep/blob/master/practical-tools/socat-shell-cheatsheet.md)

# Working with Python Scripts
Due to version and dependency issues that may arise when working with existing scripts its advisable to setup Python virtual environments.

If you need to work with earlier versions of python install `virtualenv` package.
## Installing virtualenv with Python2
```angular2
gothburz@kali:~$ sudo virtualenv --python=/usr/bin/python .venv
```

## Installing venv
```
gothburz@kali:~$  sudo apt-get install python3-venv
```
Create the virtual environment.
```angular2
gothburz@kali:~$ python3 -m venv .venv
```
Activate the virtual environment.
```
gothburz@kali:~$ source .venv/bin/activate
```
Verify
```angular2
(.venv) gothburz@kali:~$ which python
/home/gothburz/.venv/bin/python
```
Deactivate
```angular2
(.venv) gothburz@kali:~$ deactivate .venv/bin/activate
```
