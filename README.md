# Overview of my dwm build
___
lorem
## Screenshot
___
lorem

# Requirements
___
In order to build dwm you should install packages: git, xorg-server, xorg-xinit, xorg-xrandr, xorg-xsetroot.
```
$ sudo pacman -S git xorg-server xorg-xinit xorg-randr xorg-xsetroot
```

# Installation
___
## Preparation
___
First create .xinitrc in the path /etc/X11/xinit/xinitrc (remember that linux is case sensitive for X11)
```
$ cp /etc/X11/xinit/xinitrc .xinitrc
```
Then replace the last 5 lines of .xinitrc with:
```
exec dwm
```
using your text editor (nano is default on Arch).

## Git clone
___
Git clone dwm into your user's default path (~).
```
$ git clone https://github.com/jeffock/dwm
```
You may return an SSL error: if you do, run the following instead
```
$ git -c http.sslVerify=false clone https://github.com/jeffock/dwm
```

## Compile dwm
___
Enter the following command to build and install dwm (if
necessary as root):
```
    make clean install
```

# Run dwm
___
Because we added `exec dwm` to .xinitrc we can run dwm with:
```
$ startx
```

# Configuring and Building dwm to your liking
___
This fork of dwm is a basic build/rice of dwm. However, if you would like to make your own changes most settings will be found in config.h.

If you want to patch (build) to your liking follow [suckless's guide](https://suckless.org/hacking/)

If you plan on making your own build of dwm it is recommended that you use a main branch or trunk to do so, for more information follow [suckless's guide to patching in git](dwm.suckless.org/customisation/patches_in_git/)



