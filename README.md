# st - simple terminal
Fork of the [suckless terminal (st)](https://st.suckless.org/) with additional patches.

## Applied Patches:
- [scrollback](https://st.suckless.org/patches/scrollback/)
- [xresources](https://st.suckless.org/patches/xresources/)
- [boxdraw](https://st.suckless.org/patches/boxdraw/)

## Requirements
In order to build st you need the Xlib header files.

## Installation
Copy and edit config.def.h to config.h to configure st.

Afterwards enter the following command to build and install st (if necessary as root):
```bash
make clean install
```
