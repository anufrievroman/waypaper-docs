---
description: Fixing common issues with Waypaper
---

# Troubleshooting

#### General issues

* If wallpaper does not change, first, try to launch waypaper in the terminal and see the output when you are trying to change the wallpaper. Also, try to change it via command line using chosen backend to make sure that backend by itself works correctly.
* Please understand that not all backends work on all systems. `feh` is only for Xorg, while `swww` , `swaybg` and `hyprpaper` are only for Wayland.
* If you use different WMs on the same system, specify the backend when you restore the wallpaper at launch. For example: `waypaper --restore --backend feh` or use `wallutils` which works on both Wayland and Xorg.

#### Installation

* If application does not run or shows errors about GTK, make sure to install `gobject` library (it might be called `python-gobject` or `python3-gi` in your package manager). Although it is supposed to be installed automatically with the package.
* If you see errors related to `cairo` you may need to install `pycairo-devel` package. It might be called a bit different on different distributions.

#### Hyprpaper backend

* To use `hyprpaper` backend you need to be on `Hyprland` and have `hyprctl`.
* Make sure you have inter process communication (IPC) enabled, i.e. `icp = on` in `hyprpaper.conf` and there are no warnings about it when you simply start `hyprpaper`.
