# Installation

## Installation

You need to install at least one of the backends and `waypaper` itself, which works as a frontend.

#### 1. Install a backend

Install a preferred backend from your package manager: [swww](https://github.com/Horus645/swww) or [swaybg](https://github.com/swaywm/swaybg) on Wayland or [feh](https://github.com/derf/feh) on Xorg or [wallutils](https://github.com/xyproto/wallutils) on both.

#### 2. Install Waypaper

Waypaper is available as a package in different repositories listed below:

**On all distributions**

`pipx install waypaper`

If `pipx` is not found, you first need to install `pipx` from your package manager, it's sometimes called `python-pipx`.

**On Arch-based distributions**

`yay -S waypaper-git`

The [waypaper-git](https://aur.archlinux.org/packages/waypaper-git) package is available in AUR, thanks to _metak_. Please upvote to support the project.

**On NixOS**

The `waypaper` package is available thanks to Basil Keeler.

#### On OpenSUSE

Users of OpenSUSE [reported problems with installation](https://github.com/anufrievroman/waypaper/issues/30) via `pipx install waypaper`. This problem might be resolved by installing the `python311-pycairo-devel` package.

## Dependencies

* `swww` or `swaybg` or `feh` or `wallutils`
* gobject python library (it might be called `python-gobject` or `python3-gi` or `python3-gobject` in your package manager.)
* `python-importlib_metadata`
* `python-platformdirs`
