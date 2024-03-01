
## ASTRONEER

This was tested on debian, but should also work on ubuntu

Add Wine apt repository (recomended, else use `wine` instead of `winehq-stable`):
- Debian: https://wiki.winehq.org/Debian
- Ubuntu: https://wiki.winehq.org/Ubuntu

Install this for Astroneer:

```

sudo apt install winehq-stable lib32gcc-s1

```

- On older ubuntu versions, package `lib32gcc-s1` might not be available. In that case, install this:

   ```sudo apt install winehq-stable lib32gcc1```

Allow client side to join:

Add following in file `%LOCALAPPDATA%\Astro\Saved\Config\WindowsNoEditor\Engine.ini`:
```
[SystemSettings]
net.AllowEncryption=False
```

## This only supports Linux.

## Note

This should mostly work but i had sometimes false positives on stoping (to short after start) and the server continued running in the background.

This has mostly to do with the fact that the astroneer server is running through wine and my hacky way of getting the half broken RCON to connect to the console window.

I recomend blocking the RCON Port through a firewall or no port forward if behind NAT.

CommandList: https://github.com/Esinko/AstroneerRconClient/blob/master/README.md#command-reference (some are crashing on wine)
