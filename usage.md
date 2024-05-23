# Usage

`waypaper` command will run GUI application. Make sure to choose the backend that you installed.

To restore your wallpaper at launch, add `waypaper --restore` to your startup config. For example:

**In Hyprland**

`exec-once=waypaper --restore`

**In Sway or I3**

`exec waypaper --restore`

To see the list of hotkeys, press `?`.

#### Options

`--restore` - sets the last chosen wallpaper. Useful at launch of the window manager.

`--random` - sets a random wallpaper. Makes sense only together with `--restore` key.

`--backend XXX` - specifies which backend to use, which can be either `swaybg`, `swww`, `feh`, or `wallutils`. Useful if you use waypaper on both Wayland and Xorg on the same machine. By default, last used backend is used.

`--fill XXX` - specifies filling type, which can be either `fill`, `stretch`, `fit`, `center`, or `tile`.
