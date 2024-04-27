# Minetest

> These PufferPanel templates install the Minetest game engine. 

As there are no precompiled binaries, the installer compiles Minetest from source, resulting in long installation times. The number of available CPU cores can be obtained using `nproc`

Please make sure the following dependencies are installed (for Debian/Ubuntu users):
```sh
sudo apt install g++ make libc6-dev cmake libpng-dev libjpeg-dev libxi-dev libgl1-mesa-dev libsqlite3-dev libogg-dev libvorbis-dev libopenal-dev libcurl4-gnutls-dev libfreetype6-dev zlib1g-dev libgmp-dev libjsoncpp-dev libzstd-dev libluajit-5.1-dev gettext
```
*If you are using another distribution, a depency list can be found in the official Minetest documentation.*

Due to some versions requiring an additional dependency, there are two different template files:

- For Minetest versions between and including 5.5.0 and 5.8.0, please use the `minetest-irrlichtmt.json` template file.
    - Please specify the required IrrlichtMT version:
        - Minetest `5.5.0` requires IrrlichtMT `1.9.0mt4`
        - Minetest `5.5.1` requires IrrlichtMT `1.9.0mt4` or `1.9.0mt5`
        - Minetest `5.6.0` requires IrrlichtMT `1.9.0mt7`
        - Minetest `5.6.1` requires IrrlichtMT `1.9.0mt8`
        - Minetest `5.7.0` requires IrrlichtMT `1.9.0mt10`
        - Minetest `5.8.0` requires IrrlichtMT `1.9.0mt13`
- For Minetest versions below 5.5.0 and above 5.8.0, please use the `minetest.json` template file.

Minetest is only a game engine, games have to be downloaded from https://content.minetest.net/packages/?type=game and installed in the `minetest/games` directory.
