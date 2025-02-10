# Usage

`waypaper` command will run GUI application. Make sure to choose the backend that you installed.

To restore your wallpaper at launch, add `waypaper --restore` to your startup config. For example:

**In Hyprland**

`exec-once=waypaper --restore`

**In Sway or I3**

`exec waypaper --restore`

To see the list of hotkeys, press `?`.

#### CLI options

`--restore` - sets the last chosen wallpaper. Useful at launch of the window manager.

`--random` - sets a random wallpaper.

`--folder path/to/folder` - sets folder of wallpaper images.

`--wallpaper path/to/image.jpg` - sets the wallpaper without running the GUI.

`--backend XXX` - specifies which backend to use, which can be either `swaybg`, `swww`, `feh`, `hyprpaper` or `wallutils`. Useful if you use waypaper on both Wayland and Xorg on the same machine. By default, last used backend is used.

`--fill XXX` - specifies filling type, which can be either `fill`, `stretch`, `fit`, `center`, or `tile`.

`--list` - list current wallpapers, monitors and backend in standard output in json format.

`--state-file path/to/file` - sets alternative path to state file.

`--no-post-command` - prevents running the `post_command` set in config.

