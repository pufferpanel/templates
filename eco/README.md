# Template for [ECO – Global Survival](http://www.strangeloopgames.com/eco/)
This template makes it possible to run [ECO – Global Survival](http://www.strangeloopgames.com/eco/) with [PufferPanel](https://www.pufferpanel.com/) on Linux.

## Prerequisites
* To use this template, you need to install `mono` on your server.
To install `mono`, follow the instructions on [mono-project.com](https://www.mono-project.com/download/stable/) for your distribution.
* You need the `unzip` command on your server. You can install `unzip` on Debian and Ubuntu with the following commands as root:
  ```bash
  apt-get update
  apt-get install unzip
  ```

## Known issues
* The ECO server will not start when used with mono version 5.16: https://github.com/StrangeLoopGames/EcoIssues/issues/9676

  You can use version 5.14 instead.
