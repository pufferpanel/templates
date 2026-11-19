
# Conan Exiles Enhanced
 
PufferPanel template for a Conan Exiles dedicated server (Steam App ID `443030`), running in Docker with `steamcmd/steamcmd`.
 
## Ports
 
| Port  | Protocol | Purpose                                                  |
|-------|----------|----------------------------------------------------------|
| 7777  | UDP      | Game port                                                |
| 7778  | UDP      | Pinger, used by the server browser (always game port + 1) |
| 27015 | UDP      | Server query, used by the server list                    |
 
The container uses host networking, so open these ports in your firewall.
 
## Settings
 
Server name, passwords, MOTD, max players, max nudity and PVP can be changed in the panel. They are written to `ServerSettings.ini` and `Engine.ini` on every start, so manual edits to these values are overwritten.
 
Do not use double quotes (`"`) in the server name.
 
## Mods
 
With **Manage Mods with Pufferpanel** enabled, list Steam Workshop mod IDs in `mods.txt`, one per line:
 
```
3811568075 # Mod name (optional comment)
# 3720904511  <- disabled
```
 
- Mods load in the order listed.
- On every start, all mods listed in `mods.txt` are installed or updated via SteamCMD, and `modlist.txt` is regenerated from them.
- This adds to the start time with many mods enabled. For a faster start, disable **Manage Mods with Pufferpanel** and the installed mods remain untouched.
## Notes
 
- The server is updated via SteamCMD on every start.
- The first install can take a while, as the server files are large.
- Supports only Linux and Docker