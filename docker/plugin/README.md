# Monstache plugin builder

You can use the `build.sh` script in this folder to build a golang plugin for monstache using docker.

Copy your plugin source code to the `plugin` folder.  This build assumes the name of the main entry
point for the plugin is `plugin.go`.  If you want to change that edit the `.plugin` file and enter the name of
your plugin .go file without the .go extension.

Run `build.sh` from this directory and the plugin .so file will be built to a `docker-build` folder.  The path 
to the resulting .so file can be used in the monstache argument `mapper-plugin-path` to activate the plugin.

If your host is linux you may need to install `musl` to run the resulting binary. For example, on a debian system

```
sudo apt install musl
```
