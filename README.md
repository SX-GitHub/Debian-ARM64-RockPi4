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
- libmraa (build using the source code from https://github.com/brian541/mraa 1)
- gnome-screenshot

Fonts:
- SourceCodePro (Powerline fonts)
- Dejavu (Powerline fonts)
- fonts-noto (Google “no tofu” fonts)
- fonts-noto-cjk (Google “no tofu” fonts)

Themes:
- Adapta (https://github.com/adapta-project/adapta-gtk-theme) with custom color scheme, reduced the blue tint which would cause eye strain.
- DarkPaper icon theme based on the Paper (https://github.com/snwh/paper-icon-theme)
- Springfield VIM theme, based on the Behelit theme from https://github.com/vim-airline/vim-airline-themes

Tunings:
- Enabled ttyS2 on GPIO pin 8/10 for HATs
- Chromium GPU acceleration flags.
- “Open Folder as Root” context menu in File Manager

Known Issues:
- The libmraa from Radxa apt repository is not compatible with Debian ARM64, the upgrade should be set on hold:
  sudo apt-mark hold libmraa-rockpi4
- The root partition of the image is 3.0GB, you may need to increase the partition on your microSD card/EMMC
