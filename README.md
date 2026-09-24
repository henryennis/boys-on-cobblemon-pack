# Boys on Cobblemon: client pack

The mod list for the Boys on Cobblemon server, in packwiz format. Your launcher
reads it before every launch and downloads only what changed, so you never
re-import the pack by hand.

## One-time setup in Prism Launcher

1. Import the `.mrpack` you were sent, or use your existing instance.
2. Download `packwiz-installer-bootstrap.jar` from
   <https://github.com/packwiz/packwiz-installer-bootstrap/releases/latest>
   and put it in the instance's `minecraft` folder (right-click the instance,
   Folder, then open `minecraft`).
3. Right-click the instance, Edit, Settings, Custom commands. Tick the box and
   set the pre-launch command to:

   ```
   "$INST_JAVA" -jar "$INST_MC_DIR/packwiz-installer-bootstrap.jar" https://raw.githubusercontent.com/henryennis/boys-on-cobblemon-pack/main/pack.toml
   ```

4. Launch. A small window shows the sync, then the game starts.

Your own settings are safe: config files are only written when you do not have
them yet.

This repository is generated. Edit the pack in the server's infrastructure
repo and run `make publish-pack` there.
