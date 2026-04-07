# Hytale Server Template for PufferPanel

Unofficial template for running Hytale Server (Early Access) on PufferPanel.

## Features
- Automatic official server download
- Docker and Host support
- Panel-based configuration
- Optional backup system
- Configurable UDP port
- Auth mode support (authenticated / offline)

## Requirements
- PufferPanel >= 2.x
- Linux amd64
- Docker (optional)

## Notes
- This template does not include proprietary files
- Server downloads directly from official Hypixel source
- Template is experimental (Early Access)

## Legal Notice
Hytale is a registered trademark of Hypixel Studios.
This template is not officially affiliated with Hypixel Studios.

## Configurable Settings

### Server Configuration
- **Max Players**: Set the maximum number of concurrent players
- **Game Mode**: Choose your game mode
- **Memory**: Allocate RAM for the server (in MB)
- **MOTD**: Set your server's Message of the Day
- **Extra Arguments**: Add additional startup arguments

### Security & Access
- **Authentication Mode**: Choose between authenticated or offline mode
- **Allow OP**: Enable/disable operator permissions
- **Password**: Server password (if required)

### Backup
- **Enable Backups**: Automatic world backups
- **Backup Directory**: Custom backup location
- **Backup Frequency**: Interval in minutes

---
#### ⚠️ PufferPanel v2 notice
```
This template is compatible with both v2 and v3.
However, PufferPanel v2 has known Docker execution issues.

If server creation fails but the template imports correctly, please upgrade to PufferPanel v3.
```