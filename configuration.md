# Configuration

On the first run, a config file will be created in your config directory, typically at `~/.config/waypaper/config.ini`. Here is a typical config:

```
[Settings]
language = en
folder = ~/Pictures
wallpaper = ~/Pictures/wallpaper.jpg
backend = swaybg
monitors = All
fill = Fill
sort = name
color = #ffffff
subfolders = False
all_subfolders = False
show_hidden = False
show_gifs_only = False
show_path_in_tooltip = True
number_of_columns = 3
use_xdg_state = False
zen_mode = False
swww_transition_type = any
swww_transition_step = 63
swww_transition_angle = 0
swww_transition_duration = 2
swww_transition_fps = 60
mpvpaper_sound = False
mpvpaper_options = 
post_command = 
keybindings = ~/.config/waypaper/keybindings.ini
```

Most of the options in the config are controlled by the GUI application, and the user is not expected to change them manually. However, some advanced parameter can be set only in config:

### Folders

To use wallpapers from multiple folders, the folder paths will need to be placed in the config explicitly and will be overwritten if changed in the GUI. To use wallpaper from multiple folders, put folders separated line by line.

```
folder = /path/folder_1
         /path/folder_2
         /path/folder_3
```

### Running scripts after setting wallpaper

`post_command` option can be used to automatically run a command after selecting a wallpaper. This option supports the `$wallpaper` and `$monitor` variables. For example:

```
post_command = echo "New wallpaper on $monitor: $wallpaper"
```

or you can run your own script:

```
post_command = my_wallpaper_script.sh $wallpaper $monitor
```

Note that the `$wallpaper` variable provides an escaped representation of the path. If your script expects an unescaped representation, you can try:

```
read -d '' fixed <<< "$wallpaper"; my_command "$fixed"
```

### Language

The `language` parameter can be set to one of the following: `en` (English), `de` (German), `fr` (French), `pl` (Polish), `ru` (Russian), `be` (Belarusian), `es` (Spanish), `zh` (Chinese).

### State file

`use_xdg_state` parameter is useful when you want to use a state file instead of a traditional config file. The state file will be then saved separately in a state directory and contain state parameters like wallpapers and monitors. Useful for systems with immutable configs.

### Video options

`mpvpaper_options` can contain some setting for the video wallpaper is you uses _mpvpaper_ backend. For example, you can specify something like:

```
mpvpaper_options = profile=fast --vf-add=fps=3:round=near
```

### Linux Wallpaper Engine

When using the `linux-wallpaperengine` backend, Waypaper reads wallpapers from your Steam Workshop folder. By default it looks at `~/.steam/root/steamapps/workshop/content/431960`. You can override this with:

```
wallpaperengine_folder = /path/to/steamapps/workshop/content/431960
```

The following options control the linux-wallpaperengine behavior and are set via the GUI, but can also be edited manually:

```
linux_wallpaperengine_fps = 30
linux_wallpaperengine_volume = 15
linux_wallpaperengine_silent = False
linux_wallpaperengine_noautomute = False
linux_wallpaperengine_no_audio_processing = False
linux_wallpaperengine_disable_particles = True
linux_wallpaperengine_disable_mouse = False
linux_wallpaperengine_disable_parallax = False
linux_wallpaperengine_no_fullscreen_pause = False
linux_wallpaperengine_fullscreen_pause_only_active = False
linux_wallpaperengine_clamp = none
```

The `linux_wallpaperengine_clamp` option controls texture clamping and accepts: `none`, `clamp`, `border`, or `repeat`.

### Custom styles and colors

You can use a custom CSS file to alter the standard GTK theme by setting

```
stylesheet = ~/.config/waypaper/style.css
```

and creating a **style.css** file that might look something like that:

```
window {
    background-color: rgba(255, 255, 255, 0.3);
}

button:hover {
    background-image: none;
    box-shadow: none;
    border-color: transparent;
}

button:hover>image {
    -gtk-icon-shadow: none;
    -gtk-icon-effect: none;
}

.highlighted-button {
    background-image: none;
    box-shadow: none;
    background-color: rgba(255,255,255,0.5);
}

.highlighted-button>image, .highlighted-button:hover>image {
    -gtk-icon-effect: highlight;
}
```
