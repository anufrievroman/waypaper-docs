# Usage

`waypaper` command will run GUI application. Make sure to choose the backend that you installed.

To restore your wallpaper at launch, add `waypaper --restore` to your startup config. For example:

**In Hyprland**

`exec-once=waypaper --restore`

**In Sway or I3**

`exec waypaper --restore`

To see the list of hotkeys, press `?`.

### CLI options

`--restore` - sets the last chosen wallpaper. Useful at launch of the window manager.

`--random` - sets a random wallpaper.

`--folder path/to/folder` - sets folder of wallpaper images.

`--wallpaper path/to/image.jpg` - sets the wallpaper without running the GUI.

`--backend XXX` - specifies which backend to use, which can be either `swaybg`, `swww`, `feh`, `hyprpaper` or `wallutils`. Useful if you use waypaper on both Wayland and Xorg on the same machine. By default, last used backend is used.

`--fill XXX` - specifies filling type, which can be either `fill`, `stretch`, `fit`, `center`, or `tile`.

`--list` - list current wallpapers, monitors and backend in standard output in json format.

`--state-file path/to/file` - sets alternative path to state file.

`--no-post-command` - prevents running the `post_command` set in config.

### Automatically changing wallpaper

#### Simple bash script

The most basic way to automatically change wallpaper at set intervals is to run a simple script:

```
while true; do sleep 600; waypaper --random; done
```

You can start it with the start of your system, for example.

#### Cron job

For a more sophisticated solution, create these two files:

`~/.config/systemd/user/waypaper.timer`

```
[Unit]
Description=Set a random wallpaper every minute

[Timer]
Persistent=true
OnCalendar=*:0/1

[Install]
WantedBy=timers.target
```

`~/.config/systemd/user/waypaper.service`

```
[Unit]
Description=Set a random wallpaper with waypaper

[Service]
Type=oneshot
ExecStart=waypaper --random
```

Note, depending on how waypaper is installed, you may need to provide a full path to the executable in `ExecStart`.

To test, run `$ systemctl --user start waypaper.timer`\
To make persistent, run `$ systemctl --user enable waypaper.timer`
