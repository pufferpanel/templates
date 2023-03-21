# Python3 pufferpanel template
### Allows you to easly host your python projects
 - Made by @CristianEduardMihai

# Troubleshooting

```
No module named pip
```
- That's an easy fix, install pip

   Ubuntu/Debian/Raspbian
   ```
   sudo apt update
   sudo apt -y install python3-pip
   ```
   Fedora
   ```
   sudo dnf install python3-pip
   ```
   [Centos](https://linuxize.com/post/how-to-install-pip-on-centos-7/)

---
```
Could not open requirements file
```
- Read [this](https://learnpython.com/blog/python-requirements-file/) and create a requirements.txt file
---
```
can't open file '/var/lib/pufferpanel/servers/xxxxxxxx/main.py'
```
- Is your file named `main.py` ? If not, edit the server settings

![image](https://i.imgur.com/vbaWQuy.png)

### If you did everything above(and only then), and it's still not working, ask for support on discord