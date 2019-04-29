# Hornblende - A Custom Build of Debian ARM64 with Dark Theme for Radxa Rock Pi 4
*Build 4.4.154.c83*

This is a Debian ARM64 build forked from Radxa (the manufacturer)'s repository (https://github.com/radxa/rockchip-bsp), with extra customized features and tunings.

The kernel version has a prefix "*c*" (*custom*) in the local version number and aligned with Radxa's official build, e.g. 4.4.154.*c*83 is based on Radxa's 4.4.154.83. 

Installed Packages after Build:
- auto-config
- automake
- cmake
- xmms2
- rsync
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
- OTG support is turned off in the kernel, to enable ethernet over USB.
- Enabled ttyS2 on GPIO pin 8/10 for HATs
- Chromium GPU acceleration flags.
- “Open Folder as Root” context menu in File Manager.
- Bluetooth is turned on by default.

![Screenshot](Screenshot%20from%202019-04-18%2006-13-50.png)

Don't Forget:
- Set up timezone by link timezone file to /etc/localtime, e.g.:
  sudo ln -sf /usr/share/zoneinfo/America/Chicago /etc/localtime
- Set up locale:
  sudo dpkg-reconfigure locales
