---
description: Fixing common issues with Waypaper
---

# Troubleshooting

#### Installation

* If the application does not run or shows errors about GTK, make sure to install `gobject` library, which might also be called `python-gobject` or `python3-gi` in your package manager. Although it is supposed to be installed automatically with the package.
* If you see errors related to `cairo` you may need to install `pycairo-devel` or [`cairo-gobject-devel`](https://packages.fedoraproject.org/pkgs/cairo/cairo-gobject-devel/)package. It might be called a bit different on different distributions.
* On Fedora, you might need to install `cairo-gobject-devel` package, then install `waypaper` with `pipx`.
* If installation doesn't work via your distribution repository, try to install with `pipx`as: `pipx install waypaper` as this is the only officially maintained repository of Waypaper.
* On MacOS, if you see an error about cairo 1.0, you need to: `brew install pygobject3 gtk+3 cairo gobject-introspection`

#### General issues

* If too much RAM or CPU is used after changing wallpaper, make sure your `post_script` is not trying to do some heavy processing. By itself, Waypaper is not doing anything resource heavy.
* To restore the wallpaper after a reboot, you need to launch `waypaper --restore` at the start of your system. Usually, it means that you need to add it to the config of your WM.
* If the wallpaper does not change, first, try to launch Waypaper in the terminal and see the output when you are trying to change the wallpaper. Also, try to change it via command line using chosen backend to make sure that backend by itself works correctly.
* Please understand that not all backends work on all systems. `feh` is only for Xorg, while `swww` , `swaybg` and `hyprpaper` are only for Wayland.
* If you use different WMs on the same system, specify the backend when you restore the wallpaper at launch. For example: `waypaper --restore --backend feh` or use `wallutils` which works on both Wayland and Xorg.

#### Hyprpaper backend

* To use `hyprpaper` backend you have to be on `Hyprland` and have `hyprctl`.
* Make sure you have inter process communication (IPC) enabled, i.e. `icp = on` in `hyprpaper.conf` and there are no warnings about it when you simply start `hyprpaper`.

Mpvpaper backend

* If something is not working, try to click `Stop`button, it will kill all running mpvpaper processes.
* Mpvpaper often conflicts with other backends, try to stop them is something is wrong.
* If you can't set an image as wallpaper, only a video, try removing your`mpvpaper_options`
