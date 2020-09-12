# Template for [ECO – Global Survival](https://play.eco/)
This templates makes it possible to run [ECO – Global Survival](https://play.eco/) with [PufferPanel](https://www.pufferpanel.com/).

You can find two templates in this directory:
* `eco.json` to run ECO versions from 0.9.0.0-beta natively on unix systems.
* `eco-mono.json` to run ECO with [mono](https://www.mono-project.com/), supports only versions up to 0.8.3.3-beta.

## Prerequisites
### General requisites
* For both templates you need the `unzip` command on your server. You can install `unzip` on Debian and Ubuntu with the following commands as root:
  ```bash
  apt-get update
  apt-get install unzip
  ```
  
### Prerequisites for the default template
* You need to install the .NET Core Runtime on your system. For Debian you can find the instructions [on the official microsoft website](https://docs.microsoft.com/de-de/dotnet/core/install/linux-debian).

### Prerequisites for the `mono` template
* To use this template, you need to install `mono` on your server.
To install `mono`, follow the instructions on [mono-project.com](https://www.mono-project.com/download/stable/) for your distribution.

## Known issues
* The ECO server will not start when used with `mono` version 5.16: https://github.com/StrangeLoopGames/EcoIssues/issues/9676

  You can use version 5.14 instead.
