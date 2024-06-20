# Necesse Server Template

This template is for [Necesse](https://necessegame.com/) server creation for PufferPanel.

## Requirements

- PufferPanel version steamdl support.
- Necesse comes pre-bundled with Java.
  - Installing a different Java version instead of pre-bundled may break future builds.

## Additional Information

1. We are removing the `server.cfg` file on every run in order to force the server to use the variables we configured. Otherwise we will need to manually delete the file every time we change the configurations.
2. I am using `Xms512m` for JVM args in order to fix startup error when JVM args is empty.
   1. Based on my experience running the server so far, `Xms512m` should be the bare minimum.
