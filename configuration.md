# Configuration

On the first run, a config file will be created in your config directory, typically it is at`~/.config/waypaper/config.ini` Here is a typical config:

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
swww_transition_type = any
swww_transition_step = 90
swww_transition_angle = 0
swww_transition_duration = 2
swww_transition_fps = 60
mpvpaper_sound = False
mpvpaper_options = 
use_xdg_state = False
post_command = 
```

Most of the options in the config are controlled by the GUI application and user is not expected to change them manually.

However, to use wallpaper from multiple folders, the folder paths will need to be placed in the config explicitly and will be overwritten if changed in the GUI.

To use wallpaper from multiple folders, put folders separated line by line.

```
folder = /path/folder_1
         /path/folder_2
         /path/folder_3
```

The following options can be set by the user and are not changed by GUI application:

`post_command` option can be used to automatically run a command after selecting a wallpaper. This option supports `$wallpaper` parameter, so one could write something like:

`post_command = echo "My new wallpaper: $wallpaper "`

or you can run your own script there as:

`post_command = my_wallpaper_script.sh $wallpaper`&#x20;

The `language` parameter can be set to one of the following: `en`, `de`, `fr`, `ru`, `pl`, `zh`, `zh_HK`.
