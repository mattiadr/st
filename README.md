# st - simple terminal
Fork of the [suckless terminal (st)](https://st.suckless.org/) with additional patches.

## Applied Patches:
- [scrollback](https://st.suckless.org/patches/scrollback/)
- [xresources](https://st.suckless.org/patches/xresources/)
- [boxdraw](https://st.suckless.org/patches/boxdraw/)
- [right click to plumb](https://st.suckless.org/patches/right_click_to_plumb/)

## Requirements
In order to build st you need the Xlib header files.

## Installation
Copy and edit config.def.h to config.h to configure st.

Afterwards enter the following command to build and install st (if necessary as root):
```bash
make clean install
```

or you can install it [from the AUR](https://aur.archlinux.org/packages/st-mattiadr).

## Xresources
Various options can be configured from `~/.Xresources` using the syntax `st.option: value`:
- `font`
- `color0 ` to `color15`
- `foreground`
- `background`
- `cursor` - cursor color
- `reverseCursor` - reverse cursor color
- `termname`
- `shell`
- `xfps` - frames per second st should at maximum draw to the screen
- `actionfps`
- `blinktimeout` - blinking timeout (set to 0 to disable blinking) for the terminal blinking attribute
- `bellvolume`
- `tabspaces`
- `borderpx`
- `cwscale` - Kerning / character bounding-box multipliers
- `chscale`

## Right click to plumb
When you right click the selected text will be plumbed to the set command, if no text is selected then the word below the cursor will be automatically selected.

You can set the command to execute in the config.h, it defaults to `xdg-open %s`.

You have to include `%s` in the command, it will be substituted with the selected text.
