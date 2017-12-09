ARK: Survival Evolved Template

This will not be part of the default templates because it requires a lot of RAM (4GB at least) and requires that you run the following commands to increase the open files limit.

(as root)
```
echo "fs.file-max=100000" >> /etc/sysctl.conf && sysctl -p
echo "* soft nofile 1000000" >> /etc/security/limits.conf
echo "* hard nofile 1000000" >> /etc/security/limits.conf
echo "session required pam_limits.so" >> /etc/pam.d/common-session
```
There is a known issue with being able to stop it as well. Using the "kill" button should work.
