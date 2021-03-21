<h1 align="center">
  dynamd
</h1>
<h4 align="center">dynamd is an extremely fast, light-weight, efficient, highly-customizable and dynamic window manager based on <a href=https://dwm.suckless.org>DWM</a> for X</h4>


## Build Requirements
* Xlib header files
* libxft
* libxcb
* libX11
* xcb

## NOTE
The source code contains my personal configuration. If you want to use it make sure to look carefully 
in **`src/Makefile`** (specially *`CFLAGS`* & *`LDFLAGS`*) and **`src/config.h`**. If you don't want 
multiple monitors support, make sure to completely remove **XINERAMA**.

## Installation
```bash
<superuser> make --jobs "$(nproc || printf '%s\n' 1)" install
```

## Running dynamd
Add the following line to your `~/.xinitrc` to start dynamd using `startx`:
```bash
exec dynamd
```

## Java Applications
Java application are known to misbehave as java doesn't know which WM are we using. After all this result in GUI of specific java application to don't work properly. To solve this we need to install wmname tool and set it to LG3D.
* Install <a href=https://tools.suckless.org/x/wmname>WMNAME</a> and execute `wmname LG3D` to fix Java application misbehaving. To make this setting permanent add this command to `~/.xinitrc`

## LICENSE
The project is licensed under the MIT license. For more information, see the `LICENSE` file.
