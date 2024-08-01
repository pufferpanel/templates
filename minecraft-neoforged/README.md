# Template for a Minecraft Server with [NeoForged](https://neoforged.net/) installed
Template written by [Spusuf](https://github.com/spusuf
Compatible with 1.20.2 to latest (1.21.0)
Tested on Linux baremetal and using pufferpanel installed in docker, but nothing should prevent running on other platforms.
Versions older than are available on the current archive (older than 1.20.2) are hosted in a seperate location and are not compatible unless you manually download and run the installer (not recommended), anything from 1.20.2 onwards works flawlessly with no inverention needed.

# Steps
1. Download and create server using the template, give the server a name.
2. In the options tab of the server creation read and check the EULA agreement (or in the settings tab if you ignored and already created the server). No I cannot do that for you.
3. Set java version based on what is on your server (or use the default 17 to use pufferpanel's default)
4. Set Dedicated RAM amount (Default 1024 is 1 GB, 4096 (4 GB) should be fine for 4 simulatenous players and reasonable view distance (< 16), otherwise 8192 (8 GB) for higher view distance or heavier mods. Minecraft does not effectively utilise more than this, but SPECIFIC mods might)
5. Set a port. Match this to your port forward for domestic servers, or SRV record for a server behind a DNS.
6. Set neo(forged) version. This will also dictate your minecraft server's version, so choose correctly.
7. Click crete, then when the server is created click install. A wall of text should indicate downloading, if there is only a few lines you've done something wrong (probably neo version). The server will start automatically.
8. Connect and have fun. Raise an issue on github if the script stops working.
