# Minecraft: Java Edition (NeoForge)

This template installs a standalone Minecraft Java server using NeoForge.

## Variables

- `version`: Minecraft version to install, for example `1.21.11`.
- `neobuild`: Exact NeoForge version to install, for example `21.11.42`. Leave this empty to let PufferPanel resolve the latest NeoForge build for the selected Minecraft version during installation.
- `javaversion`: Java version to use. Java 21 is the default for Minecraft 1.21.x.
- `memory`: Java heap memory in MB. This is written to `user_jvm_args.txt` as `-Xmx<memory>M`.
- `jvmArgs`: Additional JVM arguments. These are written to `user_jvm_args.txt` before each server start.
- `serverArgs`: Program arguments passed after the NeoForge argument file. The default is `nogui`.
- `ip` and `port`: Server bind address and port.
- `motd`: Message displayed in the Minecraft multiplayer server list.
- `eula`: Must be set to `true` to accept the Minecraft EULA.

## Notes

For production servers, it is recommended to pin `neobuild` to a specific NeoForge version after testing. Leaving `neobuild` empty is useful for quick installs and testing, but future reinstalls may resolve to a newer NeoForge build for the same Minecraft version.

The template downloads the NeoForge installer, runs it with `--installServer`, creates `mods` and `config` directories, writes `server.properties` if missing, writes `eula.txt`, and manages `user_jvm_args.txt` from the template variables.

## Start command

NeoForge does not start like a traditional single `server.jar` Minecraft server. After installation, NeoForge generates platform-specific argument files and launcher scripts.

This template mirrors the generated `run.sh`/`run.bat` behavior:

```sh
java @user_jvm_args.txt @libraries/net/neoforged/neoforge/<resolvedNeoForgeVersion>/unix_args.txt nogui
```

On Linux and Docker the template uses `unix_args.txt`.
On Windows host environments the template uses `win_args.txt`.

Custom JVM arguments belong in the `jvmArgs` template variable. Custom program arguments belong in `serverArgs`.

