# Troubleshooting

* If wallpaper does not change, first, try to launch waypaper in the terminal and see the output. Also, try to change it via command line using chosen backend to make sure that backend by itself works correctly.
* If application does not run, make sure to install `gobject` library (it might be called `python-gobject` or `python3-gi` in your package manager). Although it is supposed to be installed automatically with the package.
* Please understand that not all backends work on all systems. `feh` is only for Xorg, while `swww` and `swaybg` are only for Wayland.
* If you use different WMs on the same system, specify the backend when you restore the wallpaper at launch. For example: `waypaper --restore --backend feh` or use `wallutils` which works on both Wayland and Xorg.
