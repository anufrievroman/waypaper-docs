# Installation

## Installation

You need to install at least one of the backends and `waypaper` itself, which works as a frontend.

#### 1. Install a backend

Install a preferred backend from your package manager. At least one backend is required.

**Wayland backends:** [swww](https://github.com/Horus645/swww), [awww](https://github.com/heapjumper/awww), [swaybg](https://github.com/swaywm/swaybg), [hyprpaper](https://github.com/hyprwm/hyprpaper), [mpvpaper](https://github.com/GhostNaN/mpvpaper), [gslapper](https://github.com/nickdirienzo/gslapper)

**Xorg backends:** [feh](https://github.com/derf/feh), [xwallpaper](https://github.com/stoeckmann/xwallpaper)

**Cross-platform:** [wallutils](https://github.com/xyproto/wallutils) (Wayland and Xorg)

**Specialized:** [linux-wallpaperengine](https://github.com/Almamu/linux-wallpaperengine) (Steam Wallpaper Engine integration)

#### 2. Install Waypaper

Waypaper is available as a package in different repositories listed below:

**On all distributions**

`pipx install waypaper`

If `pipx` is not found, you first need to install `pipx` from your package manager, it's sometimes called `python-pipx`.

**On Arch-based distributions**

`yay -S waypaper` or `yay -S waypaper-git`

The [waypaper](https://aur.archlinux.org/packages/waypaper) and [waypaper-git](https://aur.archlinux.org/packages/waypaper-git) package is available in AUR, thanks to _metak_. Please upvote them to support the project. Please understand that the `waypaper-git` package is not always stable.

**On NixOS**

The `waypaper` package is available thanks to Basil Keeler. Install with:

`nix-env -iA nixpkgs.waypaper`

#### On OpenSUSE

Users of OpenSUSE [reported problems with installation](https://github.com/anufrievroman/waypaper/issues/30) via `pipx install waypaper`. This problem might be resolved by installing the `python311-pycairo-devel` package.

#### On Fedora

Users reported [issues with installation](https://github.com/anufrievroman/waypaper/issues/53), which might be resolved by installing `cairo-gobject-devel package`. Then install with `pipx` as described above.&#x20;

If it doesn't work, Waypaper is available in an [external repository owned by Solopasha](https://copr.fedorainfracloud.org/coprs/solopasha/hyprland/). So, you can add this repository as `sudo dnf copr enable solopasha/hyprland` and install as `sudo dnf install waypaper`.

## Dependencies

* At least one backend (see above)
* `python-gobject` (GTK3 bindings, may also be called `python3-gi` or `python3-gobject`)
* `python-platformdirs`
* `python-pillow` (image processing)
* `python-imageio` and `python-imageio-ffmpeg` (video thumbnail generation, required for `mpvpaper` and `gslapper`)
* `python-screeninfo` (monitor detection)
