# Template for [ARK: Survival Evolved](http://playark.com/)
This template makes it possible to run [ARK: Survival Evolved](http://playark.com/) with [PufferPanel](https://www.pufferpanel.com/) on Linux.

This will not be part of the default templates because it requires a lot of RAM (4GB at least) and requires that you run the following commands to increase the open files limit.

## Prerequisites
* Server requires a lot of RAM, you should have at least 4 GB free
* Maybe you have to increase the open files limit on your linux system. As far as known, this is not necessary with Debian 9 (Stretch). You can increase the limits with these commands:
  
  (as root)
  ```
  echo "fs.file-max=100000" >> /etc/sysctl.conf && sysctl -p
  echo "* soft nofile 1000000" >> /etc/security/limits.conf
  echo "* hard nofile 1000000" >> /etc/security/limits.conf
  echo "session required pam_limits.so" >> /etc/pam.d/common-session
  ```
* For more information about prerequisites for ARK server follow this link. https://ark.gamepedia.com/Dedicated_Server_Setup#Prerequisites_2


Current map values available are:
* TheIsland
* TheCenter
* ScorchedEarth_P
* Ragnarok
* Aberration_P
* Extinction

## Notes
* If you want to use a whitelist you have to use the `-exclusivejoin` argument, you can set it on server creation or editing. After that you must set up a whitelist file in the file system manually. You can do this using SFTP. 
  * Create the file in the directory `ShooterGame/Binaries/Linux_OR_Win64/PlayersExclusiveJoinList.txt`
  * Find the Steam64 ID of your friends and paste them, one per line.

This only supports Linux.