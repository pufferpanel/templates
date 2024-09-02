## ASTRONEER (AstroTuxLauncher)

Runs an Astroneer Server using [AstroTuxLauncher](https://github.com/JoeJoeTV/AstroTuxLauncher/) and WINE

### Prerequisites

- Currently only Linux
- **Python 3.9+** (Tested with 3.9.5, 3.10.12, 3.11.0rc1)
- Python PIP
- WINE

### Note

Running an Astroneer Server on Linux via WINE currently **requires disabling encryption** for the connection to the server, as there is a bug preventing the server from starting with it enabled. This is also the case for _game clients_ running Astroneer via Wine/Proton on Linux.
**This means, all game clients that want to connect to a server hosted on Linux via WINE have to disable encryption locally as well, regardless of platform**

#### Disabling encryption

Encryption on the Server is handled by AstroTuxLauncher automatically.
For the clients, one must add the following lines to the end of the `Engine.ini` file:

```ini
[SystemSettings]
net.AllowEncryption=False
```

The `Engine.ini` file can be found at the following locations:

- **Windows:** `%LOCALAPPDATA%\Astro\Saved\Config\WindowsNoEditor\Engine.ini`
- **Linux (Steam)** `<Steam Library Path>/steamapps/compatdata/361420/pfx/drive_c/users/steamuser/AppData/Local/Astro/Saved/Config/WindowsNoEditor/Engine.ini`
