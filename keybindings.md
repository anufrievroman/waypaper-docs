# Keybindings

### Default keybindings

`h` `j` `k` `l` - Navigation ( `←` `↓` `↑` `→` )

`Enter` - Set the selected wallpaper

`g` - Scroll to the top

`G` - Scroll to the bottom

`f` - Change wallpaper folder

`r` - Re-cache wallpapers

`R` - Set a random wallpaper

`s` - Include/exclude subfolders

`.` - Include/exclude hidden files and folders

`/` - Search

`?` - Help

`q` - Quit (`Esc`)

### Custom keybindings

To remap keybindings, add a line in your config:

```
keybindings = ~/.config/waypaper/keybindings.ini
```

And create a `keybingins.ini` file in your config directory. Here is an example:

```ini
[Keybindings]

navigation_left = h, Left
navigation_down = j, Down
navigation_up = k, Up
navigation_right = l, Right
quit = q, Escape
clear_cache = r
random_wallpaper = R
hidden_files = period
search = slash
include_subfolders = s
choose_folder = f
zen_mode = z
scroll_to_top = g
scroll_to_bottom = G
help_page = question
select_wallpaper = Return, KP_Enter
clear_input_fields = Escape, Return, KP_Enter
```
