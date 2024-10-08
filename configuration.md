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
number_of_columns = 3
post_command = 
show_hidden = False
show_gifs_only = False
swww_transition_type = any
swww_transition_step = 90
swww_transition_angle = 0
swww_transition_duration = 2
swww_transition_fps = 60
use_xdg_state = False
```

Most of the options in the config are controlled by the GUI application and user is not expected to change them manually. However, the following options can be set by the user and are not changed by GUI application:

`number_of_columns` controls the columns in GUI.&#x20;

`post_command` option can be used to automatically run a command after selecting a wallpaper. This option supports `$wallpaper` parameter, so one could write something like:

`post_command = echo "My new wallpaper: $wallpaper "`

All the `swww` related options control wallpaper change animation with `swww` backend. More details can be found by running `man swww-img`

`language` can be set to one of the following: `en`, `de`, `fr`, `ru`, `pl`, `zh`.

