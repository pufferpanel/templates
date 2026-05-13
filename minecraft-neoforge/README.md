# Minecraft: Java Edition (NeoForge)

This template installs a standalone Minecraft Java server using NeoForge.

## Variables

- `version`: Minecraft version to install, for example `1.21.11`.
- `neobuild`: Exact NeoForge version to install. Leave this empty to let PufferPanel resolve the latest NeoForge build for the selected Minecraft version.
- `javaversion`: Java version to use. Java 21 is the default for Minecraft 1.21.x.
- `memory`: Java heap memory in MB.
- `ip` and `port`: Server bind address and port.
- `motd`: Message displayed in the Minecraft multiplayer server list.
- `jvmArgs`: Additional JVM arguments.
- `eula`: Must be set to `true` to accept the Minecraft EULA.

## Notes

For production servers, it is recommended to pin `neobuild` to a specific NeoForge version after testing. Leaving `neobuild` empty is useful for quick installs and testing, but future reinstalls may resolve to a newer NeoForge build for the same Minecraft version.

The template downloads the NeoForge installer, runs it with `--installServer`, creates `mods` and `config` directories, writes `server.properties` if missing, and writes `eula.txt`.

## Start command

NeoForge is started through the generated argument files below `libraries/net/neoforged/neoforge/<resolvedNeoForgeVersion>/`.

On Linux and Docker the template uses `unix_args.txt`.
On Windows host environments the template uses `win_args.txt`.

