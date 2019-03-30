# Debian-ARM64 for RockPi4

This is a Debian ARM64 build using the source code from Radxa (the manufacturer)'s repository (https://github.com/radxa/rockchip-bsp), with extra customized features and tunings.

Installed Packages after Build:
- auto-config
- automake
- make
- cmake
- xmms2
- openssh-server (re-installed)
- rsync
- libmraa (build using the source code from https://github.com/brian541/mraa)
- gnome-screenshot

Themes:
- Adapta (https://github.com/adapta-project/adapta-gtk-theme) with custom color scheme, reduced the blue tint which would cause eye strain.
- DarkPaper icon theme based on the Paper (https://github.com/snwh/paper-icon-theme)
- Springfield VIM theme, based on the Behelit theme from https://github.com/vim-airline/vim-airline-themes

Tunings:
- Chromium GPU acceleration flags.
